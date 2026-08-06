# Component Contract

## Stable base candidates

Use or create only when required by the page:

- Button and Icon Button.
- Text Link.
- Input, Select, Checkbox.
- Badge.
- Accordion.
- Content Container.
- Section Heading.

## Project-local candidates

Keep these local until repeated use proves stability:

- Header and Mega Menu.
- Product/Collection Card.
- Product Gallery and Product Information.
- Variant Selector.
- Reviews and proof modules.
- Ingredient, size, specification, certification, case, or RFQ modules.
- Distinctive Hero and editorial sections.

For theme-based work, keep a theme-specific section shell local to the project. Its contract must preserve the native section's supported blocks, settings, ordering, and responsive behavior. A local Figma component is not permission to require a custom Shopify or WordPress section.

## Layout contract

Record these fields for repeated layout components:

```text
GRID_SPAN     Desktop and Mobile columns occupied
WIDTH_MODE    FILL, FIXED, or HUG with reason
HEIGHT_MODE   equal-height, content-height, or intentional mixed-height
OVERFLOW      none, wrap, carousel, scroll, or clip with an explicit interaction
THEME_MAP     exact native section/block name and evidence
```

- Use equal-height siblings for cards in the same comparison or decision row unless the blueprint documents intentional asymmetry.
- Prefer FILL or grid-derived widths over manually rounded widths.
- A carousel must define viewport width, card width, gap, visible next-card preview, controls or indicator, and theme-supported behavior.
- Do not use clipping to hide a card that is wider than the Mobile content grid.

## Properties

Use the smallest useful API:

```text
TEXT         editable labels and content
BOOLEAN      optional labels, badges, icons, proof, helper text
INSTANCE_SWAP replaceable icon/media/content subcomponent
VARIANT      size, style, state, and only necessary viewport differences
```

Avoid exposing every visual detail as a variant. UI should be able to update content and common states without detaching the instance.
