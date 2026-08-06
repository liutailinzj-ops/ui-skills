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

## Section validation gate

Before continuing, verify:

- Desktop and Mobile screenshots are visually complete.
- Grid edges, equal heights, HUG/FILL/FIXED behavior, and overflow pass.
- Text styles and component instances are bound.
- The client preview contains no visible internal annotations.
- Theme mapping still matches the approved capability map.
