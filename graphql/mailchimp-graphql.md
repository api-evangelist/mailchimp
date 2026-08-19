# Mailchimp GraphQL API

An open source, API-first, modular commerce stack built using Node.js, React, and GraphQL. Formerly known as Reaction Commerce, the project has been discontinued but documentation remains available.

**Endpoint:** `https://{open-commerce-host}/graphql` — templated. Open Commerce is self-hosted software; Mailchimp operates no GraphQL endpoint for it. The only base URL the documentation states is the operator's own deployment, and the quick start uses `http://localhost:3000/graphql` on a development machine. Recorded 2026-08-13, replacing a non-routable `https://api.example.com` placeholder.

**Introspection:** not performed — there is no vendor-hosted endpoint to introspect. The SDL lives in the source repositories under the `reactioncommerce` GitHub organization. No schema is fabricated here.

**Documentation:** https://mailchimp.com/developer/open-commerce/ (HTTP 200, 2026-08-13)

**GraphQL Properties:**

- GraphQL Playground: https://mailchimp.com/developer/open-commerce/playground/ — the docs page links to a local playground instance that ships with the development platform, not a hosted one.
- Source: https://github.com/reactioncommerce

**Status:** discontinued. See `lifecycle/mailchimp-lifecycle.yml` (`deprecated_products`).
