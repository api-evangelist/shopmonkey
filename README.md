# Shopmonkey (shopmonkey)

Shopmonkey is a cloud-based shop management platform for auto repair, tire, and powersports shops, covering estimates, work orders, customer communication, parts/inventory, scheduling, invoicing, and payments. Shopmonkey publishes a documented public API at developer.shopmonkey.io / shopmonkey.dev (base `https://api.shopmonkey.cloud/v3`). Despite being commonly assumed to be GraphQL, the confirmed public API is REST/JSON (v3), authenticated with a Bearer API key, covering 50+ resources - Work Orders, Customers, Vehicles, Parts/Inventory, Invoices/Payments, Appointments, Employees (Users), Locations, and Webhooks. No GraphQL endpoint, schema, or query/mutation language is documented anywhere on Shopmonkey's developer site. Enterprise accounts can also run the open-source Enterprise Data Streaming (EDS) server for near-real-time change data capture into a customer-controlled destination.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/shopmonkey/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/shopmonkey/refs/heads/main/apis.yml)

> **Note on GraphQL:** this entry was originally scoped assuming Shopmonkey exposes a documented GraphQL API. Direct research (see `review.yml`) found that assumption to be false - Shopmonkey's developer docs explicitly state the API "is based on the REST standard." This repo therefore uses `openapi/` artifacts against the confirmed REST v3 surface, not `graphql/`.

## Tags

- Auto Repair
- Shop Management
- Field Service
- REST
- Not GraphQL

## Timestamps

- **Created:** 2026-07-04
- **Modified:** 2026-07-04

## APIs

### Shopmonkey Work Orders API

Create, update, search, and move work orders through shop workflow stages; manage order-level services, parts, labor, fees, tires, subcontracts, authorizations, files, and PDFs. Confirmed against shopmonkey.dev/resources/order.

