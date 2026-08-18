# Placeholder Policy

Use placeholder mode whenever final customer copy, product data, or imagery is incomplete.

## Allowed

- Neutral temporary product names and descriptions.
- Client-presentable generated, licensed, rendered, illustrated, diagrammatic, or deliberately graphic temporary treatments that perform the intended visual communication job.
- Licensed stock, generated images, or temporary internal references.
- Representative products selected for layout testing.
- AI-drafted copy whose unapproved status is recorded in the manifest, not rendered beside the copy.
- Presentation-only sample commerce values and states required to judge a purchase layout, including price hierarchy, compare-at/discount state, option selections, inventory, shipping, quantity, purchase actions, rating-present/absent state, and sticky-cart state. Record them as placeholders and never present them as verified customer facts.

## Required labels

Name temporary Figma nodes with a `Placeholder /` prefix and record them in the project manifest. The label belongs in the layer name and handoff data; it does not need to be visible on the rendered client preview.

Examples:

```text
Placeholder / Product Image
Placeholder / Product Name
Placeholder / Product Description
Placeholder / Review
Placeholder / Certification
```

## Client preview

- Use realistic but non-factual sample names and copy where final content is missing.
- Prefer generated or licensed category imagery for customer review.
- Keep the composition visually complete enough for the customer to judge hierarchy, spacing, and style.
- Keep the product type, configuration differences, feature differences, scene, crop, scale, and image density judgeable wherever those are part of the design responsibility.
- Do not reuse one generic image or abstract primitive for different products, configurations, features, or scenes when the media is meant to explain their difference.
- Do not show implementation classes, source warnings, replacement instructions, or large placeholder indexes as dominant content.
- Resolve visible copy/media from `content.customer_visible_ledger`. The visible value contains only storefront content; provenance, approval, replacement, and risk fields remain internal.
- Keep decision-critical commerce slots visibly complete enough to evaluate hierarchy, wrapping, state changes, and CTA behavior. Missing factual values do not justify deleting the price, option, inventory, shipping, purchase, or sticky-action responsibility from the design.
- Never render internal markers such as `Placeholder`, `TBD`, `TODO`, `Pending`, `Review concept`, `Requires approval`, `Requires confirmation`, `Requires validation`, `Replace before launch`, `待替换`, `未批准`, `待确认`, `概念预览`, `内部检查`, `QA`, `Rxx`, `Theme Native`, `Section Custom`, `source warning`, or `replacement instruction` inside customer-preview frames. Use product-specific, externally readable, non-factual storefront copy or omit the optional slot without leaving dead space.
- Do not turn evidence caution into visible draft-process copy. Certification, dimensions, performance, warranty, reviews, and other proof claims remain absent or use normal optional states when unsupported. Price, option, inventory, shipping, and purchase-control slots may use neutral presentation-only sample values when needed to prove layout and state behavior; keep their placeholder status only in the internal ledger and Chinese QA.
- Export customer screenshots only from client-preview frames.

## Handoff record

Store these outside the rendered client preview:

- Placeholder type and exact Figma node ID.
- Source class: customer, licensed, generated, competitor-reference, or temporary-unknown.
- Replacement owner.
- Theme section/block mapping.
- Publication restrictions.

## Forbidden

- Inventing product specifications, certifications, prices, shipping promises, warranties, medical claims, performance claims, cases, or reviews as facts. Neutral sample commerce values tracked as placeholders are permitted for design-state validation but must never be called approved, factual, or production-ready.
- Treating competitor imagery as approved customer material.
- Sending temporary competitor assets to production.
- Calling repeated empty rectangles or generic geometry a client-review image system when the design responsibility requires product, configuration, feature, or context differentiation.

Competitor imagery may be used only as clearly tagged internal composition reference. Prefer licensed or generated placeholders for customer-facing review. Replace all temporary assets before final production handoff.
