# Mailchimp

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

Mailchimp is an Intuit company providing a marketing automation platform and email marketing service for managing mailing lists, creating email marketing campaigns, and automating marketing workflows. It exposes two distinct developer surfaces: the Marketing API (v3, REST, 298 operations at https://<dc>.api.mailchimp.com/3.0) covering audiences, members, tags, segments, campaigns, content, automations, customer journeys, reports, e-commerce stores and orders, file manager, templates, landing pages, batch operations and webhooks; and Mailchimp Transactional, formerly Mandrill (99 RPC-style POST methods at https://mandrillapp.com/api/1.0), for one-to-one transactional email and SMS, inbound processing, dedicated IP management and subaccounts. Authentication is an API key or OAuth 2 for the Marketing API and a body-parameter API key for Transactional. Mailchimp runs a hosted MCP server for the Transactional API, publishes eight official client libraries and two mobile SDKs, and delivers audience events as HMAC-signed webhooks.

**Areas:** Campaigns · Email Marketing · Marketing Automation · Newsletters · Transactional Email · Audience Management · SMS · E-Commerce · Webhook · Marketing Analytics · Email

## Mailchimp on APIs.io

Everything profiled for Mailchimp is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/mailchimp/](https://apis.io/providers/mailchimp/)** — or go straight to one of the APIs or properties below.

### APIs (45)

- [Mailchimp Open Commerce](https://apis.io/apis/mailchimp/mailchimp-open-commerce/) — An open source, API-first, modular commerce stack built using Node.js, React, and GraphQL. Formerly known as Reaction Commerce, the project has been…
- [Mailchimp Automations API](https://apis.io/apis/mailchimp/mailchimp-automations-api/) — The Automations API from Mailchimp — 13 operation(s) for automations.
- [Mailchimp Batches API](https://apis.io/apis/mailchimp/mailchimp-batches-api/) — The Batches API from Mailchimp — 2 operation(s) for batches.
- [Mailchimp Campaigns API](https://apis.io/apis/mailchimp/mailchimp-campaigns-api/) — The Campaigns API from Mailchimp — 18 operation(s) for campaigns.
- [Mailchimp Conversations API](https://apis.io/apis/mailchimp/mailchimp-conversations-api/) — The Conversations API from Mailchimp — 4 operation(s) for conversations.
- [Mailchimp Ecommerce API](https://apis.io/apis/mailchimp/mailchimp-ecommerce-api/) — The Ecommerce API from Mailchimp — 10 operation(s) for ecommerce.
- [Mailchimp Exports API](https://apis.io/apis/mailchimp/mailchimp-exports-api/) — The Exports API from Mailchimp — 7 operation(s) for exports.
- [Mailchimp Lists API](https://apis.io/apis/mailchimp/mailchimp-lists-api/) — The Lists API from Mailchimp — 11 operation(s) for lists.
- [Mailchimp Messages API](https://apis.io/apis/mailchimp/mailchimp-messages-api/) — The Messages API from Mailchimp — 13 operation(s) for messages.
- [Mailchimp Metadata API](https://apis.io/apis/mailchimp/mailchimp-metadata-api/) — Manage custom metadata fields that can be attached to messages for tracking and filtering.
- [Mailchimp Rejects API](https://apis.io/apis/mailchimp/mailchimp-rejects-api/) — Manage the rejection blacklist, which prevents delivery to addresses that have previously bounced or been reported as spam.
- [Mailchimp Reporting API](https://apis.io/apis/mailchimp/mailchimp-reporting-api/) — The Reporting API from Mailchimp — 12 operation(s) for reporting.
- [Mailchimp Reports API](https://apis.io/apis/mailchimp/mailchimp-reports-api/) — The Reports API from Mailchimp — 24 operation(s) for reports.
- [Mailchimp Root API](https://apis.io/apis/mailchimp/mailchimp-root-api/) — The Root API from Mailchimp — 1 operation(s) for root.
- [Mailchimp Senders API](https://apis.io/apis/mailchimp/mailchimp-senders-api/) — Retrieve sender information and statistics for verified sending domains and email addresses.
- [Mailchimp Subaccounts API](https://apis.io/apis/mailchimp/mailchimp-subaccounts-api/) — Manage subaccounts for organizing sending and reporting within a single Mandrill account.
- [Mailchimp Surveys API](https://apis.io/apis/mailchimp/mailchimp-surveys-api/) — The Surveys API from Mailchimp — 12 operation(s) for surveys.
- [Mailchimp Tags API](https://apis.io/apis/mailchimp/mailchimp-tags-api/) — The Tags API from Mailchimp — 5 operation(s) for tags.
- [Mailchimp Templates API](https://apis.io/apis/mailchimp/mailchimp-templates-api/) — The Templates API from Mailchimp — 11 operation(s) for templates.
- [Mailchimp Users API](https://apis.io/apis/mailchimp/mailchimp-users-api/) — Retrieve information about the authenticated Mandrill account.
- [Mailchimp Webhooks API](https://apis.io/apis/mailchimp/mailchimp-webhooks-api/) — The Webhooks API from Mailchimp — 9 operation(s) for webhooks.
- [Mailchimp Account Export API](https://apis.io/apis/mailchimp/mailchimp-accountexport-api/) — The accountExport API from Mailchimp — 1 operation(s) for accountexport.
- [Mailchimp Audiences API](https://apis.io/apis/mailchimp/mailchimp-audiences-api/) — The audiences API from Mailchimp — 2 operation(s) for audiences.
- [Mailchimp Authorized Apps API](https://apis.io/apis/mailchimp/mailchimp-authorizedapps-api/) — The authorizedApps API from Mailchimp — 2 operation(s) for authorizedapps.
- [Mailchimp Batch Webhooks API](https://apis.io/apis/mailchimp/mailchimp-batchwebhooks-api/) — The batchWebhooks API from Mailchimp — 2 operation(s) for batchwebhooks.
- [Mailchimp Campaign Folders API](https://apis.io/apis/mailchimp/mailchimp-campaignfolders-api/) — The campaignFolders API from Mailchimp — 2 operation(s) for campaignfolders.
- [Mailchimp Connected Sites API](https://apis.io/apis/mailchimp/mailchimp-connectedsites-api/) — The connectedSites API from Mailchimp — 5 operation(s) for connectedsites.
- [Mailchimp Contacts API](https://apis.io/apis/mailchimp/mailchimp-contacts-api/) — The contacts API from Mailchimp — 6 operation(s) for contacts.
- [Mailchimp Inbound API](https://apis.io/apis/mailchimp/mailchimp-inbound-api/) — The inbound API from Mailchimp — 9 operation(s) for inbound.
- [Mailchimp Mctemplates API](https://apis.io/apis/mailchimp/mailchimp-mctemplates-api/) — The mctemplates API from Mailchimp — 4 operation(s) for mctemplates.
- [Mailchimp Ping API](https://apis.io/apis/mailchimp/mailchimp-ping-api/) — The ping API from Mailchimp — 1 operation(s) for ping.
- [Mailchimp Search Campaigns API](https://apis.io/apis/mailchimp/mailchimp-searchcampaigns-api/) — The searchCampaigns API from Mailchimp — 1 operation(s) for searchcampaigns.
- [Mailchimp Search Members API](https://apis.io/apis/mailchimp/mailchimp-searchmembers-api/) — The searchMembers API from Mailchimp — 1 operation(s) for searchmembers.
- [Mailchimp Sms Campaigns API](https://apis.io/apis/mailchimp/mailchimp-sms-campaigns-api/) — The sms-campaigns API from Mailchimp — 6 operation(s) for sms-campaigns.
- [Mailchimp URLS API](https://apis.io/apis/mailchimp/mailchimp-urls-api/) — The urls API from Mailchimp — 4 operation(s) for urls.
- [Mailchimp Verified Domains API](https://apis.io/apis/mailchimp/mailchimp-verifieddomains-api/) — The verifiedDomains API from Mailchimp — 3 operation(s) for verifieddomains.
- [Mailchimp Ips API](https://apis.io/apis/mailchimp/mailchimp-ips-api/) — The ips API from Mailchimp — 13 operation(s) for ips.
- [Mailchimp Account Exports API](https://apis.io/apis/mailchimp/mailchimp-account-exports-api/) — The Account Exports API from Mailchimp — 1 operation(s) for account exports.
- [Mailchimp Activity Feed API](https://apis.io/apis/mailchimp/mailchimp-activity-feed-api/) — The Activity Feed API from Mailchimp — 1 operation(s) for activity feed.
- [Mailchimp Allow Lists API](https://apis.io/apis/mailchimp/mailchimp-allow-lists-api/) — The Allow Lists API from Mailchimp — 3 operation(s) for allow lists.
- [Mailchimp customer Journeys API](https://apis.io/apis/mailchimp/mailchimp-customer-journeys-api/) — The customer Journeys API from Mailchimp — 1 operation(s) for customer journeys.
- [Mailchimp facebook Ads API](https://apis.io/apis/mailchimp/mailchimp-facebook-ads-api/) — The facebook Ads API from Mailchimp — 2 operation(s) for facebook ads.
- [Mailchimp File Manager API](https://apis.io/apis/mailchimp/mailchimp-file-manager-api/) — The File Manager API from Mailchimp — 5 operation(s) for file manager.
- [Mailchimp Landing Pages API](https://apis.io/apis/mailchimp/mailchimp-landing-pages-api/) — The Landing Pages API from Mailchimp — 5 operation(s) for landing pages.
- [Mailchimp Template Folders API](https://apis.io/apis/mailchimp/mailchimp-template-folders-api/) — The Template Folders API from Mailchimp — 2 operation(s) for template folders.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Arazzo workflows (19)

Multi-step workflows that chain operations into a business task.

- [Mailchimp Add Member and Attach a Note](https://apis.io/arazzos/mailchimp/mailchimp-add-member-note-workflow/)
- [Mailchimp Add Member and Tag](https://apis.io/arazzos/mailchimp/mailchimp-add-member-tag-workflow/)
- [Mailchimp Pre-Send Checklist then Send Campaign](https://apis.io/arazzos/mailchimp/mailchimp-checklist-then-send-campaign-workflow/)
- [Mailchimp Create Audience and Add First Member](https://apis.io/arazzos/mailchimp/mailchimp-create-audience-add-member-workflow/)
- [Mailchimp Create Campaign, Set Content, and Send Test](https://apis.io/arazzos/mailchimp/mailchimp-create-campaign-content-test-workflow/)
- [Mailchimp Create Campaign, Set Content, and Schedule](https://apis.io/arazzos/mailchimp/mailchimp-create-campaign-set-content-schedule-workflow/)
- [Mailchimp Create Campaign, Set Content, and Send](https://apis.io/arazzos/mailchimp/mailchimp-create-campaign-set-content-send-workflow/)
- [Mailchimp Create Merge Field and Add Member](https://apis.io/arazzos/mailchimp/mailchimp-create-merge-field-add-member-workflow/)
- [Mailchimp Create Static Segment and Add Members](https://apis.io/arazzos/mailchimp/mailchimp-create-static-segment-add-members-workflow/)
- [Mailchimp Create Template, Build Campaign, and Send](https://apis.io/arazzos/mailchimp/mailchimp-create-template-campaign-send-workflow/)
- [Mailchimp Find and Pause an Automation](https://apis.io/arazzos/mailchimp/mailchimp-find-and-pause-automation-workflow/)
- [Mailchimp Find and Start an Automation](https://apis.io/arazzos/mailchimp/mailchimp-find-and-start-automation-workflow/)
- [Mailchimp Find Campaign and Pull Its Report](https://apis.io/arazzos/mailchimp/mailchimp-find-campaign-pull-report-workflow/)
- [Mailchimp Find Member, Mark VIP, and Tag](https://apis.io/arazzos/mailchimp/mailchimp-find-member-mark-vip-tag-workflow/)
- [Mailchimp Onboard Member into a Static Segment](https://apis.io/arazzos/mailchimp/mailchimp-onboard-member-to-segment-workflow/)
- [Mailchimp Add-or-Update Member and Tag](https://apis.io/arazzos/mailchimp/mailchimp-put-member-tag-workflow/)
- [Mailchimp Replicate Campaign and Send Test](https://apis.io/arazzos/mailchimp/mailchimp-replicate-campaign-test-workflow/)
- [Mailchimp Sync Static Segment Members](https://apis.io/arazzos/mailchimp/mailchimp-sync-static-segment-members-workflow/)
- [Mailchimp Upsert Audience Member](https://apis.io/arazzos/mailchimp/mailchimp-upsert-member-workflow/)

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Mailchimp Marketing Webhooks](https://apis.io/asyncapis/mailchimp/mailchimp-marketing-webhooks-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/](https://apis.io/channels/mailchimp/untitled/)

#### GraphQL (1)

GraphQL schemas.

- [Mailchimp GraphQL API](https://apis.io/graphqls/mailchimp/mailchimp-graphql/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [mailchimp-mcp.yml](https://apis.io/servers/mailchimp/mailchimp-mcp-yml/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Mailchimp Agentic Access](https://apis.io/agentic-access/mailchimp/mailchimp-agentic-access/)

#### JSON Schema (50)

The data models the API reads and writes.

- [Mailchimp Audience (List)](https://apis.io/schemas/mailchimp/audience/)
- [Mailchimp Campaign](https://apis.io/schemas/mailchimp/campaign/)
- [AccountStats](https://apis.io/schemas/mailchimp/mailchimp-accountstats/)
- [AllowlistEntry](https://apis.io/schemas/mailchimp/mailchimp-allowlistentry/)
- [DedicatedIP](https://apis.io/schemas/mailchimp/mailchimp-dedicatedip/)
- [Error](https://apis.io/schemas/mailchimp/mailchimp-error/)
- [ExportJob](https://apis.io/schemas/mailchimp/mailchimp-exportjob/)
- [IPPool](https://apis.io/schemas/mailchimp/mailchimp-ippool/)
- [MessageContent](https://apis.io/schemas/mailchimp/mailchimp-messagecontent/)
- [MessageDetail](https://apis.io/schemas/mailchimp/mailchimp-messagedetail/)
- [MessageInfo](https://apis.io/schemas/mailchimp/mailchimp-messageinfo/)
- [MessagePayload](https://apis.io/schemas/mailchimp/mailchimp-messagepayload/)
- [MetadataField](https://apis.io/schemas/mailchimp/mailchimp-metadatafield/)
- [ParsedMessage](https://apis.io/schemas/mailchimp/mailchimp-parsedmessage/)
- [RejectEntry](https://apis.io/schemas/mailchimp/mailchimp-rejectentry/)
- [ScheduledMessage](https://apis.io/schemas/mailchimp/mailchimp-scheduledmessage/)
- [SenderDomain](https://apis.io/schemas/mailchimp/mailchimp-senderdomain/)
- [SenderInfo](https://apis.io/schemas/mailchimp/mailchimp-senderinfo/)
- [SendResult](https://apis.io/schemas/mailchimp/mailchimp-sendresult/)
- [SubaccountInfo](https://apis.io/schemas/mailchimp/mailchimp-subaccountinfo/)
- [TagInfo](https://apis.io/schemas/mailchimp/mailchimp-taginfo/)
- [TemplateInfo](https://apis.io/schemas/mailchimp/mailchimp-templateinfo/)
- [TimeSeries](https://apis.io/schemas/mailchimp/mailchimp-timeseries/)
- [AccountStats](https://apis.io/schemas/mailchimp/mailchimp-transactional-account-stats/)
- [AllowlistEntry](https://apis.io/schemas/mailchimp/mailchimp-transactional-allowlist-entry/)
- …and 25 more published on APIs.io

#### JSON Structure (24)

Data models expressed in JSON Structure.

- [Mailchimp Structure](https://apis.io/json-structure/mailchimp/mailchimp-structure/)
- [Mailchimp Transactional Account Stats Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-account-stats-structure/)
- [Mailchimp Transactional Allowlist Entry Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-allowlist-entry-structure/)
- [Mailchimp Transactional Dedicated Ip Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-dedicated-ip-structure/)
- [Mailchimp Transactional Error Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-error-structure/)
- [Mailchimp Transactional Export Job Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-export-job-structure/)
- [Mailchimp Transactional Ip Pool Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-ip-pool-structure/)
- [Mailchimp Transactional Message Content Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-message-content-structure/)
- [Mailchimp Transactional Message Detail Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-message-detail-structure/)
- [Mailchimp Transactional Message Info Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-message-info-structure/)
- [Mailchimp Transactional Message Payload Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-message-payload-structure/)
- [Mailchimp Transactional Metadata Field Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-metadata-field-structure/)
- [Mailchimp Transactional Parsed Message Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-parsed-message-structure/)
- [Mailchimp Transactional Reject Entry Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-reject-entry-structure/)
- [Mailchimp Transactional Scheduled Message Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-scheduled-message-structure/)
- [Mailchimp Transactional Send Result Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-send-result-structure/)
- [Mailchimp Transactional Sender Domain Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-sender-domain-structure/)
- [Mailchimp Transactional Sender Info Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-sender-info-structure/)
- [Mailchimp Transactional Subaccount Info Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-subaccount-info-structure/)
- [Mailchimp Transactional Tag Info Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-tag-info-structure/)
- [Mailchimp Transactional Template Info Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-template-info-structure/)
- [Mailchimp Transactional Time Series Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-time-series-structure/)
- [Mailchimp Transactional User Info Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-user-info-structure/)
- [Mailchimp Transactional Webhook Info Structure](https://apis.io/json-structure/mailchimp/mailchimp-transactional-webhook-info-structure/)

#### JSON-LD (2)

Linked-data contexts for the provider's vocabulary.

- [context Context](https://apis.io/jsonld/mailchimp/context/)
- [Mailchimp Transactional Context](https://apis.io/jsonld/mailchimp/mailchimp-transactional-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Mailchimp Domain Vocabulary](https://apis.io/vocabularies/mailchimp/mailchimp-vocabulary/)

#### Examples (89)

Example requests and responses.

- [Mailchimp Postallowlistsadd Example](https://apis.io/examples/mailchimp/mailchimp-postallowlistsadd-example/)
- [Mailchimp Postallowlistsdelete Example](https://apis.io/examples/mailchimp/mailchimp-postallowlistsdelete-example/)
- [Mailchimp Postallowlistslist Example](https://apis.io/examples/mailchimp/mailchimp-postallowlistslist-example/)
- [Mailchimp Postexportsactivity Example](https://apis.io/examples/mailchimp/mailchimp-postexportsactivity-example/)
- [Mailchimp Postexportsallowlist Example](https://apis.io/examples/mailchimp/mailchimp-postexportsallowlist-example/)
- [Mailchimp Postexportsinfo Example](https://apis.io/examples/mailchimp/mailchimp-postexportsinfo-example/)
- [Mailchimp Postexportslist Example](https://apis.io/examples/mailchimp/mailchimp-postexportslist-example/)
- [Mailchimp Postexportsrejects Example](https://apis.io/examples/mailchimp/mailchimp-postexportsrejects-example/)
- [Mailchimp Postipscreatepool Example](https://apis.io/examples/mailchimp/mailchimp-postipscreatepool-example/)
- [Mailchimp Postipsdeletepool Example](https://apis.io/examples/mailchimp/mailchimp-postipsdeletepool-example/)
- [Mailchimp Postipsinfo Example](https://apis.io/examples/mailchimp/mailchimp-postipsinfo-example/)
- [Mailchimp Postipslist Example](https://apis.io/examples/mailchimp/mailchimp-postipslist-example/)
- [Mailchimp Postipslistpools Example](https://apis.io/examples/mailchimp/mailchimp-postipslistpools-example/)
- [Mailchimp Postmessagescancelscheduled Example](https://apis.io/examples/mailchimp/mailchimp-postmessagescancelscheduled-example/)
- [Mailchimp Postmessagescontent Example](https://apis.io/examples/mailchimp/mailchimp-postmessagescontent-example/)
- [Mailchimp Postmessagesinfo Example](https://apis.io/examples/mailchimp/mailchimp-postmessagesinfo-example/)
- [Mailchimp Postmessageslistscheduled Example](https://apis.io/examples/mailchimp/mailchimp-postmessageslistscheduled-example/)
- [Mailchimp Postmessagesparse Example](https://apis.io/examples/mailchimp/mailchimp-postmessagesparse-example/)
- [Mailchimp Postmessagesreschedule Example](https://apis.io/examples/mailchimp/mailchimp-postmessagesreschedule-example/)
- [Mailchimp Postmessagessearch Example](https://apis.io/examples/mailchimp/mailchimp-postmessagessearch-example/)
- [Mailchimp Postmessagessearchtimeseries Example](https://apis.io/examples/mailchimp/mailchimp-postmessagessearchtimeseries-example/)
- [Mailchimp Postmessagessend Example](https://apis.io/examples/mailchimp/mailchimp-postmessagessend-example/)
- [Mailchimp Postmessagessendraw Example](https://apis.io/examples/mailchimp/mailchimp-postmessagessendraw-example/)
- [Mailchimp Postmessagessendtemplate Example](https://apis.io/examples/mailchimp/mailchimp-postmessagessendtemplate-example/)
- [Mailchimp Postmetadataadd Example](https://apis.io/examples/mailchimp/mailchimp-postmetadataadd-example/)
- …and 64 more published on APIs.io

#### Collections (126)

Postman and Open Collection request collections.

- [Mailchimp Marketing Abuse API](https://apis.io/collections/mailchimp/open-mailchimp-abuse-api/)
- [Mailchimp Marketing Abuse Account Export API](https://apis.io/collections/mailchimp/open-mailchimp-account-export-api/)
- [Mailchimp Marketing Abuse Accounts API](https://apis.io/collections/mailchimp/open-mailchimp-accounts-api/)
- [Mailchimp Marketing Abuse Actions API](https://apis.io/collections/mailchimp/open-mailchimp-actions-api/)
- [Mailchimp Marketing Abuse Activity API](https://apis.io/collections/mailchimp/open-mailchimp-activity-api/)
- [Mailchimp Marketing Abuse Advice API](https://apis.io/collections/mailchimp/open-mailchimp-advice-api/)
- [Mailchimp Marketing Abuse Allowlists API](https://apis.io/collections/mailchimp/open-mailchimp-allowlists-api/)
- [Mailchimp Marketing Abuse Answers API](https://apis.io/collections/mailchimp/open-mailchimp-answers-api/)
- [Mailchimp Marketing Abuse Applications API](https://apis.io/collections/mailchimp/open-mailchimp-applications-api/)
- [Mailchimp Marketing Abuse Archive API](https://apis.io/collections/mailchimp/open-mailchimp-archive-api/)
- [Mailchimp Marketing Abuse Authorized API](https://apis.io/collections/mailchimp/open-mailchimp-authorized-api/)
- [Mailchimp Marketing Abuse Authorized Apps API](https://apis.io/collections/mailchimp/open-mailchimp-authorized-apps-api/)
- [Mailchimp Marketing Abuse Automations API](https://apis.io/collections/mailchimp/open-mailchimp-automations-api/)
- [Mailchimp Marketing Abuse Batch API](https://apis.io/collections/mailchimp/open-mailchimp-batch-api/)
- [Mailchimp Marketing Abuse Batch Webhooks API](https://apis.io/collections/mailchimp/open-mailchimp-batch-webhooks-api/)
- [Mailchimp Marketing Abuse Batches API](https://apis.io/collections/mailchimp/open-mailchimp-batches-api/)
- [Mailchimp Marketing Abuse Campaign Folders API](https://apis.io/collections/mailchimp/open-mailchimp-campaign-folders-api/)
- [Mailchimp Marketing Abuse Campaigns API](https://apis.io/collections/mailchimp/open-mailchimp-campaigns-api/)
- [Mailchimp Marketing Abuse Cancels API](https://apis.io/collections/mailchimp/open-mailchimp-cancels-api/)
- [Mailchimp Marketing Abuse Carts API](https://apis.io/collections/mailchimp/open-mailchimp-carts-api/)
- [Mailchimp Marketing Abuse Categories API](https://apis.io/collections/mailchimp/open-mailchimp-categories-api/)
- [Mailchimp Marketing Abuse Chatter API](https://apis.io/collections/mailchimp/open-mailchimp-chatter-api/)
- [Mailchimp Marketing Abuse Checklist API](https://apis.io/collections/mailchimp/open-mailchimp-checklist-api/)
- [Mailchimp Marketing Abuse Click API](https://apis.io/collections/mailchimp/open-mailchimp-click-api/)
- [Mailchimp Marketing Abuse Clients API](https://apis.io/collections/mailchimp/open-mailchimp-clients-api/)
- …and 101 more published on APIs.io

#### Overlays (46)

OpenAPI overlays, including conversational phrasing for each operation.

- [Mailchimp Account Exports Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-account-exports-api-phrasing-overlay/)
- [Mailchimp Accountexport Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-accountexport-api-phrasing-overlay/)
- [Mailchimp Activity Feed Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-activity-feed-api-phrasing-overlay/)
- [Mailchimp Allow Lists Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-allow-lists-api-phrasing-overlay/)
- [Mailchimp Audiences Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-audiences-api-phrasing-overlay/)
- [Mailchimp Authorizedapps Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-authorizedapps-api-phrasing-overlay/)
- [Mailchimp Automations Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-automations-api-phrasing-overlay/)
- [Mailchimp Batches Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-batches-api-phrasing-overlay/)
- [Mailchimp Batchwebhooks Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-batchwebhooks-api-phrasing-overlay/)
- [Mailchimp Campaignfolders Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-campaignfolders-api-phrasing-overlay/)
- [Mailchimp Campaigns Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-campaigns-api-phrasing-overlay/)
- [Mailchimp Connectedsites Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-connectedsites-api-phrasing-overlay/)
- [Mailchimp Contacts Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-contacts-api-phrasing-overlay/)
- [Mailchimp Conversations Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-conversations-api-phrasing-overlay/)
- [Mailchimp Customer Journeys Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-customer-journeys-api-phrasing-overlay/)
- [Mailchimp Ecommerce Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-ecommerce-api-phrasing-overlay/)
- [Mailchimp Exports Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-exports-api-phrasing-overlay/)
- [Mailchimp Facebook Ads Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-facebook-ads-api-phrasing-overlay/)
- [Mailchimp File Manager Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-file-manager-api-phrasing-overlay/)
- [Mailchimp Inbound Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-inbound-api-phrasing-overlay/)
- [Mailchimp Ips Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-ips-api-phrasing-overlay/)
- [Mailchimp Landing Pages Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-landing-pages-api-phrasing-overlay/)
- [Mailchimp Lists Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-lists-api-phrasing-overlay/)
- [Mailchimp Marketing Api Overlay](https://apis.io/overlays/mailchimp/mailchimp-marketing-api-overlay/)
- [Mailchimp Mctemplates Api Phrasing Overlay](https://apis.io/overlays/mailchimp/mailchimp-mctemplates-api-phrasing-overlay/)
- …and 21 more published on APIs.io

#### Governance rules (3)

Spectral rulesets for the provider's contracts.

- [Mailchimp — jsonschema rules](https://apis.io/rules/mailchimp/mailchimp-jsonschema-spectral-rules/)
- [Mailchimp API Rules](https://apis.io/rules/mailchimp/mailchimp-rules/)
- [Mailchimp API Rules](https://apis.io/rules/mailchimp/mailchimp-spectral-rules/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Mailchimp Authentication](https://apis.io/security/mailchimp/mailchimp-authentication/)
- [Mailchimp Domain Security](https://apis.io/security/mailchimp/mailchimp-domain-security/)
- [Mailchimp Trust Center](https://apis.io/security/mailchimp/mailchimp-trust-center/)
- [Mailchimp Vulnerability Disclosure](https://apis.io/security/mailchimp/mailchimp-vulnerability-disclosure/)

#### Plans and pricing (2)

Published plans, tiers and prices.

- [Mailchimp Plans Pricing](https://apis.io/plans/mailchimp/mailchimp-plans-pricing/)
- [Mailchimp Price Estimates](https://apis.io/plans/mailchimp/mailchimp-price-estimates/)

#### Rate limits (1)

Published request limits.

- [Mailchimp Rate Limits](https://apis.io/rate-limits/mailchimp/mailchimp-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Mailchimp Finops](https://apis.io/finops/mailchimp/mailchimp-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.mailchimp.com/)
- [Documentation](https://mailchimp.com/developer/marketing/docs/fundamentals/)
- [Getting started](https://mailchimp.com/developer/marketing/guides/quick-start/)
- [API reference](https://mailchimp.com/developer/marketing/api/)
- [Pricing](https://mailchimp.com/pricing/marketing/)
- [Support](https://mailchimp.com/contact/)
- [Changelog](https://mailchimp.com/developer/release-notes/)
- [Blog](https://mailchimp.com/developer/blog/)
- [Security](https://mailchimp.com/about/security/#Responsible_Disclosure)
- [Compliance](https://mailchimp.com/about/security/)
- [Terms of service](https://mailchimp.com/legal/terms/)
- [Privacy policy](https://mailchimp.com/legal/privacy/)
- [GitHub](https://github.com/mailchimp)
- [Status](https://status.mailchimp.com/)

## API Evangelist rating

**Kin Score 76.7** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 81.7 |
| Contract quality | 63.4 |
| Contract governance | 18.2 |
| Operational transparency | 94.7 |
| Developer ergonomics | 83.9 |
| Access clarity | 92.1 |

**Agent readiness 41.3** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | verified |
| MCP Server | verified |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly |

**Regulatory alignment 30.0** — Telecommunications

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/mailchimp/](https://apis.io/providers/mailchimp/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Mailchimp: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/mailchimp/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
