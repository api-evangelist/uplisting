# Uplisting (uplisting)

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
