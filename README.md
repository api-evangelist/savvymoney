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

SavvyMoney supplies credit score, credit monitoring, financial wellness, pre-qualified offer and
digital account-opening software to banks and credit unions, delivered embedded inside a financial
institution's existing online and mobile banking. SavvyMoney states it is live across 70+ pre-built
integrations spanning 40+ digital banking platforms, including Alkami, Fiserv, Q2, Lumin and
Candescent.

## The API surface

Partners integrate against a partner-scoped REST API on `creditscore.savvymoney.com`:

- **SavvyMoney SSO REST API** — a JWT flow (authenticate, optional browser fingerprint, sign-on,
  prolong, log off, plus a `RelayPost` form endpoint for iFrame embedding) that hands a partner's
  already-authenticated member into SavvyMoney without a second credential. Access tokens live 10
  minutes. SAML 2.0 is documented as an alternative.
- **SavvyMoney External Credit API** — `User Status` and `User Credit Score`, so a partner can render
  score, score change and monitoring alerts in its own UI.
- **Embedded widgets** — hosted, SSO-gated iFrame surfaces: desktop and mobile dashboards, a score
  widget and an offer widget.

A full beta estate runs at `creditscoretest.savvymoney.com`.

## What is public, and what is not

Two integration guides — the SSO REST API guide (v2.1, 2022-08-08) and the Mobile Integration Guide
(v1.8, 2019-09-17) — are served without authentication from the partner-hub CDN, and they are the
source for most of this profile. The full endpoint reference ("SavvyMoney API Document"), credentials
and the Partner Hub itself are behind a partner agreement.

Not published anywhere on the estate: an OpenAPI or any other machine-readable contract, an AsyncAPI
or webhook surface, a first-party SDK in any package registry, a GitHub organisation, an MCP server,
an A2A agent card, a `security.txt`, a pricing page, or any rate limit.

## Notable findings

- **Errors are decoupled from HTTP status.** An unauthenticated `POST {}` to
  `/sso/api/rest/signon` returns **HTTP 200** carrying
  `{"errorMessage":"Missing authCode.","hasErrors":true}`. A client that branches on the status code
  alone reads a validation failure as a success.
- **Live status API.** `status.savvymoney.com` is an Atlassian Statuspage with a v2 JSON API and 20
  named components — including `SSO Service - Auth`, `Credit Service`, `Offers Engine` and a separate
  `Lending & Deposits - API Service`.
- **Strong published compliance posture.** SOC 2 Type 2, CSA STAR Level 1 and 2, CSA Trusted Cloud
  Provider, TRUSTe, GLBA, NIST CSF, CCPA/CPRA, with `security@savvymoney.com` and a Responsible
  Disclosure practice — but no RFC 9116 `security.txt` to make any of it machine-discoverable.
- **Documentation currency gap.** The newest dated API change SavvyMoney publishes anywhere is
  2022-08-08, four years before this pass — though the endpoints it describes were confirmed live.
- **`api.savvymoney.com` resolves but is unrouted**, answering "Site Not Configured | 404 Not Found"
  on every path. The real API host is `creditscore.savvymoney.com`.

See `apis.yml` for the full artifact index.
