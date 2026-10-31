# SavvyMoney

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

SavvyMoney is a Dublin, California based financial technology company that supplies credit score, credit monitoring, financial wellness, pre-qualified offer and digital account-opening software to banks and credit unions. Its platform is delivered embedded inside a financial institution's existing online and mobile banking rather than as a standalone destination, and SavvyMoney states it is live across 70+ pre-built integrations spanning 40+ digital banking platforms including Alkami, Fiserv, Q2, Lumin and Candescent. The technical surface partners integrate against is a partner-scoped REST API on creditscore.savvymoney.com: a JWT-based Single Sign-On API (authenticate, sign-on, optional browser fingerprint, prolong, log off, and a RelayPost form endpoint) that hands a partner's authenticated member into SavvyMoney without a second credential, plus an External Credit API that returns User Status and User Credit Score data so the partner can render score, score change and monitoring alerts in its own UI. Embeddable iFrame widgets (score widget, offer widget, desktop and mobile dashboards) are published alongside the API, and a documented beta environment runs at creditscoretest.savvymoney.com. Credentials, the full API document and the partner hub are gated behind a partner agreement; no OpenAPI, AsyncAPI, SDK, MCP server or agent card is published publicly.

**Areas:** Company · Financial Services · Credit Score · Credit Monitoring · Financial Wellness · Banking · Credit Union · Fintech · SSO · Embedded Finance · Lending · Account Opening

## SavvyMoney on APIs.io

Everything profiled for SavvyMoney is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/savvymoney/](https://apis.io/providers/savvymoney/)** — or go straight to one of the APIs or properties below.

### APIs (2)

- [SavvyMoney SSO REST API](https://apis.io/apis/savvymoney/savvymoney-sso-rest-api/) — JWT-based Single Sign-On REST API that lets a partner's online or mobile banking platform transfer an authenticated member into SavvyMoney without a second…
- [SavvyMoney External Credit API](https://apis.io/apis/savvymoney/savvymoney-external-credit-api/) — Partner-facing REST API that returns select credit data for an SSO-identified member so the partner can render it inside its own experience. SavvyMoney's…

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Savvymoney Authentication](https://apis.io/security/savvymoney/savvymoney-authentication/)
- [Savvymoney Domain Security](https://apis.io/security/savvymoney/savvymoney-domain-security/)
- [Savvymoney Trust Center](https://apis.io/security/savvymoney/savvymoney-trust-center/)
- [Savvymoney Vulnerability Disclosure](https://apis.io/security/savvymoney/savvymoney-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Savvymoney Scopes](https://apis.io/scopes/savvymoney/savvymoney-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Savvymoney Plans Pricing](https://apis.io/plans/savvymoney/savvymoney-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Savvymoney Rate Limits](https://apis.io/rate-limits/savvymoney/savvymoney-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.savvymoney.com/)
- [Documentation](https://www.savvymoney.com/why-savvymoney/integration-partners/)
- [Sign up](https://www.savvymoney.com/book-a-demo/)
- [Support](https://www.savvymoney.com/book-a-demo/)
- [Blog](https://www.savvymoney.com/category/news/)
- [Trust centre](https://trust.savvymoney.com/)
- [Terms of service](https://www.savvymoney.com/terms-of-service/)
- [Privacy policy](https://www.savvymoney.com/privacy-policy/)
- [Status](https://status.savvymoney.com/)

## API Evangelist rating

**Kin Score 37.9** — thin · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 0.0 |
| Contract governance | 18.2 |
| Operational transparency | 42.1 |
| Developer ergonomics | 45.2 |
| Access clarity | 50.0 |

**Agent readiness 16.2** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | — |
| Agentic Access | — |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |

**Regulatory alignment 46.5** — Banking & Open Finance

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/savvymoney/](https://apis.io/providers/savvymoney/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for SavvyMoney: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/savvymoney/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
