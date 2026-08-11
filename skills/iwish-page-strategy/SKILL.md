---
name: iwish-page-strategy
description: Analyze products, category context, competitors, DTC conversion chains or B2B buying paths, then define an evidence-backed page blueprint and theme implementation route. Use for Shopify or WordPress research-led, specified-reference, hybrid-reference, current-site revision, template, theme-customized, or fully custom UI production before visual direction and Figma page generation.
---

# IWISH Page Strategy

Produce the business, content, source, and implementation blueprint that `$iwish-visual-direction` will translate into a visual system. Treat common ecommerce patterns as baselines, not templates.

## Inputs

- Production project manifest from `$iwish-ui-workflow`.
- Customer facts, assets, current site, requested page, and contracted features.
- Separate structure, theme-capability, competitor, and visual-inspiration sources.
- Site model, strategy mode, build route, theme state, content state, and website language.

## Research

Read [references/product-competitor-analysis.md](references/product-competitor-analysis.md) and [references/research-method.md](references/research-method.md). Complete product, category, competitor, and DTC conversion-chain or B2B buying-path analysis before page hierarchy or theme selection.

- `research_led`: let product, competitor, and journey evidence determine content responsibilities and sequence.
- `reference_led`: test source relevance and risks but do not silently change the requested structure.
- `hybrid_led`: preserve selected source modules and design remaining responsibilities from research.
- `existing_site_led`: decide what current content and proof to retain, revise, relocate, or replace.

Use [references/reference-routing.md](references/reference-routing.md) to keep source roles separate.

## Specified-Reference Work

For `structure_target`, capture every visible module as one stable Rxx source row, then record shared content responsibility, content items, ordering, connected composition groups, responsive anatomy, and target-theme correspondence. Read [references/responsive-section-contract.md](references/responsive-section-contract.md), [references/reference-to-theme.md](references/reference-to-theme.md), and [references/layout-topology-contract.md](references/layout-topology-contract.md). Apply `theme_adaptation` unless exact replication is explicit.

For strict `reference_to_theme`, verify source identity and complete source capture before theme mapping. Do not continue when required topology or critical function is unresolved and no approved route exists.

For theme-based work, build the Theme Capability Map in [references/theme-capability-map.md](references/theme-capability-map.md) from current official theme listing, vendor documentation, editor evidence, and live demo where useful. Map across sources:

```text
structure source Rxx
→ exact target-theme Section / Blocks / Settings / responsive behavior
→ theme capability evidence
```

A theme demo may prove capability but may not replace Build Truth.

## Strategy Rules

- Derive hierarchy from product category, market, audience, decision complexity, available proof, and page purpose.
- For DTC, trace product comprehension, desire/relevance, trust/proof, evaluation, objection reduction, action, and retention only where relevant.
- For B2B, apply [references/dtc-b2b-routing.md](references/dtc-b2b-routing.md).
- Do not ask the customer to design page structure or supply marketing strategy.
- Do not require a priority product. Select representative content and keep it replaceable.
- Mark missing customer facts and assets as temporary instead of inventing claims.
- For PDP work, apply [references/pdp-coverage.md](references/pdp-coverage.md); do not claim catalog-wide coverage from one product.
- Preserve connected source compositions. Do not split them into unrelated full-width sections because semantic module names appear to match.
- Define one Responsive Section Contract per page section. Desktop and Mobile are breakpoint states of the same section identity and shared content, not separate compositions.
- For theme-based work, permit only documented theme breakpoint settings or observed automatic theme behavior. For custom work, define intentional breakpoint changes without creating a second content or component system.
- Use `native_adaptation` only when evidenced native behavior preserves required content, critical function, and reading order while changing a named topology detail.
- Resolve theme implementation in this order: native theme → configuration → style → custom CSS → custom Liquid → custom section → custom.
- Keep template work within native/configuration/style scope unless custom work is explicitly approved.
- Do not select a visual palette, component house style, or generic Figma layout in this Skill. Provide evidence and requirements to `$iwish-visual-direction`.
- Do not read or execute repository regression fixtures in production.

## Output

Produce [references/page-blueprint.md](references/page-blueprint.md) with:

- Product and Competitor Analysis, evidence gaps, and conversion or buying-path implications.
- Page responsibilities, content types, sequence, responsive priority, and asset state.
- Theme Capability Map and Theme Assembly Plan for theme-based work.
- Responsive Section Contract, alignment groups, shared content bindings, and breakpoint states.
- Source specification, content-layout matrix, topology contract, and composition groups when applicable.
- Product Coverage Matrix and truthful PDP template strategy when applicable.
- Component requirements and implementation level without pre-designing generic components.
- A Visual Direction Brief containing required brand impression, content emphasis, source visual principles, theme constraints, imagery needs, and responsive priorities. This is input to the visual-direction Skill, not a finished visual direction.

Do not write to Figma and do not produce QA or regression results in this Skill.
