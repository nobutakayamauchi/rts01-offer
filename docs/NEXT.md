# rts01-offer Next Actions

## Immediate

1. Confirm the real Brain sales URL for WebAI-Bridge.
2. Replace the development placeholder in `legal/products/webai-bridge.html`.
3. Add the same sales URL to `products/catalog.json` and `products/index.html`.
4. Ensure the Brain sales article links to the WebAI-Bridge legal page.
5. After merge, confirm GitHub Pages serves `/products/`, `/legal/`, and `/legal/products/webai-bridge.html`.

## For Every New Product

Use `docs/MULTI_PRODUCT_SALES_LEGAL.md`.

Minimum additions:

- one catalog entry
- one product-specific legal page
- one catalog card
- one verified sales URL or explicit PRE_SALE state

## Verification

Before publishing, confirm:

- price / quantity tier
- payment method and timing
- delivery timing
- included deliverables/features
- extra API/external-service costs
- cancellation/refund boundary
- support/recovery fees
- legal contact route
- product claims against implementation repository

## Do Not Do

- do not place secrets in this repository
- do not copy private-core source into sales pages
- do not leave `example.invalid` or other placeholder purchase links on a live page
- do not use sales/legal copy as runtime authority
