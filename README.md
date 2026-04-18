# Mailchimp (mailchimp)

Mailchimp is an Intuit company providing a marketing automation platform and email marketing service for managing mailing lists, creating email marketing campaigns, and automating marketing workflows.

**URL:** [Visit APIs.json URL](https://raw.githubusercontent.com/api-evangelist/mailchimp/refs/heads/main/apis.yml)

## Tags:

 - Campaigns, Email Marketing, Marketing Automation, Newsletters, Transactional Email

## Timestamps

- **Created:** 2023-11-23
- **Modified:** 2026-04-18

## APIs

### Mailchimp Marketing API
The Mailchimp Marketing API provides programmatic access to Mailchimp data and functionality, allowing developers to build custom features to sync email activity and campaign analytics with their database, manage audiences and campaigns, and more.

**Human URL:** [https://mailchimp.com/developer/marketing/](https://mailchimp.com/developer/marketing/)

#### Tags:

 - Audiences, Automation, Campaigns, Email Marketing

#### Properties

- [Documentation](https://mailchimp.com/developer/marketing/docs/fundamentals/)
- [OpenAPI](openapi/mailchimp-marketing-api-openapi.yml)
- [Integrations](https://mailchimp.com/developer/marketing/docs/integrations/)
- [Errors](https://mailchimp.com/developer/marketing/docs/errors/)
- [APIReference](https://mailchimp.com/developer/marketing/api/)
- [GettingStarted](https://mailchimp.com/developer/marketing/guides/quick-start/)
- [Authentication](https://mailchimp.com/developer/marketing/guides/access-user-data-oauth-2/)

### Mailchimp Transactional API
Mailchimp Transactional (formerly Mandrill) is a powerful email delivery service that lets you send personalized, one-to-one emails like password resets, order confirmations, and welcome messages.

**Human URL:** [https://mailchimp.com/developer/transactional/](https://mailchimp.com/developer/transactional/)

#### Tags:

 - Email Delivery, Messaging, Transactional Email

#### Properties

- [Documentation](https://mailchimp.com/developer/transactional/docs/fundamentals/)
- [OpenAPI](openapi/mailchimp-transactional-api-openapi.yml)
- [GettingStarted](https://mailchimp.com/developer/transactional/guides/quick-start/)
- [Authentication](https://mailchimp.com/developer/transactional/docs/authentication-delivery/)
- [APIReference](https://mailchimp.com/developer/transactional/api/)

### Mailchimp Open Commerce
An open source, API-first, modular commerce stack built using Node.js, React, and GraphQL. Formerly known as Reaction Commerce, the project has been discontinued but documentation remains available.

**Human URL:** [https://mailchimp.com/developer/open-commerce/](https://mailchimp.com/developer/open-commerce/)

#### Tags:

 - E-Commerce, GraphQL, Headless Commerce

#### Properties

- [Documentation](https://mailchimp.com/developer/open-commerce/docs/fundamentals/)
- [GettingStarted](https://mailchimp.com/developer/open-commerce/guides/quick-start/)
- [GitHubOrganization](https://github.com/reactioncommerce)

## Common Properties

- [Features](https://mailchimp.com/features/)
- [UseCases](https://mailchimp.com/solutions/)
- [Integrations](https://mailchimp.com/integrations/)
- [Portal](https://mailchimp.com/developer/)
- [ChangeLog](https://mailchimp.com/developer/release-notes/)
- [Blog](https://mailchimp.com/developer/blog/)
- [Pricing](https://mailchimp.com/pricing/marketing/)
- [SDK](https://mailchimp.com/developer/marketing/guides/client-libraries-and-sdks/)
- [StatusPage](https://status.mailchimp.com/)
- [Support](https://mailchimp.com/contact/)
- [TermsOfService](https://mailchimp.com/legal/terms/)
- [PrivacyPolicy](https://mailchimp.com/legal/privacy/)
- [SignUp](https://login.mailchimp.com/signup/)
- [GitHubOrganization](https://github.com/mailchimp)
- [Login](https://login.mailchimp.com/)
- [Authentication](https://mailchimp.com/developer/marketing/guides/access-user-data-oauth-2/)
- [StackOverflow](https://stackoverflow.com/questions/tagged/mailchimp)
- [SDK - Mobile](https://mailchimp.com/developer/marketing/docs/mobile-sdk/)

## OpenAPI

- [Marketing API OpenAPI](openapi/mailchimp-marketing-api-openapi.yml)
- [Transactional API OpenAPI](openapi/mailchimp-transactional-api-openapi.yml)

## JSON Schema

| Schema | File |
|---|---|
| Campaign Schema | [json-schema/campaign.json](json-schema/campaign.json) |
| Audience Schema | [json-schema/audience.json](json-schema/audience.json) |
| Member Schema | [json-schema/member.json](json-schema/member.json) |
| Template Schema | [json-schema/template.json](json-schema/template.json) |
| Transactional Send Result Schema | [json-schema/mailchimp-transactional-send-result-schema.json](json-schema/mailchimp-transactional-send-result-schema.json) |
| Transactional Message Info Schema | [json-schema/mailchimp-transactional-message-info-schema.json](json-schema/mailchimp-transactional-message-info-schema.json) |
| Transactional Template Info Schema | [json-schema/mailchimp-transactional-template-info-schema.json](json-schema/mailchimp-transactional-template-info-schema.json) |

## JSON-LD

- [Mailchimp Context](json-ld/context.jsonld)
- [Transactional Context](json-ld/mailchimp-transactional-context.jsonld)

## Vocabulary

- [Mailchimp Vocabulary](vocabulary/mailchimp-vocabulary.yaml)

## Rules

- [Spectral Rules](rules/mailchimp-spectral-rules.yml)

## Capabilities

| Capability | Type | File |
|---|---|---|
| Email Marketing | Workflow | [capabilities/email-marketing.yaml](capabilities/email-marketing.yaml) |
| Marketing | Shared | [capabilities/shared/marketing.yaml](capabilities/shared/marketing.yaml) |
| Transactional | Shared | [capabilities/shared/transactional.yaml](capabilities/shared/transactional.yaml) |

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
