# rts01-offer Status

Status: ACTIVE / MULTI-PRODUCT SALES + LEGAL HUB / STATIC

`rts01-offer` is the public static sales/legal surface for risingson offers.

## Current Position

The original project-audit / initial-flow offer remains available, but the repository now also provides a reusable structure for additional products.

Canonical public surfaces:

- `/products/index.html` — product catalog
- `/products/catalog.json` — compact product registry
- `/legal/index.html` — seller-wide legal index
- `/legal/products/<slug>.html` — product-specific Tokushoho page
- `/offer/<slug>.html` — optional hosted sales LP

Existing legacy product paths remain valid unless explicitly migrated.

## Boundary

This repository owns public sales/legal presentation only.

It does not own product runtime, customer state, authentication, product secrets, or commercial core implementation.

For each product, runtime facts must be verified against that product's implementation repository before sales/legal copy is published.

For WebAI-Bridge:

- public/runtime authority: `nobutakayamauchi/WebAI-Bridge`
- private commercial/runtime authority: `nobutakayamauchi/WebAI-Bridge-Core`

## Current WebAI-Bridge Sales State

WebAI-Bridge has a product-specific legal page in development. Its Brain sales URL is intentionally left as a development placeholder until the real sales URL is known.

Do not publish a placeholder purchase link as if it were live.

## Allowed Changes

- static copy and layout
- adding product catalog entries
- adding product-specific legal pages
- adding external sales links after verification
- adding public guides/links
- accessibility/readability improvements

## Prohibited by Default

- product runtime
- account/customer database behavior
- secrets/private-core content
- hidden tracking
- automatic payment fulfillment
- guaranteed outcome claims
