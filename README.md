# Mailchimp (mailchimp)

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

Mailchimp is an Intuit company providing a marketing automation platform and email marketing service for managing mailing lists, creating email marketing campaigns, and automating marketing workflows.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/mailchimp/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/mailchimp/refs/heads/main/apis.yml)

## Tags

- Campaigns
- Email Marketing
- Marketing Automation
- Newsletters
- Transactional Email

## Timestamps

- **Created:** 2023/11/23
- **Modified:** 2026-05-30

## APIs

### Mailchimp Marketing API

The Mailchimp Marketing API provides programmatic access to Mailchimp data and functionality, allowing developers to build custom features to sync email activity and campaign analytics with their database, manage audiences and campaigns, and more.

- **Human URL:** [https://mailchimp.com/developer/marketing/](https://mailchimp.com/developer/marketing/)
- **Base URL:** `https://server.api.mailchimp.com/3.0`

#### Tags

- Audiences
- Automation
- Campaigns
- Email Marketing

#### Properties

- [Documentation](https://mailchimp.com/developer/marketing/docs/fundamentals/)
- [OpenAPI](openapi/mailchimp-marketing-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mailchimp-marketing-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mailchimp-marketing-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [AsyncAPI](openapi/mailchimp-marketing-webhooks-asyncapi.yml) — [AsyncAPI Specification](https://www.asyncapi.com/docs/reference/specification/latest)
- [JSON Schema](json-schema/campaign.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/audience.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/member.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/template.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Integrations](https://mailchimp.com/developer/marketing/docs/integrations/)
- [Errors](https://mailchimp.com/developer/marketing/docs/errors/)
- [API Reference](https://mailchimp.com/developer/marketing/api/)
- [Getting Started](https://mailchimp.com/developer/marketing/guides/quick-start/)
- [Authentication](https://mailchimp.com/developer/marketing/guides/access-user-data-oauth-2/)
- [E- Commerce](https://mailchimp.com/developer/marketing/docs/e-commerce/)
- [Methods and  Parameters](https://mailchimp.com/developer/marketing/docs/methods-parameters/)

### Mailchimp Transactional API

Mailchimp Transactional (formerly Mandrill) is a powerful email delivery service that lets you send personalized, one-to-one emails like password resets, order confirmations, and welcome messages.

- **Human URL:** [https://mailchimp.com/developer/transactional/](https://mailchimp.com/developer/transactional/)
- **Base URL:** `https://mandrillapp.com/api/1.0`

#### Tags

- Email Delivery
- Messaging
- Transactional Email

#### Properties

- [Documentation](https://mailchimp.com/developer/transactional/docs/fundamentals/)
- [OpenAPI](openapi/mailchimp-transactional-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/mailchimp-transactional-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mailchimp-transactional-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON-LD](json-ld/context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)
- [Getting Started](https://mailchimp.com/developer/transactional/guides/quick-start/)
- [Authentication](https://mailchimp.com/developer/transactional/docs/authentication-delivery/)
- [Webhooks](https://mailchimp.com/developer/transactional/docs/webhooks/)
- [API Reference](https://mailchimp.com/developer/transactional/api/)
- [Getting Started](https://mailchimp.com/developer/transactional/guides/send-first-email/)
- [Outbound  Email](https://mailchimp.com/developer/transactional/docs/outbound-email/)
- [Tags and  Metadata](https://mailchimp.com/developer/transactional/docs/tags-metadata/)

### Mailchimp Open Commerce

An open source, API-first, modular commerce stack built using Node.js, React, and GraphQL. Formerly known as Reaction Commerce, the project has been discontinued but documentation remains available.

- **Human URL:** [https://mailchimp.com/developer/open-commerce/](https://mailchimp.com/developer/open-commerce/)
- **Base URL:** `https://api.example.com`

#### Tags

- E-Commerce
- GraphQL
- Headless Commerce

#### Properties

- [Documentation](https://mailchimp.com/developer/open-commerce/docs/fundamentals/)
- [Getting Started](https://mailchimp.com/developer/open-commerce/guides/quick-start/)
- [Graph Q L  Playground](https://mailchimp.com/developer/open-commerce/playground/)
- [Plugin  Development](https://mailchimp.com/developer/open-commerce/guides/build-api-plugin/)
- [Sharing  Code  Between  Plugins](https://mailchimp.com/developer/open-commerce/docs/sharing-code-between-plugins/)
- [GitHub Organization](https://github.com/reactioncommerce)
- [Contributing](https://mailchimp.com/developer/open-commerce/docs/contribute-open-commerce/)
- [Postman Collection](collections/mailchimp-marketing-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mailchimp-marketing-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/mailchimp-transactional-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/mailchimp-transactional-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Arazzo Workflows](arazzo/) — [Arazzo Specification](https://spec.openapis.org/arazzo/latest.html)
- [LinkedIn](https://www.linkedin.com/company/intuitmailchimp)
- [Features](https://mailchimp.com/features/)
- [Use Cases](https://mailchimp.com/solutions/)
- [Integrations](https://mailchimp.com/integrations/)
- [Resources](https://mailchimp.com/developer/tools/)
- [Portal](https://mailchimp.com/developer/)
- [Changelog](https://mailchimp.com/developer/release-notes/)
- [Blog](https://mailchimp.com/developer/blog/)
- [Pricing](https://mailchimp.com/pricing/marketing/)
- [SDK](https://mailchimp.com/developer/marketing/guides/client-libraries-and-sdks/)
- [Status Page](https://status.mailchimp.com/)
- [Support](https://mailchimp.com/contact/)
- [Terms of Service](https://mailchimp.com/legal/terms/)
- [Privacy Policy](https://mailchimp.com/legal/privacy/)
- [A P I  Use  Policy](https://mailchimp.com/legal/api_use/)
- [Sign Up](https://login.mailchimp.com/signup/)
- [GitHub Organization](https://github.com/mailchimp)
- [Login](https://login.mailchimp.com/)
- [Authentication](https://mailchimp.com/developer/marketing/guides/access-user-data-oauth-2/)
- [Stack Overflow](https://stackoverflow.com/questions/tagged/mailchimp)
- [SDK](https://mailchimp.com/developer/marketing/docs/mobile-sdk/)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
