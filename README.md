# EMIS Health (emis-health)

EMIS Health is a United Kingdom health-technology company and one of the two dominant GP clinical-system providers in the NHS (alongside TPP SystmOne), supplying the EMIS Web electronic patient record used across primary care, community pharmacy, and other care settings. EMIS is migrating from EMIS Web to EMIS-X, a cloud-first platform, and exposes third-party integration through the gated EMIS Partner Developer Portal at [docs.partner.emis-x.uk](https://docs.partner.emis-x.uk/).

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/emis-health/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/emis-health/refs/heads/main/apis.yml)

## Tags

- Healthcare
- United Kingdom
- EHR
- EMR
- Interoperability
- HL7
- FHIR
- Primary Care
- NHS
- Clinical Data
- Electronic Patient Record

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### EMIS Partner API (PAPI)

A RESTful JSON API for EMIS-X / EMIS Web integration, exposing appointments, the clinical/medical record, patient demographics, patient matching, organisation lookup, and clinical searches. Documented as OpenAPI 3.0.4 (Partner API v1.2) with 40 operations. Access is OAuth2 authorization-code with scoped bearer (JWT) tokens.

- **Human URL:** [https://docs.partner.emis-x.uk/papi-overview](https://docs.partner.emis-x.uk/papi-overview)
- **Base URL:** `https://api.platform.emis-x.uk/partner`

#### Properties

- [OpenAPI](openapi/emis-health-partner-api-openapi.json)
- [Documentation](https://docs.partner.emis-x.uk/papi-overview)
- [API Reference](https://docs.partner.emis-x.uk/openapi/papi)
- [Authentication](https://docs.partner.emis-x.uk/auth/)

### EMIS-X App Launch

Launch partner applications in-context from within the EMIS-X / EMIS Web clinical workflow, passing authenticated user and patient context via the shared EMIS-X OAuth2 / OIDC authentication.

- **Human URL:** [https://docs.partner.emis-x.uk/emisx-app-launch/](https://docs.partner.emis-x.uk/emisx-app-launch/)

### EMIS-X Analytics

Partner access to an EMIS-X data warehouse with modelled datasets across Community Pharmacy, Incremental Primary Care Views (iPCVs), OpenSAFELY, Recruit, and IM1 Bulk Extract, browsable through the developer portal data explorer.

- **Human URL:** [https://docs.partner.emis-x.uk/getting-started/](https://docs.partner.emis-x.uk/getting-started/)

## Authentication

OAuth2 / OIDC via Microsoft Entra External ID (Azure AD B2C) at `identity.stg.emis-x.uk`, supporting authorization-code, PKCE, and client-credentials flows with scoped JWT bearer access tokens. PAPI OAuth2 scopes include `papi-appt.read`, `papi-appt.write`, `papi-cr.read`, `papi-cr.write`, `papi-subjects.read`, `papi-config.read`, and `papi-searches.read`. Native HL7 FHIR resource support is documented as upcoming; the current Partner API is REST JSON, not FHIR, and no SMART-on-FHIR configuration is served at review time.

## Common Properties

- [Website](https://www.emishealth.com/)
- [Developer Portal](https://docs.partner.emis-x.uk/)
- [Getting Started](https://docs.partner.emis-x.uk/getting-started/)
- [Onboarding](https://docs.partner.emis-x.uk/onboarding-one/)
- [Authentication](https://docs.partner.emis-x.uk/auth/)
- [Privacy Policy](https://www.emishealth.com/privacy-policy)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
