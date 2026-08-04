# Uplisting (uplisting)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Uplisting is short-term and vacation rental management software and a channel manager for professional hosts and property managers. It syncs listings, bookings, availability, rates, and guest messaging across Airbnb, Vrbo, and Booking.com, and powers a direct booking website and unified inbox. Uplisting exposes an invite-only Public and Partner REST API at `https://connect.uplisting.io` for reading properties, bookings, availability, and calendar (prices and restrictions), creating confirmed bookings, and registering webhooks that push booking changes. Authentication is HTTP Basic with a Base64-encoded API key generated on the Connect page. Uplisting is part of the AirDNA family.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/uplisting/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/uplisting/refs/heads/main/apis.yml)

> **API access is invite-only.** Request access and the full reference (an invite-only Postman collection) from support@uplisting.io. The Users, Properties, Bookings, Availability, and Calendar surfaces plus the webhook, rate-limit, and response-code behaviors below are confirmed from Uplisting's public documentation. Individual-resource fetches and the Rates, Guests, and Messages resources are honestly modeled from Uplisting's documented product behavior and marked as such.

## Tags

- Vacation Rental
- Short-Term Rental
- Channel Manager
- Property Management
- Bookings
- Hospitality

## Timestamps

- **Created:** 2026-07-03
- **Modified:** 2026-07-03

## Authentication

HTTP Basic auth: send `Authorization: Basic <base64(api_key)>`. API keys are generated on the Uplisting Connect page. V2 endpoints additionally require a Client ID partner identifier. Staging and production share the same paths on different base domains, with environment-specific accounts and keys.

## APIs

### Uplisting Bookings API

Retrieve a snapshot list of bookings and individual booking detail, and create confirmed bookings, across all connected channels (Airbnb, Vrbo, Booking.com, and the Uplisting direct booking website). Booking changes are then pushed via webhooks.

- **Human URL:** [https://support.uplisting.io/docs/api](https://support.uplisting.io/docs/api)
- **Base URL:** `https://connect.uplisting.io`

#### Tags

- Bookings
- Reservations

#### Properties

- [Documentation](https://support.uplisting.io/docs/api)
- [API Reference](https://documenter.getpostman.com/view/1320372/SWTBfdW6)
- [OpenAPI](openapi/uplisting-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uplisting.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uplisting.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Uplisting Properties API

List the properties (listings) in an Uplisting account and retrieve detail for a single property, including the property slug used to build direct booking and payment-page links.

- **Human URL:** [https://support.uplisting.io/docs/api](https://support.uplisting.io/docs/api)
- **Base URL:** `https://connect.uplisting.io`

#### Tags

- Properties
- Listings

#### Properties

- [Documentation](https://support.uplisting.io/docs/api)
- [OpenAPI](openapi/uplisting-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uplisting.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uplisting.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Uplisting Availability API

Return the list of properties that are available for a given date range, optionally filtered by number of guests. Used to power search on the direct booking widget and website.

- **Human URL:** [https://support.uplisting.io/docs/api](https://support.uplisting.io/docs/api)
- **Base URL:** `https://connect.uplisting.io`

#### Tags

- Availability
- Search

#### Properties

- [Documentation](https://support.uplisting.io/docs/api)
- [OpenAPI](openapi/uplisting-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uplisting.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uplisting.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Uplisting Calendar API

Retrieve availability, prices, and restrictions (minimum stay, closed to arrival/departure) for a property across a date range, and submit calendar updates. Calendar update calls are accepted asynchronously (HTTP 202).

- **Human URL:** [https://support.uplisting.io/docs/api](https://support.uplisting.io/docs/api)
- **Base URL:** `https://connect.uplisting.io`

#### Tags

- Calendar
- Availability
- Restrictions

#### Properties

- [Documentation](https://support.uplisting.io/docs/api)
- [OpenAPI](openapi/uplisting-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uplisting.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uplisting.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Uplisting Rates API

Read and push nightly rates and price adjustments per property and date, delivered through the calendar surface. Rate updates propagate out to the connected channels. Endpoint shapes are modeled from the documented calendar and pricing behavior; confirm exact paths under the invite-only reference.

- **Human URL:** [https://support.uplisting.io/docs/api](https://support.uplisting.io/docs/api)
- **Base URL:** `https://connect.uplisting.io`

#### Tags

- Rates
- Pricing

#### Properties

- [Documentation](https://support.uplisting.io/docs/api)
- [OpenAPI](openapi/uplisting-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uplisting.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uplisting.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Uplisting Guests API

Read guest records associated with bookings - name, contact details, and identity-verification status. Guest resources are modeled from Uplisting's documented booking and guest-verification features; confirm exact paths under the invite-only reference.

- **Human URL:** [https://support.uplisting.io/docs/api](https://support.uplisting.io/docs/api)
- **Base URL:** `https://connect.uplisting.io`

#### Tags

- Guests
- Contacts

#### Properties

- [Documentation](https://support.uplisting.io/docs/api)
- [OpenAPI](openapi/uplisting-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uplisting.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uplisting.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Uplisting Messages API

Read and send guest messages tied to a booking through Uplisting's unified inbox, which consolidates Airbnb, Vrbo, and Booking.com conversations. Message resources are modeled from the documented automated-messaging and inbox features; confirm exact paths under the invite-only reference.

- **Human URL:** [https://support.uplisting.io/docs/api](https://support.uplisting.io/docs/api)
- **Base URL:** `https://connect.uplisting.io`

#### Tags

- Messages
- Unified Inbox

#### Properties

- [Documentation](https://support.uplisting.io/docs/api)
- [OpenAPI](openapi/uplisting-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uplisting.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uplisting.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Uplisting Webhooks API

Register, list, and remove webhook endpoints that receive booking created, updated, and removed events. Endpoints must return a 2xx response within 5 seconds; an endpoint is auto-disabled after 5 consecutive failed deliveries. Webhooks are the recommended way to stay in sync after an initial snapshot.

- **Human URL:** [https://support.uplisting.io/docs/api](https://support.uplisting.io/docs/api)
- **Base URL:** `https://connect.uplisting.io`

#### Tags

- Webhooks
- Events

#### Properties

- [Documentation](https://support.uplisting.io/docs/api)
- [OpenAPI](openapi/uplisting-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/uplisting.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/uplisting.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [LinkedIn](https://www.linkedin.com/company/uplisting)
- [Website](https://www.uplisting.io)
- [Documentation](https://support.uplisting.io/docs/api)
- [Plans](plans/uplisting-plans-pricing.yml)
- [Rate Limits](rate-limits/uplisting-rate-limits.yml)
- [Fin Ops](finops/uplisting-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
