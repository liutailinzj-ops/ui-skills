---
name: iwish-component-resolver
description: Resolve the editable Figma component set required by an IWISH page blueprint by reusing compatible local/library components, extending or wrapping close matches, and creating project-local components when needed. Use after Figma foundations exist and before composing Shopify/WordPress Desktop and Mobile pages.
---

# IWISH Component Resolver

Create a bounded component map for the current page. Load the available Figma use and design-system/library Skills before Figma mutations.

## Inputs

- Page blueprint.
- Product and Competitor Analysis, including page-level DTC conversion or B2B buying responsibilities.
- Source Page Specification, Layout Topology Contract, composition groups, fidelity profile, and Theme Assembly Plan for specified-structure work.
- Reference Content-Layout Matrix for `structure_target` work.
- Product Coverage Matrix and template strategy for PDP work.
- Theme Capability Map for template or theme-customization work.
- Source Identity Fingerprint and explicit source-role table for specified-structure work.
- Project manifest and foundation IDs.
- Existing local components and accessible libraries.
- Platform/theme implementation notes.

## Resolve in This Order

1. For specified-structure theme work, verify that the Build Truth URL/fingerprint belongs to the structure source and each capability evidence URL belongs to the target theme. Stop on theme-demo self-mapping or source-identity mismatch.
2. For theme-based work, resolve the exact theme section/block primitive and each setting required by the cross-source mapping. Reject generic or invented theme-module names. In `theme_adaptation`, record an evidenced native substitute and its exact difference instead of inventing an exact match.
3. Reuse a compatible existing local component.
4. Import a compatible subscribed-library component.
5. Wrap or extend a visually useful component whose property API needs a local contract.
6. Create a project-local component.

Reuse only when properties, token bindings, naming, ownership, and editability are compatible. Do not detach imported instances merely to make them look editable.

Do not invent a bespoke component or mark a section custom when the Theme Capability Map identifies a supported native section. Represent brand styling through tokens, allowed settings, and content slots before changing the implementation class.

## Componentization Rules

Read [references/component-contract.md](references/component-contract.md).

- Componentize repeated elements and semantically reusable interactive elements.
- Do not force every unique editorial section into the company library.
- Keep project-specific components on `03_Local Components`.
- Use TEXT, BOOLEAN, and INSTANCE_SWAP properties where they make UI edits easier.
- Use INSTANCE_SWAP for icon or media choices instead of a variant per asset.
- If a variant matrix exceeds 30 combinations, split the component.
- Bind visual properties to variables where appropriate.
- Bind every client-facing text node to an approved text style.
- Define the grid span, equal-height policy, and Desktop/Mobile sizing contract for repeated cards before creating instances.
- Preserve the content slots and states needed to answer the page blueprint's product, proof, evaluation, objection, action, and buying-path responsibilities. Do not bake invented claims into component defaults.
- For PDP components, define content states rather than binding the API to one sampled product. Cover long/short titles, optional rating/badges, variant wrapping, gallery-count differences, optional subscription/RFQ, and absent below-fold content when applicable.
- Keep product-specific modules conditional. Do not bake one product's ingredients, specifications, proof, or story into the base PDP component contract.
- When the template strategy is `template_family`, record which components are shared and which are template-specific.
- For `structure_target`, record which unique `Rxx` source row, content slots, critical function, order, and Desktop/Mobile reading flow each component preserves or adapts.
- For `reference_to_theme`, resolve every stable source section ID to the exact theme section, block sequence, settings, content bindings, and Desktop/Mobile layout class in the Theme Assembly Plan. A generic component with different slots, item count, ordering, or layout class is not compatible.
- Preserve composition groups and major-region topology. Do not resolve a connected source experience into unrelated component families merely because their semantic labels match available theme sections.
- Accept `composed_native` only when every contributing native primitive and setting is evidenced and the assembled components satisfy the selected fidelity profile. For `strict_replication`, preserve source boundary, normalized geometry, visible-item count, interaction contract, and Mobile transformation. For `theme_adaptation`, allow a documented native difference while preserving critical function and reading flow.
- For `reference_to_theme`, require every component record to carry `structure_source_url`, `source_fingerprint_digest`, and `theme_capability_url`. Do not accept a component map whose source identity describes the theme demo instead of the specified page.
- In `strict_replication`, use only `exact_native`, valid `composed_native`, or explicitly approved deviations. In `theme_adaptation`, allow `native_adaptation`; if higher fidelity `requires_custom`, resolve the documented native fallback unless that custom form is explicitly required. Stop only for a critical `unresolved` mapping or failed source capture/identity.
- Keep implementation annotations in the manifest or handoff documentation, not as visible client-preview content.
- Build and validate one component family at a time.

## Company Library Policy

The absence of a company component library is not a blocker. Follow [references/promotion-policy.md](references/promotion-policy.md). Start project-local, collect evidence across real work, and promote only stable repeated patterns later.

## Output

Return a component map containing:

- Logical component ID.
- Figma component/component-set ID and key.
- Source: local, library, wrapped, or created.
- Variant axes and component properties.
- Variable/style bindings.
- Desktop/Mobile behavior.
- Page-blueprint sections that consume it.
- Analysis and journey responsibilities that consume it.
- Product archetypes and content states that consume it for PDP work.
- Reference section correspondence for `structure_target` work.
- Source section ID, priority, composition group, exact content-slot bindings, field-evidenced theme settings, Desktop/Mobile topology, and `exact_native | composed_native | native_adaptation | requires_custom | unresolved` status for specified-structure work.
- Proposed adaptations, their preserved responsibility, exact difference, evidence, and UI review owner.
- Exact theme section/block represented and permitted divergence.
- Grid span, equal-height policy, and overflow behavior.
- Validation screenshot and metadata status.
