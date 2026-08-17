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
GRID_SPAN     columns occupied in each recorded breakpoint state
WIDTH_MODE    FILL, FIXED, or HUG with reason
HEIGHT_MODE   equal-height, content-height, or intentional mixed-height
OVERFLOW      none, wrap, carousel, scroll, or clip with an explicit interaction
THEME_MAP     exact native section/block name and evidence
PRODUCT_STATES product archetypes and optional/required content states validated
REFERENCE_MAP source responsibility and layout anatomy preserved or adapted
VISUAL_DIRECTION typography, imagery, density, spacing, media/content relationship, and responsive rules inherited
FIDELITY_PROFILE theme_adaptation or not_applicable
MAPPING_STATUS exact_native, composed_native, native_adaptation, requires_custom, or unresolved
SOURCE_MAP    stable source section ID and exact source item order
CONTENT_BINDINGS source text/media/control/repeated-item slots mapped one by one
THEME_SETTINGS exact section/block settings supported by theme evidence
RESPONSIVE_SECTION stable shared Section identity and paired breakpoint instance IDs
LAYOUT_CLASS  shared layout family plus Desktop and Mobile state match status
COMPOSITION_GROUP connected source region that must remain visually or interactively continuous
TOPOLOGY normalized major-region bounds, media ratios, repetition, interaction, and responsive transformation
SETTING_EVIDENCE exact evidence for every theme setting used
```

- Use equal-height siblings for cards in the same comparison or decision row unless the blueprint documents intentional asymmetry.
- Prefer FILL or grid-derived widths over manually rounded widths.
- Assign every major edge to a foundation `alignment_group_id`; paired instances must use the group defined for their breakpoint.
- A carousel must define viewport width, card width, gap, visible next-card preview, controls or indicator, and theme-supported behavior.
- Do not use clipping to hide a card that is wider than the Mobile content grid.
- Reject any child overflow inside a clipping parent unless `OVERFLOW` names an evidenced interaction and affordance.
- Keep shared copy, controls, content bindings, Section order, and component identity equal across viewport variants. A viewport variant may change only fields listed by the Responsive Section Contract.
- Define the collapse behavior when product-specific content is absent; empty modules must not leave reserved blank height.
- Reject a component whose generic visual grammar overrides the approved representative composition even when its content slots are technically compatible.

Every active component family must also satisfy the Component Library Presentation Contract. Structural validity does not excuse loose canvas placement, misaligned family rows, inconsistent variant order, overlapping component sets, or stale empty component-set bounds.

For selected competitor-module work, the contract must preserve each selected module's visible content slots, local ordering, critical function, and responsive reading flow through one shared Section identity. Changed item visibility, columns, section boundaries, or interaction form may use `native_adaptation` when the exact difference and theme evidence are recorded; otherwise name the scoped custom implementation. Product-state properties may extend the component only after the selected module contract remains reproducible.

When a component belongs to a connected composition group, preserve the group's shared container, adjacency, spacing, interaction, and responsive transformation. Multiple semantic components may exist internally, but they must not render as unrelated page sections.

Add these provenance fields to every selected competitor-module component contract:

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

Reject the component contract when `structure_source_url` is missing, differs from the selected module's recorded source, or points to a theme demo that the user did not select as that module's structure source.

Reject `exact_native` or `composed_native` when a required Section, Block, or Setting uses a descriptive alias instead of the exact target-theme name or lacks evidence. A topology change is `native_adaptation`, not an exact claim. Do not use `Approved` to bypass this check without approval provenance in the manifest.

## Properties

Use the smallest useful API:

```text
TEXT         editable labels and content
BOOLEAN      optional labels, badges, icons, proof, helper text
INSTANCE_SWAP replaceable icon/media/content subcomponent
VARIANT      size, style, state, and only necessary evidenced viewport differences
```

Avoid exposing every visual detail as a variant. UI should be able to update content and common states without detaching the instance.
