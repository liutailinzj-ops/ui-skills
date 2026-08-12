---
name: iwish-page-strategy
description: Analyze products, category context, competitors, DTC conversion chains or B2B buying paths, then define an evidence-backed page blueprint and implementation route. Use for Shopify or WordPress research-led partial theme customization, selected competitor-module translation into partial theme customization, or fully custom UI production before visual direction and Figma page generation.
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
- `hybrid_led`: preserve selected source modules and design remaining responsibilities from research.
- `custom_led`: derive an original page system from requirements, research, references, and available brand inputs without theme-module constraints.

Keep selected structure sources, theme-capability sources, competitor evidence, and visual inspiration in separate roles throughout the workflow.

## Selected Competitor-Module Work

For `selected_structure_modules`, capture only the explicitly named source modules and the minimum surrounding context needed to understand their boundaries, interaction, responsive behavior, and role in the journey. Do not make the rest of the source page mandatory; design the remaining page from product, category, competitor, and journey evidence.

Read [references/responsive-section-contract.md](references/responsive-section-contract.md) and [references/layout-topology-contract.md](references/layout-topology-contract.md). Verify the identity of every selected source module before theme mapping. Do not continue when a selected module's critical function is unresolved and no feasible native or scoped custom route exists.

For theme-based work, build the Theme Capability Map in [references/theme-capability-map.md](references/theme-capability-map.md) from current official theme listing, vendor documentation, editor evidence, and live demo where useful. Map across sources:

```text
structure source Rxx
→ exact target-theme Section / Blocks / Settings / responsive behavior
→ theme capability evidence
```

A theme demo may prove capability but may not replace a selected competitor module's structure source.

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
- For native/configured theme Sections, use documented theme breakpoint settings or observed automatic behavior. For custom Sections and fully custom work, define an explicit responsive implementation plan without creating a second content or component system.
- Use `native_adaptation` only when evidenced native behavior preserves required content, critical function, and reading order while changing a named topology detail.
- Resolve theme implementation in this order: native theme → configuration → style → custom CSS → custom Liquid → custom section → custom.
- For theme customization, decide each Section independently as native, configured, styled, CSS, Liquid, new custom Section, app/third-party, or pending engineering confirmation. Do not impose a universal custom-work percentage.
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
