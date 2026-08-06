# Figma QA Checklist

## File and naming

- Expected pages and root frames exist.
- No duplicate generated pages/components.
- No unexplained unnamed layers.
- Node IDs in the manifest still resolve.

## Foundations

- Required variables and styles exist.
- Semantic variables alias primitives where planned.
- Colors, spacing, radii, typography, and effects are not unnecessarily hardcoded.
- The intended product font is actually used.
- Every client-facing Text node is bound to an approved Text Style; target 100%.

## Components

- Repeated elements are component instances or documented exceptions.
- Component properties remain editable.
- Variants have purposeful axes and no excessive matrix.
- Icons/media use suitable instance-swap or replaceable structures.
- Instances are not detached without a documented reason.

## Layout

- Layout containers are Frames with Auto Layout where appropriate.
- HUG/FILL/FIXED behavior is deliberate.
- Text is not clipped.
- Elements do not overlap unexpectedly.
- Image crops and aspect ratios are usable.
- Applied grid edges and spans differ by no more than 1 px.
- Same-row comparison or decision cards are equal height unless intentional asymmetry is documented.
- Section height uses HUG plus tokenized padding where possible; fixed heights have a reference-backed reason.
- Grid rows have no unexplained remainder space caused by manually rounded widths.

## Responsive

- Desktop and Mobile frames both exist.
- Mobile hierarchy is intentionally adapted, not merely scaled.
- Navigation, touch targets, text sizing, wrapping, and stacking are practical.
- A Mobile child is not wider than its viewport unless an evidenced native interaction requires it.
- Carousels define viewport, card width, gap, next-card preview, indicator or controls, and swipe behavior.
- Clipping is intentional and does not cut the active card.

## Content and assets

- Temporary layers use `Placeholder /` names and are recorded in the manifest.
- The client preview uses presentable sample content; visible internal placeholder instructions do not dominate the composition.
- Unapproved factual claims are not presented as final.
- Competitor/reference imagery is not presented as customer-owned production material.
- Missing content and replacement responsibility are recorded.

## Platform feasibility

- Every theme-based section maps to an exact documented theme section/block and evidence URL.
- Implementation levels use theme-native, configuration, style, custom CSS, custom Liquid, section-custom, or custom.
- Shopify/WordPress implementation risks are visible.
- Theme-based designs do not silently exceed known theme constraints.
- `template` routes contain no unapproved custom Liquid, section-custom, or custom sections.
- `theme_customization` routes keep section-custom and custom work at or below 20% of both section count and estimated page height unless explicitly approved.

## Client preview separation

- No visible `THEME NATIVE`, `SECTION CUSTOM`, `CONFIGURATION`, source-warning, or replacement-instruction labels appear inside client-preview frames.
- Implementation notes and placeholder provenance live in the manifest or project/handoff documentation.
- Customer screenshots are exported only from client-preview frames.

## Blocking result

Mark QA blocked when any of these fail:

- Theme evidence or mapping.
- Route custom budget.
- Text-style binding.
- Grid and equal-height integrity.
- Mobile clipping or carousel contract.
- Client-preview separation.
