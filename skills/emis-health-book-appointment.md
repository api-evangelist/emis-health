---
name: Find a slot and book an appointment
description: List appointment sessions and slots, book a patient into a slot, then set or cancel the appointment via the EMIS Partner API.
api: openapi/emis-health-partner-api-openapi.json
operations: [GetAppointmentSessions, GetSlotsForSession, BookAppointment, SetAppointmentStatus, CancelAppointment]
scopes: [papi-appt.read, papi-appt.write]
---

# Find a slot and book an appointment

Appointment lifecycle against `https://api.platform.emis-x.uk/partner`. Reads
require `papi-appt.read`; booking/status/cancel require `papi-appt.write`. Every
request needs an `applicationId` header and a `Bearer` JWT.

## Steps

1. **List sessions.** Call `GetAppointmentSessions` to find sessions for the
   organisation within a time frame. Requires `papi-appt.read`.
2. **List slots.** Call `GetSlotsForSession` with the `sessionId` to find free
   slots (each has a `slotId`).
3. **Book.** Call `BookAppointment` with the required query parameters `slotId`,
   `patientNumber`, `reason`, and `bookedBy` (optional `bookingNote`). Requires
   `papi-appt.write`.
4. **Update status.** Call `SetAppointmentStatus` (or `SetAppointmentStatusEx`)
   to move the appointment through arrived / sent-in / seen states.
5. **Cancel if needed.** Call `CancelAppointment` to release the booking.

## Rules

- `BookAppointment`, `CancelAppointment`, `SetAppointmentStatus` are declared
  `GET`/`PATCH` in the spec but require the `papi-appt.write` scope — send the
  correct scope or you get `401`.
- No idempotency-key mechanism is documented; do not blindly retry a book on a
  timeout — re-list slots first to avoid double-booking.
- A taken/invalid `slotId` returns `404`; malformed parameters return `400`.
- Errors are `PartnerApi.Service.Model.ErrorResponse`; capture `messageId`.
