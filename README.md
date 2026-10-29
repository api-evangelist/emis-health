# EMIS Health

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

EMIS Health is a United Kingdom health-technology company and one of the two dominant GP clinical-system providers in the NHS (alongside TPP SystmOne), supplying the EMIS Web electronic patient record used across primary care, community pharmacy, and other care settings. EMIS is migrating from EMIS Web to EMIS-X, a cloud-first platform, and exposes third-party integration through the EMIS Partner Developer Portal at docs.partner.emis-x.uk. The gated partner programme documents a RESTful JSON Partner API (PAPI) covering appointments, the clinical/medical record, patient demographics and matching, organisation lookup and clinical searches, plus EMIS-X App Launch and an EMIS-X Analytics data warehouse. Authentication is OAuth2 / OIDC (Microsoft Entra External ID / Azure AD B2C) using authorization-code, PKCE, and client-credentials flows with scoped JWT access tokens; native HL7 FHIR resource support is documented as upcoming rather than yet available.

**Areas:** Healthcare · United Kingdom · Electronic Health Records · Interoperability · HL7 · FHIR · Primary Care · NHS · Clinical Data · Electronic Patient Record

## EMIS Health on APIs.io

Everything profiled for EMIS Health is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/emis-health/](https://apis.io/providers/emis-health/)** — or go straight to one of the APIs or properties below.

### APIs (12)

- [EMIS-X App Launch](https://apis.io/apis/emis-health/emis-x-app-launch/) — EMIS-X App Launch lets partner applications be launched in-context from within the EMIS-X / EMIS Web clinical workflow, passing an authenticated user and…
- [EMIS-X Analytics](https://apis.io/apis/emis-health/emis-x-analytics/) — EMIS-X Analytics provides partner access to an EMIS-X data warehouse with modelled datasets across domains including Community Pharmacy, Incremental Primary…
- [EMIS Health Appointments API](https://apis.io/apis/emis-health/emis-health-appointments-api/) — The appointments API from EMIS Health — 17 operation(s) for appointments.
- [EMIS Health CORS API](https://apis.io/apis/emis-health/emis-health-cors-api/) — The CORS API from EMIS Health — 40 operation(s) for cors.
- [EMIS Health API](https://apis.io/apis/emis-health/emis-health-health-api/) — The health API from EMIS Health — 1 operation(s) for health.
- [EMIS Health Medical Record API](https://apis.io/apis/emis-health/emis-health-medicalrecord-api/) — The medicalRecord API from EMIS Health — 12 operation(s) for medicalrecord.
- [EMIS Health Organisation API](https://apis.io/apis/emis-health/emis-health-organisation-api/) — The organisation API from EMIS Health — 2 operation(s) for organisation.
- [EMIS Health Patient API](https://apis.io/apis/emis-health/emis-health-patient-api/) — The patient API from EMIS Health — 1 operation(s) for patient.
- [EMIS Health Patient Matching API](https://apis.io/apis/emis-health/emis-health-patientmatching-api/) — The patientMatching API from EMIS Health — 4 operation(s) for patientmatching.
- [EMIS Health Search API](https://apis.io/apis/emis-health/emis-health-search-api/) — The search API from EMIS Health — 1 operation(s) for search.
- [EMIS Health Swagger API](https://apis.io/apis/emis-health/emis-health-swagger-api/) — The swagger API from EMIS Health — 1 operation(s) for swagger.
- [EMIS Health User API](https://apis.io/apis/emis-health/emis-health-user-api/) — The user API from EMIS Health — 1 operation(s) for user.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [emis-partner-api](https://apis.io/servers/emis-health/emis-partner-api/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Emis Health Agentic Access](https://apis.io/agentic-access/emis-health/emis-health-agentic-access/)

#### Collections (1)

Postman and Open Collection request collections.

- [Partner API](https://apis.io/collections/emis-health/open-emis-health-partner-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Emis Health Partner Api Overlay](https://apis.io/overlays/emis-health/emis-health-partner-api-overlay/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Emis Health Authentication](https://apis.io/security/emis-health/emis-health-authentication/)
- [Emis Health Domain Security](https://apis.io/security/emis-health/emis-health-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Emis Health Scopes](https://apis.io/scopes/emis-health/emis-health-scopes/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.emishealth.com/)
- [Documentation](https://docs.partner.emis-x.uk/getting-started/)
- [Getting started](https://docs.partner.emis-x.uk/getting-started/)
- [API reference](https://docs.partner.emis-x.uk/openapi/papi)
- [Blog](https://www.enliviohealth.com/news/news)
- [Privacy policy](https://www.emishealth.com/privacy-policy)

## API Evangelist rating

**Kin Score 34.6** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 64.3 |
| Contract quality | 42.7 |
| Contract governance | 4.5 |
| Operational transparency | 0.0 |
| Developer ergonomics | 61.3 |
| Access clarity | 10.5 |

**Agent readiness 31.8** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | — |
| Rate Limit Signal | — |
| Event Surface Described | — |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | documented (partial credit) |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 34.4** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/emis-health/](https://apis.io/providers/emis-health/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for EMIS Health: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/emis-health/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
