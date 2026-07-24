---
name: Retrieve a patient's medical record
description: Match a patient, confirm demographics, and read their EMIS-X clinical record (coded record, medication) via the EMIS Partner API.
api: openapi/emis-health-partner-api-openapi.json
operations: [GetMatchedPatients, GetPatientDemographics, GetMedicalRecord, GetCodedRecord, GetMedicationIssues]
scopes: [papi-subjects.read, papi-cr.read]
---

# Retrieve a patient's medical record

Read-only clinical retrieval from EMIS-X. All requests are `GET` against
`https://api.platform.emis-x.uk/partner`, require an `applicationId` header, and
a `Bearer` JWT with the `papi-subjects.read` and `papi-cr.read` scopes (and the
`clinical-cr.read` grant in the token's `authorizations` claim).

## Steps

1. **Match the patient.** Call `GetMatchedPatients` with the demographic search
   criteria to resolve a `patientNumber`. Requires `papi-subjects.read`.
2. **Confirm demographics.** Call `GetPatientDemographics` with the
   `patientNumber` to verify identity before reading clinical data.
3. **Read the record.** Call `GetMedicalRecord` for the full record, or
   `GetCodedRecord` for the coded (SNOMED) entries only. Requires `papi-cr.read`.
4. **Read medication.** Call `GetMedicationIssues` for the patient's medication
   issues.

## Rules

- Send `applicationId` on every request; a missing/invalid token returns `401`
  ("Authentication token not valid") — refresh the JWT (tokens last ~1 hour).
- A bad `patientNumber` or out-of-scope resource returns `404`.
- Errors come back as `PartnerApi.Service.Model.ErrorResponse`
  (`messageId`, `text`, `issue`, `legacyOutcome`) — log the `messageId` for support.
- This is real patient data under NHS information governance; only read what the
  partner agreement authorizes.
