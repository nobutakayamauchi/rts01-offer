# AGENTS.md

These instructions apply to AI coding agents working in this repository.

## Repository Role

`rts01-offer` is the public static sales/legal hub for risingson offers.

It may contain:

- static sales LPs
- product catalog/index pages
- product-specific legal disclosures
- public setup/usage guides and links
- conservative product descriptions

It is not RTS core, WebAI-Bridge runtime, WebAI-Bridge-Core, or a delivery application.

## Required Reading

Before editing, read:

1. `README.md`
2. `docs/STATUS.md`
3. `docs/NEXT.md`
4. `docs/MULTI_PRODUCT_SALES_LEGAL.md` when touching product sales/legal content

## Default Mode

Prefer small, reviewable static changes.

- keep implementation and delivery authority in the product repository
- verify product capabilities against the product repository before publishing claims
- keep seller-wide legal information centralized and product terms product-specific
- preserve existing public paths unless migration is explicitly approved
- use human-readable HTML/CSS and simple data files

## Forbidden by Default

Do not, without explicit operator approval:

- add customer account flows
- add customer storage behavior
- add automatic checkout/runtime behavior
- add hidden tracking behavior
- add background jobs
- promise guaranteed outcomes
- expose secrets/private-core material
- turn this repository into product runtime or delivery authority

## Product Authority Rule

Sales/legal copy is descriptive only.

When a sales/legal claim conflicts with implementation, the implementation repository wins. Correct the sales/legal copy; do not alter runtime merely to preserve marketing text.

For WebAI-Bridge, check both:

- `nobutakayamauchi/WebAI-Bridge`
- `nobutakayamauchi/WebAI-Bridge-Core`

## Multi-product Paths

```text
/products/index.html
/products/catalog.json
/legal/index.html
/legal/products/<slug>.html
/offer/<slug>.html
```

Existing legacy paths may remain for compatibility.

## Change Scope Rule

Before editing, identify intended files, assumptions, risks, and stop conditions. After editing, report changed files, validation, remaining placeholders, and the next operator action.

## Unknown Handling

Do not invent unknown price, payment, delivery, refund, or runtime facts. Keep a development-only placeholder or stop for operator input.
