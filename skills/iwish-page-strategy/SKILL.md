---
name: iwish-page-strategy
description: Research and define a project-specific website page blueprint from brand facts, product category, target market, competitor/reference sites, internal scope, and available assets. Use for Shopify or WordPress DTC/B2B page strategy when the section structure, content emphasis, responsive priorities, and required UI patterns must be derived rather than supplied by the customer.
---

# IWISH Page Strategy

Produce the page blueprint that downstream Figma Skills will build. Treat common ecommerce structures as a baseline, not a template.

## Inputs

- Project manifest from `$iwish-ui-workflow`.
- Existing customer assets and current site when available.
- Theme/demo reference for template or theme-customization work. Treat this as required evidence, not optional inspiration.
- Requested page and contracted features.

## Research

Read [references/research-method.md](references/research-method.md). Browse current first-party competitor, category, and reference sites when internet access is available. Research what users need to understand and which patterns the market uses; do not copy a competitor page or visual identity.

Classify references before analysis and follow [references/reference-routing.md](references/reference-routing.md):

- `structure_target`: the client expects the target page's content structure and layout logic to be represented through the selected theme.
- `visual_inspiration`: use art direction and presentation principles without preserving section correspondence.
- `competitor_evidence`: use the site to understand category conventions, gaps, and opportunities.

For `structure_target`, produce a Reference Content-Layout Matrix before the page blueprint. Analyze content responsibilities, content types, Desktop/Mobile anatomy, ordering, conditional behavior, and theme correspondence. Do not reduce the source to screenshots or mood adjectives.

For template or theme-customization work, build the Theme Capability Map in [references/theme-capability-map.md](references/theme-capability-map.md) before writing the page blueprint. Use the current official theme listing, theme-vendor documentation, and live demo where available. Do not infer theme feasibility from visual similarity alone.

## Strategy Rules

- Derive the content hierarchy from product category, market, audience type, decision complexity, available proof, and page purpose already established internally.
- Do not ask the customer to design the page structure.
- Do not require a priority product. Select representative content for composition and keep it replaceable.
- Do not force every DTC homepage into the same Hero -> USP -> Products -> Reviews -> FAQ sequence.
- Use different content responsibilities for DTC and B2B as described in [references/dtc-b2b-routing.md](references/dtc-b2b-routing.md).
- Mark any section that depends on missing customer facts as placeholder-backed.
- For PDP work, read [references/pdp-coverage.md](references/pdp-coverage.md). Analyze the catalog or available product records, define product archetypes, and decide whether the project needs one validated base template or a template family.
- Treat a supplied PDP as one product state, not proof of a universal template. Preserve reusable content responsibilities while making product-specific modules conditional.
- When only one product can be inspected, use `coverage_partial`; do not claim that the layout fits the full catalog.
- For `structure_target`, preserve source responsibility coverage and sequence unless theme evidence, product relevance, mobile behavior, or scope requires a documented adaptation.
- A creative content responsibility does not imply custom implementation. Map it to an exact theme section or block before considering code.
- Resolve theme-based implementation in this order: `theme_native` -> `configuration` -> `style` -> `custom_css` -> `custom_liquid` -> `section_custom` -> `custom`.
- For `template` work, do not use `custom_liquid`, `section_custom`, or `custom` without explicit scope approval.
- For `theme_customization` work, keep `section_custom` and `custom` at or below 20% of both section count and estimated page height by default. Record explicit approval for every exception.
- Stop the strategy as blocked when a theme-based section has no evidenced mapping, the theme reference is unavailable, or the custom budget is exceeded without approval. Do not silently fall back to a custom DTC layout.

## Output

Produce the schema in [references/page-blueprint.md](references/page-blueprint.md). Include:

- Theme Capability Map and evidence URLs for theme-based work.
- Reference classification and Reference Content-Layout Matrix when a reference is supplied.
- Product Coverage Matrix, template strategy, conditional modules, and tested product states for PDP work.
- One-sentence strategic concept.
- Section sequence and responsibility.
- Required content type, not invented factual content.
- Desktop and Mobile priority.
- Component needs.
- Asset status.
- Exact theme section/block mapping and implementation level.
- Custom-section count and estimated-height ratios.
- One primary design direction and, only when materially useful, one alternative direction.

For `structure_target`, report responsibility coverage, ordering divergences, layout divergences, and theme-constrained substitutions. For PDP work, report `single_template_validated`, `template_family`, or `coverage_partial`.

Do not write to Figma in this Skill. Pass the blueprint to the foundation, component, and page-building Skills.
