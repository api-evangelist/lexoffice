# lexoffice (lexoffice)

lexoffice - rebranded to **lexware Office** in 2025 - is a German cloud accounting, invoicing, and bookkeeping SaaS from Lexware (Haufe Group). Its public REST API lets developers push and pull business data - contacts, invoices, quotations, order confirmations, delivery notes, credit notes, dunnings, bookkeeping vouchers, files, payments, and profile metadata - and subscribe to webhooks through event subscriptions.

**Access model:** Self-serve. Any lexoffice / lexware Office customer on a paid plan can generate a private API key from the Public API add-on at [app.lexware.de/addons/public-api](https://app.lexware.de/addons/public-api) and start calling the API immediately - there is no partner application or OAuth client registration for the standard REST API. The key is a long-lived Bearer token, passed as `Authorization: Bearer YOUR_API_KEY`. The API is rate limited to **2 requests per second** per client (HTTP 429 on exceed).

**Rebrand / domain note:** As part of the lexoffice → lexware Office rebrand, the API gateway moved from `https://api.lexoffice.io` to `https://api.lexware.io` on **26 May 2025**; the legacy host remained available through December 2025. The developer portal is now [developers.lexware.io](https://developers.lexware.io/docs/) (developers.lexoffice.io redirects there). This catalog entry keeps the slug/aid `lexoffice` for continuity while naming the rebrand honestly. Current base URL: `https://api.lexware.io/v1`.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/lexoffice/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/lexoffice/refs/heads/main/apis.yml)

## Tags

- Accounting
- Invoicing
- Bookkeeping
- Finance
- Germany
- Vouchers
- Contacts
- SaaS
- Financial Software

## Timestamps

- **Created:** 2026-07-12
- **Modified:** 2026-07-12

## APIs

### lexoffice Contacts API

Create, retrieve, list, and update contacts - customers and vendors with company or person roles, addresses, contact persons, email/phone, and bank details. Contacts are referenced by invoices, vouchers, and other documents.

- **Human URL:** [https://developers.lexware.io/docs/#contacts-endpoint](https://developers.lexware.io/docs/#contacts-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Contacts
- Customers
- Vendors

#### Properties

- [Documentation](https://developers.lexware.io/docs/)
- [API Reference](https://developers.lexware.io/docs/#contacts-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lexoffice.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### lexoffice Invoices API

Create and retrieve invoices with line items, tax conditions, shipping, and payment conditions. Invoices are drafts by default; pass `finalize=true` to create them in the open status. Fetch the rendered PDF via the document and file sub-resources.

- **Human URL:** [https://developers.lexware.io/docs/#invoices-endpoint](https://developers.lexware.io/docs/#invoices-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Invoices
- Billing
- Documents

#### Properties

- [API Reference](https://developers.lexware.io/docs/#invoices-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lexoffice.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### lexoffice Quotations API

Create and retrieve quotations (offers) with line items, expiration dates, and tax conditions, then fetch the rendered PDF document for a sales offer.

- **Human URL:** [https://developers.lexware.io/docs/#quotations-endpoint](https://developers.lexware.io/docs/#quotations-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Quotations
- Offers
- Sales

#### Properties

- [API Reference](https://developers.lexware.io/docs/#quotations-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lexoffice.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### lexoffice Order Confirmations API

Create and retrieve order confirmations that acknowledge a customer order, with line items and tax conditions, plus the rendered PDF document.

- **Human URL:** [https://developers.lexware.io/docs/#order-confirmations-endpoint](https://developers.lexware.io/docs/#order-confirmations-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Order Confirmations
- Sales

#### Properties

- [API Reference](https://developers.lexware.io/docs/#order-confirmations-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### lexoffice Delivery Notes API

Create and retrieve delivery notes documenting shipped goods, with line items (without prices) and delivery details, plus the rendered PDF document.

- **Human URL:** [https://developers.lexware.io/docs/#delivery-notes-endpoint](https://developers.lexware.io/docs/#delivery-notes-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Delivery Notes
- Fulfillment

#### Properties

- [API Reference](https://developers.lexware.io/docs/#delivery-notes-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### lexoffice Credit Notes API

Create and retrieve credit notes (Rechnungskorrektur) that credit a customer, with line items and tax conditions, plus the rendered PDF document.

- **Human URL:** [https://developers.lexware.io/docs/#credit-notes-endpoint](https://developers.lexware.io/docs/#credit-notes-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Credit Notes
- Refunds

#### Properties

- [API Reference](https://developers.lexware.io/docs/#credit-notes-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### lexoffice Dunnings API

Create and retrieve dunnings (payment reminders) that reference a preceding open invoice, with line items and dunning level, plus the rendered PDF document.

- **Human URL:** [https://developers.lexware.io/docs/#dunnings-endpoint](https://developers.lexware.io/docs/#dunnings-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Dunnings
- Reminders
- Collections

#### Properties

- [API Reference](https://developers.lexware.io/docs/#dunnings-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### lexoffice Vouchers API

Manage bookkeeping vouchers (sales/purchase invoices and credit notes) - create, retrieve, update, delete, and search via the voucherlist - with voucher items, tax type, and posting categories. Upload and attach receipt files via the files endpoint.

- **Human URL:** [https://developers.lexware.io/docs/#vouchers-endpoint](https://developers.lexware.io/docs/#vouchers-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Vouchers
- Bookkeeping
- Files

#### Properties

- [API Reference](https://developers.lexware.io/docs/#vouchers-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/lexoffice.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### lexoffice Event Subscriptions API

Subscribe to change events (e.g. `contact.created`, `invoice.created`) by registering an HTTPS callback URL. lexoffice POSTs a webhook payload to your callback when a subscribed event fires. Create, list, retrieve, and delete subscriptions. These are server-to-endpoint HTTP callbacks, not a WebSocket.

- **Human URL:** [https://developers.lexware.io/docs/#event-subscriptions-endpoint](https://developers.lexware.io/docs/#event-subscriptions-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Webhooks
- Event Subscriptions
- Notifications

#### Properties

- [API Reference](https://developers.lexware.io/docs/#event-subscriptions-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### lexoffice Payments API

Retrieve the payment status and payment items recorded for a voucher, and list the payment conditions (terms and discounts) configured in the account.

- **Human URL:** [https://developers.lexware.io/docs/#payments-endpoint](https://developers.lexware.io/docs/#payments-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Payments
- Payment Conditions

#### Properties

- [API Reference](https://developers.lexware.io/docs/#payments-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### lexoffice Profile and Metadata API

Read account profile and connection metadata, the list of supported countries, posting categories used to classify vouchers, and recurring templates that generate recurring invoices.

- **Human URL:** [https://developers.lexware.io/docs/#profile-endpoint](https://developers.lexware.io/docs/#profile-endpoint)
- **Base URL:** `https://api.lexware.io/v1`

#### Tags

- Profile
- Metadata
- Recurring Templates

#### Properties

- [API Reference](https://developers.lexware.io/docs/#profile-endpoint)
- [OpenAPI](openapi/lexoffice-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Open Collection](collections/lexoffice.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Domain Security](security/lexoffice-domain-security.yml)
- [Authentication](authentication/lexoffice-authentication.yml)
- [LinkedIn](https://www.linkedin.com/company/lexware)
- [Website](https://www.lexware.de/lexware-office/)
- [Documentation](https://developers.lexware.io/docs/)
- [Plans](plans/lexoffice-plans-pricing.yml)
- [Rate Limits](rate-limits/lexoffice-rate-limits.yml)
- [Fin Ops](finops/lexoffice-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
