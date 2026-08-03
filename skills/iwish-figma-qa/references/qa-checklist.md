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

## Responsive

- Desktop and Mobile frames both exist.
- Mobile hierarchy is intentionally adapted, not merely scaled.
- Navigation, touch targets, text sizing, wrapping, and stacking are practical.

## Content and assets

- Temporary content uses `Placeholder /` labels.
- Unapproved factual claims are not presented as final.
- Competitor/reference imagery is not presented as customer-owned production material.
- Missing content and replacement responsibility are recorded.

## Platform feasibility

- Sections are labeled theme-native, configuration, style, section-custom, or custom where relevant.
- Shopify/WordPress implementation risks are visible.
- Theme-based designs do not silently exceed known theme constraints.

