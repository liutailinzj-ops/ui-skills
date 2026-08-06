# Placeholder Policy

Use placeholder mode whenever final customer copy, product data, or imagery is incomplete.

## Allowed

- Neutral temporary product names and descriptions.
- Client-presentable neutral image treatments.
- Licensed stock, generated images, or temporary internal references.
- Representative products selected for layout testing.
- AI-drafted copy marked as unapproved.

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
- Do not show implementation classes, source warnings, replacement instructions, or large placeholder indexes as dominant content.
- Export customer screenshots only from client-preview frames.

## Handoff record

Store these outside the rendered client preview:

- Placeholder type and exact Figma node ID.
- Source class: customer, licensed, generated, competitor-reference, or temporary-unknown.
- Replacement owner.
- Theme section/block mapping.
- Publication restrictions.

## Forbidden

- Inventing product specifications, certifications, prices, shipping promises, warranties, medical claims, performance claims, cases, or reviews as facts.
- Treating competitor imagery as approved customer material.
- Sending temporary competitor assets to production.

Competitor imagery may be used only as clearly tagged internal composition reference. Prefer licensed or generated placeholders for customer-facing review. Replace all temporary assets before final production handoff.
