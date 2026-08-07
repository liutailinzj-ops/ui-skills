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

For PDP work, model variable product content through properties and conditional subcomponents. Do not create a component that remains editable only for the representative product used in the client preview.

## Layout contract

Record these fields for repeated layout components:

```text
GRID_SPAN     Desktop and Mobile columns occupied
WIDTH_MODE    FILL, FIXED, or HUG with reason
HEIGHT_MODE   equal-height, content-height, or intentional mixed-height
OVERFLOW      none, wrap, carousel, scroll, or clip with an explicit interaction
THEME_MAP     exact native section/block name and evidence
PRODUCT_STATES product archetypes and optional/required content states validated
REFERENCE_MAP source responsibility and layout anatomy preserved or adapted
FIDELITY_PROFILE strict_replication or theme_adaptation
MAPPING_STATUS exact_native, composed_native, native_adaptation, requires_custom, or unresolved
SOURCE_MAP    stable source section ID and exact source item order
CONTENT_BINDINGS source text/media/control/repeated-item slots mapped one by one
THEME_SETTINGS exact section/block settings supported by theme evidence
LAYOUT_CLASS  Desktop and Mobile source layout class and target match status
COMPOSITION_GROUP connected source region that must remain visually or interactively continuous
TOPOLOGY normalized major-region bounds, media ratios, repetition, interaction, and responsive transformation
SETTING_EVIDENCE exact evidence for every theme setting used
```

- Use equal-height siblings for cards in the same comparison or decision row unless the blueprint documents intentional asymmetry.
- Prefer FILL or grid-derived widths over manually rounded widths.
- A carousel must define viewport width, card width, gap, visible next-card preview, controls or indicator, and theme-supported behavior.
- Do not use clipping to hide a card that is wider than the Mobile content grid.
- Define the collapse behavior when product-specific content is absent; empty modules must not leave reserved blank height.

For specified-structure work, the contract must preserve the primary reference page's visible content slots, stable ordering, critical function, and Desktop/Mobile reading flow. In `strict_replication`, repeated-item count and topology must also match unless explicitly approved. In `theme_adaptation`, changed item visibility, columns, section boundaries, or interaction form may use `native_adaptation` when the exact difference and theme evidence are recorded. Product-state properties may extend the component only after the primary contract remains reproducible.

When a component belongs to a connected composition group, preserve the group's shared container, adjacency, spacing, interaction, and responsive transformation. Multiple semantic components may exist internally, but they must not render as unrelated page sections.

Add these provenance fields to every strict-reference component contract:

```yaml
structure_source_url:
source_section_id:
source_fingerprint_digest:
theme_capability_url:
theme_section:
theme_blocks: []
theme_settings: {}
theme_setting_evidence: {}
composition_group_id:
topology_signature:
```

Reject the component contract when `structure_source_url` is missing, differs from Build Truth, or points to a theme demo that the user did not select as the structure source.

Reject `exact_native` or `composed_native` when a required Section, Block, or Setting uses a descriptive alias instead of the exact target-theme name or lacks evidence. A topology change is `native_adaptation`, not an exact claim. Do not use `Approved` to bypass this check without approval provenance in the manifest.

## Properties

Use the smallest useful API:

```text
TEXT         editable labels and content
BOOLEAN      optional labels, badges, icons, proof, helper text
INSTANCE_SWAP replaceable icon/media/content subcomponent
VARIANT      size, style, state, and only necessary viewport differences
```

Avoid exposing every visual detail as a variant. UI should be able to update content and common states without detaching the instance.
