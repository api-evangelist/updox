# Updox

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

Updox is a healthcare communication and patient engagement platform for in-person and virtual care, offering a single inbox for secure/direct messaging, electronic fax, document management, patient reminders, forms, and telehealth video chat, integrated with 100+ EHR and pharmacy management systems. Updox has been a part of EverCommerce (NASDAQ - EVCM) since its December 2020 acquisition. Updox exposes a documented public/partner API (an IO Docs explorer plus a knowledge-base API reference) used mainly by EHR, pharmacy, and integration partners; API access is granted via application credentials rather than open self-serve signup, and much of the endpoint surface below is modeled from Updox's documented functional areas and webhook catalog.

**Areas:** Healthcare · Patient Engagement · Secure Messaging · Electronic Fax · Telehealth · Document Management · HIPAA · EverCommerce

## Updox on APIs.io

Everything profiled for Updox is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/updox/](https://apis.io/providers/updox/)** — or go straight to one of the APIs or properties below.

### APIs (12)

- [Updox Direct Messaging API](https://apis.io/apis/updox/updox-direct-messaging-api/) — Send and receive HISP Direct secure messages between providers, with Direct Messaging webhooks for delivery/receipt events. Endpoints modeled from Updox's…
- [Updox Secure Conversation API](https://apis.io/apis/updox/updox-secure-conversation-api/) — Manage secure two-way patient conversations (secure text/SMS threads), with Secure Conversation Management webhooks for new-message events. Endpoints…
- [Updox Document Management API](https://apis.io/apis/updox/updox-document-management-api/) — Create, retrieve, and route documents within the Updox inbox, with Document Management webhooks for document lifecycle events. Endpoints modeled from…
- [Updox Patient Management API](https://apis.io/apis/updox/updox-patient-management-api/) — Create and update patient records and demographics that anchor reminders, forms, portal access, and conversations, with Patient Management webhooks.…
- [Updox Patient Portal API](https://apis.io/apis/updox/updox-patient-portal-api/) — Provision and manage patient portal access and portal messaging, with Patient Portal webhooks for portal activity. Endpoints modeled from Updox's documented…
- [Updox Reminders API](https://apis.io/apis/updox/updox-reminders-api/) — Schedule and manage appointment reminders and broadcast messages across text, voice, and email, with Reminders webhooks for confirmation/response events.…
- [Updox Forms API](https://apis.io/apis/updox/updox-forms-api/) — Send electronic intake and consent forms to patients and receive completed submissions, with Forms webhooks for completion events. Endpoints modeled from…
- [Updox Account Management API](https://apis.io/apis/updox/updox-account-management-api/) — Administer accounts, users, and application connectivity, including the tiered Ping health-check actions (Ping, PingWithApplicationAuth,…
- [Updox Address Book API](https://apis.io/apis/updox/updox-address-book-api/) — Practice-level contact/address-book actions.
- [Updox Faxing API](https://apis.io/apis/updox/updox-faxing-api/) — Inbound electronic fax retrieval.
- [Updox Ping API](https://apis.io/apis/updox/updox-ping-api/) — Connectivity and authentication health checks.
- [Updox Video Chat API](https://apis.io/apis/updox/updox-video-chat-api/) — Telehealth video call actions.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Updox Agentic Access](https://apis.io/agentic-access/updox/updox-agentic-access/)

#### Collections (4)

Postman and Open Collection request collections.

- [Updox IO API (Modeled) Address Book API](https://apis.io/collections/updox/open-updox-address-book-api/)
- [Updox IO API (Modeled) Address Book Faxing API](https://apis.io/collections/updox/open-updox-faxing-api/)
- [Updox IO API (Modeled) Address Book Ping API](https://apis.io/collections/updox/open-updox-ping-api/)
- [Updox IO API (Modeled) Address Book Video Chat API](https://apis.io/collections/updox/open-updox-video-chat-api/)

#### Security (1)

Authentication, trust centre, and vulnerability disclosure.

- [Updox Domain Security](https://apis.io/security/updox/updox-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Updox Plans Pricing](https://apis.io/plans/updox/updox-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Updox Rate Limits](https://apis.io/rate-limits/updox/updox-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Updox Finops](https://apis.io/finops/updox/updox-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.updox.com)
- [Documentation](https://help.updox.com/help/public-api)
- [API reference](https://updoxqa.com/api/newio)
- [Support](https://www.updox.com/support/)
- [Blog](https://www.updox.com/blog/)

## API Evangelist rating

**Kin Score 22.6** — emerging · rubric 0.24.0 · scored 2026-10-17

| Facet | Score |
|---|---|
| Discoverability | 66.1 |
| Contract quality | 42.6 |
| Contract governance | 0.0 |
| Operational transparency | 7.9 |
| Developer ergonomics | 22.6 |
| Access clarity | 7.9 |

**Agent readiness 15.4** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | — |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |

**Regulatory alignment 4.7** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/updox/](https://apis.io/providers/updox/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Updox: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/updox/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
