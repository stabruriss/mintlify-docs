# Vibrant Wellness Portal API — Documentation

This repository hosts the developer documentation for the Vibrant Wellness Portal API. It is built with [Mintlify](https://mintlify.com).

## Structure

```
.
├── docs.json                      # Site config: navigation, theme, branding
├── index.mdx                      # Landing page
├── quickstart.mdx                 # Five-minute setup
├── authentication.mdx             # Bearer auth, scopes, rotation
├── api-keys.mdx                   # API key portal walk-through
├── concepts/                      # Domain explainers
├── guides/                        # End-to-end workflows
├── platform/                      # Cross-cutting concerns (errors, pagination, webhooks…)
├── coming-soon/                   # Reference shapes for unreleased endpoints
└── api-reference/
    ├── introduction.mdx
    ├── openapi.json               # Full OpenAPI 3.1 spec
    ├── orders/                    # Endpoint MDX bound to OpenAPI paths
    ├── tracking/
    ├── reports/
    ├── tests/
    └── webhooks/
```

## Local preview

Install the Mintlify CLI and start the dev server:

```bash
npm i -g mint
mint dev
```

View the site at `http://localhost:3000`.

## Editing endpoints

Endpoint pages under `api-reference/` are thin MDX files whose frontmatter binds to an OpenAPI operation:

```mdx
---
title: "Create an order"
openapi: "POST /v1/orders"
---
```

The full request/response shape, parameters, and try-it widget come from `api-reference/openapi.json`. To add or change an endpoint:

1. Edit `api-reference/openapi.json`.
2. Add a matching MDX stub under the appropriate folder.
3. Add the page to the relevant group in `docs.json`.

## Publishing

The Mintlify GitHub app deploys changes to the default branch automatically. See the dashboard at https://dashboard.mintlify.com.

## Status

This site is the **demo/requirements reference** version. The actual backend is in active development; treat URLs and IDs as illustrative.
