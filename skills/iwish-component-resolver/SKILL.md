---
name: iwish-component-resolver
description: Resolve the editable Figma component set required by an IWISH page blueprint by reusing compatible local/library components, extending or wrapping close matches, and creating project-local components when needed. Use after Figma foundations exist and before composing Shopify/WordPress Desktop and Mobile pages.
---

# IWISH Component Resolver

Create a bounded component map for the current page. Load the available Figma use and design-system/library Skills before Figma mutations.

## Inputs

- Page blueprint.
- Project manifest and foundation IDs.
- Existing local components and accessible libraries.
- Platform/theme implementation notes.

## Resolve in This Order

1. Reuse a compatible existing local component.
2. Import a compatible subscribed-library component.
3. Wrap or extend a visually useful component whose property API needs a local contract.
4. Create a project-local component.

Reuse only when properties, token bindings, naming, ownership, and editability are compatible. Do not detach imported instances merely to make them look editable.

## Componentization Rules

Read [references/component-contract.md](references/component-contract.md).

- Componentize repeated elements and semantically reusable interactive elements.
- Do not force every unique editorial section into the company library.
- Keep project-specific components on `03_Local Components`.
- Use TEXT, BOOLEAN, and INSTANCE_SWAP properties where they make UI edits easier.
- Use INSTANCE_SWAP for icon or media choices instead of a variant per asset.
- If a variant matrix exceeds 30 combinations, split the component.
- Bind visual properties to variables where appropriate.
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
- Validation screenshot and metadata status.

