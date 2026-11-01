# Uplisting

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

Uplisting is short-term and vacation rental management software and a channel manager for professional hosts and property managers. It syncs listings, bookings, availability, rates, and guest messaging across Airbnb, Vrbo, and Booking.com, and powers a direct booking website and unified inbox. Uplisting exposes an invite-only Public and Partner REST API at https://connect.uplisting.io for reading properties, bookings, availability, and calendar (prices and restrictions), plus webhooks that push booking changes to partner endpoints. Authentication is HTTP Basic with a Base64-encoded API key generated on the Connect page. Uplisting is part of the AirDNA family.

**Areas:** Vacation Rentals · Short-Term Rental · Channel Manager · Property Management · Booking · Hospitality

## Uplisting on APIs.io

Everything profiled for Uplisting is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/uplisting/](https://apis.io/providers/uplisting/)** — or go straight to one of the APIs or properties below.

### APIs (9)

- [Uplisting Account API](https://apis.io/apis/uplisting/uplisting-account-api/) — Authenticated account/user context.
- [Uplisting Availability API](https://apis.io/apis/uplisting/uplisting-availability-api/) — Properties available for a date range.
- [Uplisting Bookings API](https://apis.io/apis/uplisting/uplisting-bookings-api/) — Reservations across all connected channels.
- [Uplisting Calendar API](https://apis.io/apis/uplisting/uplisting-calendar-api/) — Availability, prices, and restrictions per property and date.
- [Uplisting Guests API](https://apis.io/apis/uplisting/uplisting-guests-api/) — Guest records tied to bookings (modeled).
- [Uplisting Messages API](https://apis.io/apis/uplisting/uplisting-messages-api/) — Guest messaging via the unified inbox (modeled).
- [Uplisting Properties API](https://apis.io/apis/uplisting/uplisting-properties-api/) — Properties (listings) in the account.
- [Uplisting Rates API](https://apis.io/apis/uplisting/uplisting-rates-api/) — Nightly rates and price adjustments (modeled via the calendar).
- [Uplisting Webhooks API](https://apis.io/apis/uplisting/uplisting-webhooks-api/) — Endpoints that receive booking change events.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [uplisting](https://apis.io/servers/uplisting/uplisting/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Uplisting Agentic Access](https://apis.io/agentic-access/uplisting/uplisting-agentic-access/)

#### Collections (10)

Postman and Open Collection request collections.

- [Uplisting Public and Partner API](https://apis.io/collections/uplisting/open-uplisting/)
- [Uplisting Public and Partner Account API](https://apis.io/collections/uplisting/open-uplisting-account-api/)
- [Uplisting Public and Partner Account Availability API](https://apis.io/collections/uplisting/open-uplisting-availability-api/)
- [Uplisting Public and Partner Account Bookings API](https://apis.io/collections/uplisting/open-uplisting-bookings-api/)
- [Uplisting Public and Partner Account Calendar API](https://apis.io/collections/uplisting/open-uplisting-calendar-api/)
- [Uplisting Public and Partner Account Guests API](https://apis.io/collections/uplisting/open-uplisting-guests-api/)
- [Uplisting Public and Partner Account Messages API](https://apis.io/collections/uplisting/open-uplisting-messages-api/)
- [Uplisting Public and Partner Account Properties API](https://apis.io/collections/uplisting/open-uplisting-properties-api/)
- [Uplisting Public and Partner Account Rates API](https://apis.io/collections/uplisting/open-uplisting-rates-api/)
- [Uplisting Public and Partner Account Webhooks API](https://apis.io/collections/uplisting/open-uplisting-webhooks-api/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Uplisting Authentication](https://apis.io/security/uplisting/uplisting-authentication/)
- [Uplisting Domain Security](https://apis.io/security/uplisting/uplisting-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Uplisting Plans Pricing](https://apis.io/plans/uplisting/uplisting-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Uplisting Rate Limits](https://apis.io/rate-limits/uplisting/uplisting-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Uplisting Finops](https://apis.io/finops/uplisting/uplisting-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.uplisting.io)
- [Documentation](https://support.uplisting.io/docs/api)
- [Blog](https://www.uplisting.io/blog)

## API Evangelist rating

**Kin Score 23.7** — emerging · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 68.3 |
| Contract quality | 44.8 |
| Contract governance | 0.0 |
| Operational transparency | 7.9 |
| Developer ergonomics | 21.4 |
| Access clarity | 7.9 |

**Agent readiness 42.4** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
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
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 11.8** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/uplisting/](https://apis.io/providers/uplisting/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Uplisting: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/uplisting/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
