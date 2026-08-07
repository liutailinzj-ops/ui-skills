---
name: iwish-page-strategy
description: Analyze products, category context, competitors, DTC conversion chains or B2B buying paths, then define a project-specific website blueprint or reference conversion plan. Use for Shopify or WordPress DTC/B2B research-led, specified-reference, hybrid-reference, current-site revision, template, theme-customized, or fully custom UI strategy.
---

# IWISH Page Strategy

Produce the page blueprint that downstream Figma Skills will build. Treat common ecommerce structures as a baseline, not a template.

## Inputs

- Project manifest from `$iwish-ui-workflow`.
- Existing customer assets and current site when available.
- Separate structure-source URLs and theme-capability URLs for template or theme-customization work. Treat the former as Build Truth and the latter as implementation evidence.
- Requested page and contracted features.
- Inferred `site_model`, `strategy_mode`, `build_route`, `theme_state`, and content state.

## Research

Read [references/product-competitor-analysis.md](references/product-competitor-analysis.md) and produce the Product and Competitor Analysis before page hierarchy, theme selection, or reference conversion. Then read [references/research-method.md](references/research-method.md). Browse current first-party product, competitor, category, and reference sources when internet access is available. Research what users need to understand and how the market presents, proves, compares, and converts; do not copy a competitor page or visual identity.

Apply the analysis according to `strategy_mode`:

- `research_led`: let product, competitor, and journey evidence determine the content hierarchy.
- `reference_led`: use analysis to test source relevance and identify conversion risks, but do not silently change an approved strict structure.
- `hybrid_led`: preserve selected source modules and use analysis to supply the remaining responsibilities.
- `existing_site_led`: use analysis to decide what current content and proof to retain, revise, relocate, or replace.

Assign source roles before analysis and follow [references/reference-routing.md](references/reference-routing.md). Never merge the structure source and theme capability source into a generic reference field:

- `reference_to_theme`: strict conversion for an explicitly exact/no-change target. Convert the captured page into evidenced theme sections/blocks without creative restructuring. Read [references/reference-to-theme.md](references/reference-to-theme.md).
- `structure_target`: the production default when the client expects the selected theme to represent a reference page's content structure and layout logic. Use `theme_adaptation` unless exact replication is explicit.
- `visual_inspiration`: use art direction and presentation principles without preserving section correspondence.
- `competitor_evidence`: use the site to understand category conventions, gaps, and opportunities.

For `structure_target`, produce a complete stable `Rxx` Source Page Specification and Reference Content-Layout Matrix before the page blueprint. Analyze every visible module's content responsibility, content items, Desktop/Mobile anatomy, ordering, conditional behavior, and theme correspondence. Create composition groups only after the `Rxx` list is complete; groups reference rows and never replace them. Reuse the capture and mapping schemas in [references/reference-to-theme.md](references/reference-to-theme.md), but apply the `theme_adaptation` gate instead of strict fidelity thresholds. Do not reduce the source to screenshots, topic summaries, or mood adjectives.

For strict `reference_to_theme`, produce the Source Identity Fingerprint and Source Page Specification from the specified structure source first. Read [references/layout-topology-contract.md](references/layout-topology-contract.md), capture section topology and composition groups, then produce the Theme Assembly Plan using only separate theme capability sources. Do not write the page blueprint or continue to Figma until source identity and source capture pass, Desktop and Mobile topology evidence exists, and every source section and composition group is mapped or a deviation is explicitly approved.

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
- Classify every source row as `critical`, `structural`, or `presentational`. Critical means a purchase, inquiry, navigation, comparison, legally required, or other indispensable interaction/content responsibility; structural means order, grouping, and major-region logic; presentational means columns, exact dimensions, spacing, crop, and decoration.
- For `structure_target` with `theme_adaptation`, preserve every relevant source row, content responsibility, content binding, sequence, critical function, and Desktop/Mobile reading flow. Allow documented theme-native adaptations to structural or presentational topology when they preserve the essential responsibility.
- For `reference_to_theme`, do not derive a new content hierarchy, add category-best-practice modules, improve the source sequence, or select a different layout. Preserve captured source content, order, and layout class. Separate temporary source material from customer-approved production content.
- For `reference_to_theme`, treat layout topology as Build Truth: preserve composition groups, major-region geometry, repeated-item visibility, interaction viewport, overflow, and Desktop/Mobile transformation. A matching topic or section title is not a topology match.
- Do not split a connected source composition group into independent full-width sections unless target-theme evidence reproduces the same visible relationship or a named deviation is explicitly approved.
- For `reference_to_theme`, the Build Truth URL, product/category identity, H1, hero signature, and stable section sequence must remain the specified structure source throughout all artifacts. A theme demo cannot replace it merely because the demo is easier to inspect or maps cleanly.
- Map across sources: `structure source Rxx -> target theme Section/Blocks/Settings -> theme capability evidence URL`. A map of `theme demo section -> same theme demo section` is invalid and must never contribute to coverage.
- Use exact theme-editor or vendor-documentation names. A generic label such as `approved modular composition`, `static prototype`, or `native-like section` is not a valid target-theme mapping.
- Allow `composed_native` only when each contributing native primitive is evidenced and their combined output preserves the required fidelity profile. In `strict_replication`, this includes source boundary and exact topology. In `theme_adaptation`, multiple adjacent native primitives may preserve one visually continuous responsibility when the relationship and reading flow remain clear.
- Use `native_adaptation` when an evidenced theme-native substitute preserves required content, critical function, and reading order while changing a non-critical topology detail. Use `requires_custom` when higher fidelity needs code, and record the best feasible native fallback separately.
- Treat approval as provenance, not wording. Record the decision, exact deviation, approver, source, and date before using `approved`; generated layer names or reports cannot create approval.
- A creative content responsibility does not imply custom implementation. Map it to an exact theme section or block before considering code.
- Resolve theme-based implementation in this order: `theme_native` -> `configuration` -> `style` -> `custom_css` -> `custom_liquid` -> `section_custom` -> `custom`.
- For `template` work, do not use `custom_liquid`, `section_custom`, or `custom` without explicit scope approval.
- For `theme_customization` work, keep `section_custom` and `custom` at or below 20% of both section count and estimated page height by default. Record explicit approval for every exception.
- Stop the strategy only when source capture is incomplete, required theme evidence is unavailable, source identity fails, a critical responsibility has no feasible native or approved custom route, or a material route/budget decision remains unresolved. A presentational or structural difference with an evidenced native substitute is not a blocker in `theme_adaptation`.

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

For `structure_target`, report complete `Rxx` and content-item coverage, critical responsibility coverage, exact mappings, native adaptations, ordering/layout divergences, and theme-constrained substitutions. Label AI-selected differences `proposed_adaptation` for UI review. For PDP work, report `single_template_validated`, `template_family`, or `coverage_partial`.

For `reference_to_theme`, report Build Truth URL identity, source fingerprint match, product/category identity, source section count, exact order match, visible content-item coverage, composition-group coverage, Desktop topology coverage, Mobile topology coverage, resolved cross-source theme mapping count, and approved deviations with provenance. Use `blocked` when identity fails or any unapproved value is below 100%.

Do not write to Figma in this Skill. Pass the blueprint to the foundation, component, and page-building Skills.
