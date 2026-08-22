# Updox (updox)

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

Updox is a healthcare communication and patient engagement platform for in-person and virtual care, offering a single inbox for secure/direct messaging, electronic fax, document management, patient reminders, forms, and telehealth video chat. Updox is integrated with 100+ EHR and pharmacy management systems and has been a part of **EverCommerce** (NASDAQ: EVCM) since its **December 2020** acquisition.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/updox/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/updox/refs/heads/main/apis.yml)

## Access model (read this first)

Updox exposes a **documented but partner-gated** public API, not an open self-serve developer program:

- The API is a **POST-based "IO" API** surfaced through an **IO Docs explorer** at [updoxqa.com/api/newio](https://updoxqa.com/api/newio) (base `https://updoxqa.com/api/io`), plus a knowledge base at [help.updox.com](https://help.updox.com/help/public-api).
- Authentication is **tiered**: `applicationId` + `applicationPassword`, then `accountId`, then `userId`, depending on the action. Credentials are **issued by Updox to partners** (EHR, pharmacy, integration vendors) rather than created via open signup.
- Event delivery is by **HTTP webhooks** across eleven functional areas (no public WebSocket — see `review.yml`).
- The reachable reference host is the QA/IO Docs environment (`updoxqa.com`); the production base is provisioned per partner.

**Confirmed** from the IO Docs explorer and knowledge base: the `Ping` health checks, Address Book actions (`AddressBookList` incl. v1.1, `AddressBookSearch`, `ContactCreate`), the Faxing poll functions (`FaxOemPop`, `PopPDF`), and Video Chat `VideoCallActions` (`SendInvite`, retrieval). The remaining logical APIs below (Direct Messaging, Secure Conversation, Document Management, Patient Management, Patient Portal, Reminders, Forms, and the rest of Account Management) are **modeled** from Updox's documented functional areas and webhook catalog. The bundled OpenAPI (`openapi/updox-openapi.yml`) covers only the confirmed actions and is marked `x-modeled: true`.

## Tags

- Healthcare
- Patient Engagement
- Secure Messaging
- Electronic Fax
- Telehealth
- Document Management
- HIPAA
- EverCommerce

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## APIs

### Updox Address Book API
List, search, and create practice-level contacts — `AddressBookList` (with an international-address v1.1), `AddressBookSearch`, and `ContactCreate`. Confirmed in the IO Docs explorer. Base URL: `https://updoxqa.com/api/io`.

### Updox Faxing API
Send and retrieve electronic faxes. `FaxOemPop` and `PopPDF` are multifunction poll endpoints that report whether inbound faxes are queued, return the fax image (PNG or PDF) in the JSON response, and mark it handled via `lastRetrievedFaxId` until `endOfQueue`. Faxing webhooks notify partners of fax events.

### Updox Video Chat API
Telehealth video integration via `VideoCallActions` — `SendInvite` to invite a patient into an Updox Video Chat session, plus retrieval actions for call state. Paired with the Updox Video Chat web interface and video webhooks.

### Updox Direct Messaging API
HISP Direct secure messaging between providers, with Direct Messaging webhooks. *(Endpoints modeled from the documented functional area.)*

### Updox Secure Conversation API
Two-way secure patient conversations (secure text/SMS), with Secure Conversation Management webhooks. *(Modeled.)*

### Updox Document Management API
Create, retrieve, and route documents in the Updox inbox, with Document Management webhooks. *(Modeled.)*

### Updox Patient Management API
Create and update patient records/demographics that anchor reminders, forms, portal, and conversations, with Patient Management webhooks. *(Modeled.)*

### Updox Patient Portal API
Provision and manage patient portal access and portal messaging, with Patient Portal webhooks. *(Modeled.)*

### Updox Reminders API
Schedule appointment reminders and broadcast messages across text, voice, and email, with Reminders webhooks. *(Modeled.)*

### Updox Forms API
Send electronic intake/consent forms and receive completed submissions, with Forms webhooks. *(Modeled.)*

### Updox Account Management API
Administer accounts, users, and connectivity, including the tiered `Ping` health checks (confirmed) and Account Management webhooks. *(Remaining endpoints modeled.)*

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/updox)
- [Website](https://www.updox.com)
- [Documentation](https://help.updox.com/help/public-api)
- [API Reference (IO Docs)](https://updoxqa.com/api/newio)
- [Support](https://www.updox.com/support/)
- [Plans](plans/updox-plans-pricing.yml)
- [Rate Limits](rate-limits/updox-rate-limits.yml)
- [Fin Ops](finops/updox-finops.yml)
- [Blog](https://blog.updox.com)

## Pricing

Updox is subscription SaaS priced by practice size and capability mix; there is no public "buy now" list price. A [pricing calculator](https://www.updox.com/tools/updox-pricing-calculator/) and sales contact drive quotes. Reported tiers span a small/solo tier (~$49–$119 per provider/month), mid tiers with capped monthly allowances (faxes, telehealth sessions, reminders, broadcast messages), and a custom enterprise tier for larger practices, health systems, and EHR/pharmacy partners. API/integration access is provisioned to partners on top of a subscription rather than sold as a standalone metered API. See `plans/` and `finops/`.

## WebSocket Review

**Does Updox expose a documented public WebSocket API? No.** Updox's own public API is request/response HTTP POST (the IO API) and its event delivery is via HTTP webhooks — neither is a server-push WebSocket. No AsyncAPI document was authored. See `review.yml`.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
