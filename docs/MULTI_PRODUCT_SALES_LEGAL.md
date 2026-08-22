# Multi-product Sales / Legal Workflow

## Decision

`rts01-offer` becomes the external static sales/legal hub for risingson offers while delivery/runtime remains in each product's own repository.

Do not move WebAI-Bridge runtime or commercial core into this repository.

## Repository boundary

- `rts01-offer`: public sales pages, product catalog, product-specific legal pages, public guides/links.
- `WebAI-Bridge`: public product/runtime surface for WebAI-Bridge.
- `WebAI-Bridge-Core`: private commercial/runtime core for WebAI-Bridge.
- other product repositories: product implementation/delivery authority.

Sales copy must describe the product; it must not become product runtime authority.

## Canonical paths

```text
/products/index.html                    # public product catalog
/products/catalog.json                  # compact product registry
/legal/index.html                       # seller-wide legal index
/legal/products/<product-slug>.html     # product-specific Tokushoho page
/offer/<product-slug>.html              # optional GitHub Pages sales LP
```

Existing paths remain valid unless explicitly migrated.

## New product procedure

When a new product is sold:

1. Add one record to `products/catalog.json`.
2. Add `/legal/products/<slug>.html` by copying the closest existing product page.
3. Add the product card to `/products/index.html`.
4. If this repository hosts the sales LP, add `/offer/<slug>.html`; otherwise set/link the external sales channel (Brain, note, etc.).
5. Link the sales page to the product-specific legal page.
6. Verify price, payment method/timing, delivery timing, refund/cancellation terms, additional charges, support boundaries, external-service costs, and contact method.
7. Never copy implementation claims from memory. Verify product capabilities against the product repository before publishing.

## Product data split

Seller-wide fields should stay stable across products:

- seller/business name
- responsible operator
- address
- phone/contact preference
- contact email

Product-specific fields must be reviewed per product:

- product name
- sales URL/channel
- price and quantity/price-tier condition
- additional costs
- payment method/timing
- delivery timing
- included features/deliverables
- support/recovery fees
- refund/cancellation rule
- operating environment
- external-service/API costs and risks
- outcome disclaimer

## WebAI-Bridge current authority

For WebAI-Bridge implementation claims, verify against `nobutakayamauchi/WebAI-Bridge` and `nobutakayamauchi/WebAI-Bridge-Core`. The sales/legal repository is not authoritative for runtime behavior.

## Stop conditions

Do not publish a new product legal page if any of these are unknown:

- actual selling price or price rule
- payment channel
- when delivery starts
- what exactly is delivered
- cancellation/refund boundary
- sales URL or a deliberate `PRE_SALE` placeholder state

A placeholder is acceptable on a development branch, but not as a live purchase link.
