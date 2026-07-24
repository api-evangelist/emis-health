---
name: File a record into a patient's clinical record
description: Match a patient then file a clinical record entry into their EMIS-X medical record via the EMIS Partner API.
api: openapi/emis-health-partner-api-openapi.json
operations: [GetMatchedPatients, FileRecord]
scopes: [papi-subjects.read, papi-cr.write]
---

# File a record into a patient's clinical record

A write flow that adds an entry to the EMIS-X clinical record. Requires the
`papi-cr.write` scope plus the `clinical-cr.write` grant in the token's
`authorizations` claim.

## Steps

1. **Match the patient.** Call `GetMatchedPatients` to resolve the
   `patientNumber` for the target patient. Requires `papi-subjects.read`.
2. **File the record.** Call `FileRecord` (`POST /api/v1/medicalRecord/FileRecord`)
   with the record payload (`application/json` or `application/xml`). Requires
   `papi-cr.write`.

## Rules

- Include the `applicationId` header and a valid `Bearer` JWT with `papi-cr.write`;
  otherwise `401`.
- Send a supported `Content-Type` (`application/json` or `application/xml`) or
  you get `415` ("Media type not valid for URL").
- Malformed payloads return `400`; an unknown patient returns `404`.
- No idempotency contract is documented — guard against duplicate filings on the
  client side (check before re-sending after a timeout).
- Filing to a live clinical record is a safety-relevant write; only file what the
  partner agreement and clinician workflow authorize.
