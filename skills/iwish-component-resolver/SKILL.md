---
name: iwish-component-resolver
description: Resolve editable responsive IWISH Figma components and Section families, theme/source contracts, properties, and breakpoint states, then arrange active masters in an aligned usable component-library presentation. Use after Figma foundations and visual direction exist and before Shopify/WordPress page assembly.
---

# IWISH Component Resolver

Create a bounded component map for the current page. Load the available Figma use and design-system/library Skills before Figma mutations.

## Inputs

- Page blueprint.
- Active Visual Direction Contract, applicable approved page override, representative Section-family node IDs, and paired breakpoint-proof node IDs.
- Responsive Section Contracts, alignment groups, shared content bindings, and allowed breakpoint differences.
- Product and Competitor Analysis, including page-level DTC conversion or B2B buying responsibilities.
- Selected-module specification, Layout Topology Contract, composition groups, and Theme Assembly Plan for selected competitor-module work.
- Reference Content-Layout Matrix for selected-module structure work.
- Product Coverage Matrix and template strategy for PDP work.
- Theme Capability Map and per-Section implementation classification for theme-customization work.
- Source Identity Fingerprint and explicit source-role table for selected competitor-module work.
- Project manifest and foundation IDs.
- Existing local components and accessible libraries.
- Platform/theme implementation notes.

## Resolve in This Order

1. For selected competitor-module work, verify that each selected module's source URL/fingerprint belongs to the structure source and each capability evidence URL belongs to the target theme. Stop on theme-demo self-mapping or source-identity mismatch.
2. For theme-based work, resolve the exact theme section/block primitive and each setting required by the cross-source mapping. Reject generic or invented theme-module names. In `theme_adaptation`, record an evidenced native substitute and its exact difference instead of inventing an exact match.
3. Reuse a compatible existing local component.
4. Import a compatible subscribed-library component.
5. Wrap or extend a visually useful component whose property API needs a local contract.
6. Create a project-local component.

Reuse only when properties, token bindings, naming, ownership, and editability are compatible. Do not detach imported instances merely to make them look editable.

Do not invent a bespoke component or mark a section custom when the Theme Capability Map identifies a supported native section. Represent brand styling through tokens, allowed settings, and content slots before changing the implementation class.

Do not resolve components from a generic house library before reading the Visual Direction Contract. A technically compatible component is not visually compatible when its hierarchy, media ratio, density, card language, or responsive behavior contradicts the approved direction. If the representative compositions are missing or still generic, return the missing visual-direction dependency instead of creating a fallback black-box system.

Retrieved design recommendations and unapproved candidates do not qualify as component requirements. For a targeted revision, resolve only the named component family and directly invalidated shared dependencies; preserve every unrelated component ID and instance.

## Componentization Rules

Read [references/component-contract.md](references/component-contract.md) and [references/component-library-presentation.md](references/component-library-presentation.md).

- Componentize repeated elements and semantically reusable interactive elements.
- Do not force every unique editorial section into the company library.
- Keep project-specific components on `03_Local Components`.
- Use TEXT, BOOLEAN, and INSTANCE_SWAP properties where they make UI edits easier.
- Use INSTANCE_SWAP for icon or media choices instead of a variant per asset.
- If a variant matrix exceeds 30 combinations, split the component.
- Bind visual properties to variables where appropriate.
- Bind every client-facing text node to an approved text style.
- Define the grid span, equal-height policy, and responsive sizing contract for repeated cards before creating instances.
- Preserve the content slots and states needed to answer the page blueprint's product, proof, evaluation, objection, action, and buying-path responsibilities. Do not bake invented claims into component defaults.
- Preserve the Visual Direction Contract's typography, imagery, density, spacing rhythm, media/content relationship, control language, and responsive transformation through component properties and layout contracts.
- Resolve one component family per Responsive Section Contract. Use shared subcomponents, content properties, and the smallest necessary viewport variants; do not resolve Desktop and Mobile as unrelated components.
- Keep content-slot names, copy bindings, controls, source IDs, and Section order identical across breakpoint variants unless a recorded content variant has evidence.
- For PDP components, define content states rather than binding the API to one sampled product. Cover long/short titles, optional rating/badges, variant wrapping, gallery-count differences, optional subscription/RFQ, and absent below-fold content when applicable.
- Keep product-specific modules conditional. Do not bake one product's ingredients, specifications, proof, or story into the base PDP component contract.
- When the template strategy is `template_family`, record which components are shared and which are template-specific.
- For `selected_structure_modules`, require that correspondence only for explicitly selected source modules; components for the rest of the page trace to research-backed page responsibilities.
- Preserve composition groups and major-region topology. Do not resolve a connected source experience into unrelated component families merely because their semantic labels match available theme sections.
- Accept `composed_native` only when every contributing native primitive and setting is evidenced and the assembled components preserve the selected module's critical function and reading flow. Otherwise record `native_adaptation` or the scoped custom implementation.
- For selected competitor-module work, require every source-derived component record to carry `structure_source_url`, `source_fingerprint_digest`, and `theme_capability_url`. Do not accept a component map whose source identity describes the theme demo instead of the selected competitor module.
- In `theme_adaptation`, allow `native_adaptation` and feasible in-scope custom implementation. Stop only for a critical `unresolved` mapping or failed source capture/identity.
- Keep implementation annotations in the manifest or handoff documentation, not as visible client-preview content.
- Build and validate one component family at a time.
- Place every active master or component set into the aligned component-library root, category, and family row as it is created. Do not leave masters floating on the canvas and organize them later.
- Capture the component library at readable scale before page assembly. Fail when categories, family rows, paired breakpoint variants, component-set bounds, captions, or variant order are not aligned and usable by UI.

## Company Library Policy

The absence of a company component library is not a blocker. Follow [references/promotion-policy.md](references/promotion-policy.md). Start project-local, collect evidence across real work, and promote only stable repeated patterns later.

## Output

Return a component map containing:

- Logical component ID.
- Figma component/component-set ID and key.
- Source: local, library, wrapped, or created.
- Variant axes and component properties.
- Variable/style bindings.
- Responsive behavior, breakpoint states, paired instance contract, and allowed differences.
- Page-blueprint sections that consume it.
- Analysis and journey responsibilities that consume it.
- Product archetypes and content states that consume it for PDP work.
- Reference-section correspondence for explicitly selected modules in `selected_structure_modules` work.
- Source section ID, priority, composition group, exact shared content-slot bindings, field-evidenced theme settings, paired breakpoint topology, and `exact_native | composed_native | native_adaptation | requires_custom | unresolved` status for selected-module work.
- Proposed adaptations, their preserved responsibility, exact difference, evidence, and UI review owner.
- Exact theme section/block represented and permitted divergence.
- Alignment group, container mode, grid span, equal-height policy, and explicit overflow behavior.
- Validation screenshot and metadata status.
- Visual-direction correspondence and any component-level divergence from the representative compositions.
- Component-library root/category/family-row node IDs, presentation screenshot, alignment status, and active/archive separation.