- **Human URL:** [https://shopmonkey.dev/resources/order](https://shopmonkey.dev/resources/order)
- **Base URL:** `https://api.shopmonkey.cloud/v3`

#### Tags

- Work Orders
- Orders
- Service

#### Properties

- [Documentation](https://shopmonkey.dev/overview)
- [API Reference](https://shopmonkey.dev/resources/order)
- [OpenAPI](openapi/shopmonkey-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shopmonkey.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shopmonkey.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shopmonkey Customers API

Create, update, soft-delete, and search customer records; manage a customer's emails and phone numbers; list a customer's vehicles, orders, and deferred services. Confirmed against shopmonkey.dev/resources/customer.

- **Human URL:** [https://shopmonkey.dev/resources/customer](https://shopmonkey.dev/resources/customer)
- **Base URL:** `https://api.shopmonkey.cloud/v3`

#### Tags

- Customers
- CRM

#### Properties

- [Documentation](https://shopmonkey.dev/overview)
- [API Reference](https://shopmonkey.dev/resources/customer)
- [OpenAPI](openapi/shopmonkey-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shopmonkey.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shopmonkey.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shopmonkey Vehicles API

Create and update vehicles; validate VINs and license plates; look up year/make/model/submodel data; track mileage and tire-pressure logs, ownership history, and deferred services. Confirmed against shopmonkey.dev/resources/vehicle.

- **Human URL:** [https://shopmonkey.dev/resources/vehicle](https://shopmonkey.dev/resources/vehicle)
- **Base URL:** `https://api.shopmonkey.cloud/v3`

#### Tags

- Vehicles
- VIN
- Fitment

#### Properties

- [Documentation](https://shopmonkey.dev/overview)
- [API Reference](https://shopmonkey.dev/resources/vehicle)
- [OpenAPI](openapi/shopmonkey-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shopmonkey.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shopmonkey.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shopmonkey Inventory & Parts API

List, search, and summarize parts inventory; find vehicle-compatible parts; manage bulk line-item assignments of parts, tires, and labor to order services. Confirmed against shopmonkey.dev/resources/part.

- **Human URL:** [https://shopmonkey.dev/resources/part](https://shopmonkey.dev/resources/part)
- **Base URL:** `https://api.shopmonkey.cloud/v3`

#### Tags

- Inventory
- Parts
- Tires

#### Properties

- [Documentation](https://shopmonkey.dev/overview)
- [API Reference](https://shopmonkey.dev/resources/part)
- [OpenAPI](openapi/shopmonkey-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shopmonkey.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shopmonkey.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shopmonkey Invoices & Payments API

Retrieve customer-shared order PDFs and signed invoices, search payments, and record or refund manual payments against an order. Confirmed against shopmonkey.dev/resources/payment and the order_shared endpoints surfaced under shopmonkey.dev/resources/order.

- **Human URL:** [https://shopmonkey.dev/resources/payment](https://shopmonkey.dev/resources/payment)
- **Base URL:** `https://api.shopmonkey.cloud/v3`

#### Tags

- Invoices
- Payments
- Refunds

#### Properties

- [Documentation](https://shopmonkey.dev/overview)
- [API Reference](https://shopmonkey.dev/resources/payment)
- [OpenAPI](openapi/shopmonkey-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shopmonkey.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shopmonkey.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shopmonkey Appointments API

Create, update, search, confirm, and cancel shop appointments, including recurring appointment modifications. Confirmed against shopmonkey.dev/resources/appointment.

- **Human URL:** [https://shopmonkey.dev/resources/appointment](https://shopmonkey.dev/resources/appointment)
- **Base URL:** `https://api.shopmonkey.cloud/v3`

#### Tags

- Appointments
- Scheduling

#### Properties

- [Documentation](https://shopmonkey.dev/overview)
- [API Reference](https://shopmonkey.dev/resources/appointment)
- [OpenAPI](openapi/shopmonkey-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shopmonkey.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shopmonkey.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shopmonkey Employees API

List, create, and update Shopmonkey users (employees), assign roles, change passwords, and fetch the currently authenticated user. Confirmed against shopmonkey.dev/resources/user.

- **Human URL:** [https://shopmonkey.dev/resources/user](https://shopmonkey.dev/resources/user)
- **Base URL:** `https://api.shopmonkey.cloud/v3`

#### Tags

- Employees
- Users
- Roles

#### Properties

- [Documentation](https://shopmonkey.dev/overview)
- [API Reference](https://shopmonkey.dev/resources/user)
- [OpenAPI](openapi/shopmonkey-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shopmonkey.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shopmonkey.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shopmonkey Locations API

Update shop location data - address, contact details, timezone, and display preferences - for companies operating multiple locations. Only a PUT endpoint is explicitly documented; GET-by-id is modeled by convention. Confirmed against shopmonkey.dev/resources/location.

- **Human URL:** [https://shopmonkey.dev/resources/location](https://shopmonkey.dev/resources/location)
- **Base URL:** `https://api.shopmonkey.cloud/v3`

#### Tags

- Locations
- Multi-Shop

#### Properties

- [Documentation](https://shopmonkey.dev/overview)
- [API Reference](https://shopmonkey.dev/resources/location)
- [OpenAPI](openapi/shopmonkey-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shopmonkey.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shopmonkey.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### Shopmonkey Webhooks API

Create, retrieve, update, and delete webhook subscriptions that push Shopmonkey events (scoped company-wide or per-location) to an external URL, with error-state tracking. Confirmed against shopmonkey.dev/resources/webhook.

- **Human URL:** [https://shopmonkey.dev/resources/webhook](https://shopmonkey.dev/resources/webhook)
- **Base URL:** `https://api.shopmonkey.cloud/v3`

#### Tags

- Webhooks
- Events
- Integrations

#### Properties

- [Documentation](https://shopmonkey.dev/overview)
- [API Reference](https://shopmonkey.dev/resources/webhook)
- [OpenAPI](openapi/shopmonkey-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/shopmonkey.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/shopmonkey.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [GitHub Organization](https://github.com/shopmonkeyus)
- [LinkedIn](https://www.linkedin.com/company/shopmonkey)
- [Website](https://www.shopmonkey.io/)
- [Documentation](https://shopmonkey.dev/overview)
- [Plans](plans/shopmonkey-plans-pricing.yml)
- [Rate Limits](rate-limits/shopmonkey-rate-limits.yml)
- [Fin Ops](finops/shopmonkey-finops.yml)

## Review

Does Shopmonkey expose a documented public WebSocket API? **No.** See [review.yml](review.yml) for the full findings, including why no `graphql/` or `asyncapi/` artifacts were created for this entry.

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
