---
name: iwish-page-strategy
description: Analyze products, category context, competitors, DTC conversion chains or B2B buying paths, then define a project-specific website blueprint or reference conversion plan. Use for Shopify or WordPress DTC/B2B research-led, specified-reference, hybrid-reference, current-site revision, template, theme-customized, or fully custom UI strategy.
---

# IWISH Page Strategy

Produce the page blueprint that downstream Figma Skills will build. Treat common ecommerce structures as a baseline, not a template.

## Inputs

- Project manifest from `$iwish-ui-workflow`.
- Existing customer assets and current site when available.
- Theme/demo reference for template or theme-customization work. Treat this as required evidence, not optional inspiration.
- Requested page and contracted features.
- Inferred `site_model`, `strategy_mode`, `build_route`, `theme_state`, and content state.

## Research

Read [references/product-competitor-analysis.md](references/product-competitor-analysis.md) and produce the Product and Competitor Analysis before page hierarchy, theme selection, or reference conversion. Then read [references/research-method.md](references/research-method.md). Browse current first-party product, competitor, category, and reference sources when internet access is available. Research what users need to understand and how the market presents, proves, compares, and converts; do not copy a competitor page or visual identity.

Apply the analysis according to `strategy_mode`:

- `research_led`: let product, competitor, and journey evidence determine the content hierarchy.
- `reference_led`: use analysis to test source relevance and identify conversion risks, but do not silently change an approved strict structure.
- `hybrid_led`: preserve selected source modules and use analysis to supply the remaining responsibilities.
- `existing_site_led`: use analysis to decide what current content and proof to retain, revise, relocate, or replace.

Classify references before analysis and follow [references/reference-routing.md](references/reference-routing.md):

- `reference_to_theme`: convert the captured reference page's visible content inventory, section order, and Desktop/Mobile layout anatomy into evidenced theme sections/blocks without creative restructuring. Read [references/reference-to-theme.md](references/reference-to-theme.md).
- `structure_target`: the client expects the target page's content structure and layout logic to be represented through the selected theme.
- `visual_inspiration`: use art direction and presentation principles without preserving section correspondence.
- `competitor_evidence`: use the site to understand category conventions, gaps, and opportunities.

For `structure_target`, produce a Reference Content-Layout Matrix before the page blueprint. Analyze content responsibilities, content types, Desktop/Mobile anatomy, ordering, conditional behavior, and theme correspondence. Do not reduce the source to screenshots or mood adjectives.

For `reference_to_theme`, produce the Source Page Specification first, then the Theme Assembly Plan. Do not write the page blueprint or continue to Figma until every source section is mapped or a deviation is explicitly approved.

For template or theme-customization work, build the Theme Capability Map in [references/theme-capability-map.md](references/theme-capability-map.md) before writing the page blueprint. Use the current official theme listing, theme-vendor documentation, and live demo where available. Do not infer theme feasibility from visual similarity alone.

## Strategy Rules

- Derive the content hierarchy from product category, market, audience type, decision complexity, available proof, and page purpose already established internally.
- For DTC, trace the relevant page responsibilities across product comprehension, relevance/desire, trust/proof, evaluation/selection, objection/risk reduction, action, and retention where applicable. This is a decision chain, not a fixed section list.
- Record competitor presentation logic and conversion sequencing, not just visual style. Separate category conventions from distinctive competitor choices and unsupported claims.
- Do not ask the customer to design the page structure.
- Do not require a priority product. Select representative content for composition and keep it replaceable.
- Do not force every DTC homepage into the same Hero -> USP -> Products -> Reviews -> FAQ sequence.
- Use different content responsibilities for DTC and B2B as described in [references/dtc-b2b-routing.md](references/dtc-b2b-routing.md).
- Mark any section that depends on missing customer facts as placeholder-backed.
- For PDP work, read [references/pdp-coverage.md](references/pdp-coverage.md). Analyze the catalog or available product records, define product archetypes, and decide whether the project needs one validated base template or a template family.
- Treat a supplied PDP as one product state, not proof of a universal template. Preserve reusable content responsibilities while making product-specific modules conditional.
- When only one product can be inspected, use `coverage_partial`; do not claim that the layout fits the full catalog.
- For `structure_target`, preserve source responsibility coverage and sequence unless theme evidence, product relevance, mobile behavior, or scope requires a documented adaptation.
- For `reference_to_theme`, do not derive a new content hierarchy, add category-best-practice modules, improve the source sequence, or select a different layout. Preserve captured source content, order, and layout class. Separate temporary source material from customer-approved production content.
- A creative content responsibility does not imply custom implementation. Map it to an exact theme section or block before considering code.
- Resolve theme-based implementation in this order: `theme_native` -> `configuration` -> `style` -> `custom_css` -> `custom_liquid` -> `section_custom` -> `custom`.
- For `template` work, do not use `custom_liquid`, `section_custom`, or `custom` without explicit scope approval.
- For `theme_customization` work, keep `section_custom` and `custom` at or below 20% of both section count and estimated page height by default. Record explicit approval for every exception.
- Stop the strategy as blocked when a theme-based section has no evidenced mapping, the theme reference is unavailable, or the custom budget is exceeded without approval. Do not silently fall back to a custom DTC layout.

## Output

Produce the schema in [references/page-blueprint.md](references/page-blueprint.md). Include:

- Product and Competitor Analysis with evidence gaps, conversion/buying chain, and page implications.
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

For `reference_to_theme`, report source section count, exact order match, visible content-item coverage, Desktop layout-class coverage, Mobile layout-class coverage, resolved theme mapping count, and approved deviations. Use `blocked` when any unapproved value is below 100%.

Do not write to Figma in this Skill. Pass the blueprint to the foundation, component, and page-building Skills.
