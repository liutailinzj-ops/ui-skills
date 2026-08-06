# Build Contract

## Naming

```text
Page / {Page Name} / Desktop
Page / {Page Name} / Mobile
Section / {Section Name}
Content / {Purpose}
Component / {Component Name}
Placeholder / {Content Type}
```

## Layout

- Use Frame nodes, not Group nodes, for layout structure.
- Use Auto Layout for normal content flow.
- Set HUG, FILL, and FIXED deliberately after parenting nodes.
- Use absolute positioning only for intentional decoration or overlap.
- Keep containers, grids, padding, and section spacing traceable to foundations.
- Align content edges and grid spans to the applied layout grid within 1 px.
- Use equal-height siblings for cards in the same row unless intentional asymmetry is documented in the blueprint.
- Prefer HUG section height with tokenized top and bottom padding. Use a fixed section height only when the reference or interaction requires it.
- Do not leave unexplained remainder space inside a grid row; use FILL or exact grid-derived widths.

## Editability

- Do not flatten sections.
- Do not use a full-page screenshot as the final design.
- Keep text as Text nodes.
- Keep images as replaceable fills or component properties.
- Keep repeated content as instances.
- Preserve clear section boundaries for Shopify Sections or WordPress Blocks.
- Bind every client-facing text node to an approved text style.
- Keep visible implementation labels, replacement warnings, and internal source notes outside client-preview frames.

## Responsive behavior

- Desktop and Mobile are independent final frames.
- Reorder, simplify, stack, or hide content based on priority rather than uniformly scaling.
- Ensure touch targets, text size, image crops, and navigation behavior remain practical.
- Do not clip content accidentally. A card may not be wider than its Mobile viewport unless an evidenced native interaction requires it.
- For carousels, define viewport width, card width, gap, next-card preview, indicator or controls, and intended swipe behavior. A clipped card alone is not a carousel.

## Theme fidelity

- Use the exact section/block mapping approved in the Theme Capability Map.
- Keep layout, ordering, controls, and responsive behavior within documented theme settings.
- Record every visual divergence and its implementation level.
- Stop the build when a section would cross the approved route budget; do not auto-promote it to custom.

## Reference fidelity

For `structure_target`:

- Build from the Reference Content-Layout Matrix, not visual memory.
- Preserve every relevant source responsibility or record an omission.
- Preserve section order unless the blueprint records a product, theme, responsive, or scope reason to change it.
- Compare layout anatomy: column ratio, media/content placement, grouping, repeated item count, interaction, and Mobile transformation.
- Do not count matching colors or section names as structural fidelity.

For `reference_to_theme`:

- Build from the Source Page Specification and Theme Assembly Plan, never from a generic PDP pattern or visual memory.
- Preserve every stable source section ID, exact section order, visible content item and repeated-item count.
- Match the recorded Desktop and Mobile layout class, media/content placement, grouping, controls, and responsive transformation.
- Use only `exact_native` or `composed_native` mappings. Any `unresolved` mapping blocks the build.
- Apply the recorded theme section, blocks, and concrete setting values. Do not invent settings unsupported by evidence.
- Require 100% section-count, order, content-item, Desktop layout-class, Mobile layout-class, and resolved-mapping coverage unless the manifest contains a named approved deviation.
- Do not add, omit, reorder, rewrite, or redesign source content under the label of adaptation.

## Regression no-op guard

Before mutation, record a baseline signature containing root IDs, stable section IDs/order, section Y positions and heights, child counts, and text/content digests. Record the same fields after the build.

If the regression declares expected changed sections but the affected order, geometry, child tree, and content digests are unchanged, return `blocked_no_op`. A new page name, new coverage report, or newly created wrapper does not prove that the requested design changed.

## PDP coverage

- Build one primary client-preview product without hardcoding its content into the template structure.
- Swap or simulate every approved additional product state through component properties and conditional modules.
- Verify long titles, option wrapping, gallery-count differences, absent ratings/proof, content-rich modules, and Mobile stacking when applicable.
- Collapse absent optional modules without blank section height.
- Use multiple product templates only when the blueprint selects `template_family` and theme/platform assignment is evidenced.
- Report `coverage_partial` when the available product evidence cannot support a catalog-wide claim.

## Section validation gate

Before continuing, verify:

- Desktop and Mobile screenshots are visually complete.
- Grid edges, equal heights, HUG/FILL/FIXED behavior, and overflow pass.
- Text styles and component instances are bound.
- The client preview contains no visible internal annotations.
- Theme mapping still matches the approved capability map.
- Reference responsibility, order, and layout-anatomy correspondence still matches the approved matrix when applicable.
- `reference_to_theme` source sections, content items, order, layout classes, and exact theme settings still match the approved specifications when applicable.
- The regression result signature contains actual changes for every expected changed section; otherwise it is `blocked_no_op`.
- PDP scenario states pass without detaching components, clipping content, or leaving empty modules when applicable.
