---
name: iwish-component-resolver
description: Resolve the editable Figma component set required by an IWISH page blueprint by reusing compatible local/library components, extending or wrapping close matches, and creating project-local components when needed. Use after Figma foundations exist and before composing Shopify/WordPress Desktop and Mobile pages.
---

# IWISH Component Resolver

Create a bounded component map for the current page. Load the available Figma use and design-system/library Skills before Figma mutations.

## Inputs

- Page blueprint.
- Source Page Specification and Theme Assembly Plan for `reference_to_theme` work.
- Reference Content-Layout Matrix for `structure_target` work.
- Product Coverage Matrix and template strategy for PDP work.
- Theme Capability Map for template or theme-customization work.
- Project manifest and foundation IDs.
- Existing local components and accessible libraries.
- Platform/theme implementation notes.

## Resolve in This Order

1. For theme-based work, resolve the exact theme section/block primitive required by the approved mapping.
2. Reuse a compatible existing local component.
3. Import a compatible subscribed-library component.
4. Wrap or extend a visually useful component whose property API needs a local contract.
5. Create a project-local component.

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
- For PDP components, define content states rather than binding the API to one sampled product. Cover long/short titles, optional rating/badges, variant wrapping, gallery-count differences, optional subscription/RFQ, and absent below-fold content when applicable.
- Keep product-specific modules conditional. Do not bake one product's ingredients, specifications, proof, or story into the base PDP component contract.
- When the template strategy is `template_family`, record which components are shared and which are template-specific.
- For `structure_target`, record which source content/layout responsibility each component preserves or adapts.
- For `reference_to_theme`, resolve every stable source section ID to the exact theme section, block sequence, settings, content bindings, and Desktop/Mobile layout class in the Theme Assembly Plan. A generic component with different slots, item count, ordering, or layout class is not compatible.
- In `reference_to_theme`, use only `exact_native` or `composed_native` for a successful mapping. If a required mapping is `unresolved`, stop before creating or changing Figma components.
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
- Product archetypes and content states that consume it for PDP work.
- Reference section correspondence for `structure_target` work.
- Source section ID, exact content-slot bindings, theme settings, Desktop/Mobile layout classes, and `exact_native | composed_native | unresolved` status for `reference_to_theme` work.
- Exact theme section/block represented and permitted divergence.
- Grid span, equal-height policy, and overflow behavior.
- Validation screenshot and metadata status.
