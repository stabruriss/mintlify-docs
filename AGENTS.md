# Documentation project instructions

## About this project

- Mintlify-powered docs for the **Vibrant Wellness Portal API**.
- Pages are MDX files with YAML frontmatter; site config is `docs.json`.
- Endpoint reference is OpenAPI-driven: `api-reference/openapi.json` is the source of truth; MDX files under `api-reference/**` are thin frontmatter stubs that bind to OpenAPI paths.
- Run `mint dev` to preview locally, `mint broken-links` to validate.

## Terminology

- "Order" — a lab requisition for one or more panels for one patient.
- "Test" / "panel" — a single test code in the catalog (e.g. `GUT-ZOOMER-3.0`).
- "Report" — the finalized result of running one panel; one order can produce many reports.
- "Provider" — the ordering clinician. Not the same as a payment provider.
- "Patient" — the person whose sample is collected.
- Use "API key", not "token", for the bearer credential. Reserve "token" for OAuth (none yet).
- Use "sandbox" / "production", not "test" / "live", when referring to environments.

## Style preferences

- Use active voice and second person ("you").
- Sentence case for headings.
- Bold for UI elements: Click **Settings → API keys**.
- Code formatting for `field_names`, `endpoints`, file names, and example IDs.
- Prefer concrete examples (`ord_01HZ7M3K2N8R9Q`) over placeholders (`<order_id>`) in narrative; placeholders are fine inside `curl` snippets.
- For coming-soon endpoints, lead with a `<Note>` callout that the shape may change.

## Content boundaries

- Do **not** document internal lab operations, accessioning workflows, or admin-only endpoints.
- Do **not** publish real provider, patient, or order data. Use the illustrative IDs already in this repo.
- Do **not** link to internal Notion or Jira; only link to public surfaces.
- "Coming soon" pages must include the warning banner and avoid implying a launch date.
