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

## Editability

- Do not flatten sections.
- Do not use a full-page screenshot as the final design.
- Keep text as Text nodes.
- Keep images as replaceable fills or component properties.
- Keep repeated content as instances.
- Preserve clear section boundaries for Shopify Sections or WordPress Blocks.

## Responsive behavior

- Desktop and Mobile are independent final frames.
- Reorder, simplify, stack, or hide content based on priority rather than uniformly scaling.
- Ensure touch targets, text size, image crops, and navigation behavior remain practical.

