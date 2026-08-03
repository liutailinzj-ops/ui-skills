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

## Properties

Use the smallest useful API:

```text
TEXT         editable labels and content
BOOLEAN      optional labels, badges, icons, proof, helper text
INSTANCE_SWAP replaceable icon/media/content subcomponent
VARIANT      size, style, state, and only necessary viewport differences
```

Avoid exposing every visual detail as a variant. UI should be able to update content and common states without detaching the instance.

