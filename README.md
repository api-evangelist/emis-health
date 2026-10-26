# EMIS Health (emis-health)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
