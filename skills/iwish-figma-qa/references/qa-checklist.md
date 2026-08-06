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

## Product, competitor, and journey analysis

- Product model, competitor matrix, and DTC conversion chain or B2B buying path exist.
- Decision-critical statements distinguish customer facts, research observations, inferences, unknowns, and placeholders.
- Each non-strict-reference section traces to a visitor question, journey responsibility, platform responsibility, or approved requirement.
- Competitor observations explain presentation and conversion logic rather than visual similarity alone.
- The page does not invent proof, reviews, certifications, results, specifications, prices, or guarantees.
- Relevant conversion/buying gaps are reported. Do not fail a page merely because a responsibility belongs on another scoped page.
- For strict `reference_to_theme`, analysis gaps are reported without treating unapproved structural additions as repairs.

## Reference fidelity

For `structure_target`:

- Every relevant source section has a target responsibility mapping.
- Required source content types are represented or explicitly unavailable.
- Section order matches or has a documented reason to diverge.
- Desktop and Mobile layout anatomy is preserved or deliberately adapted.
- Theme substitutions and omitted sections have evidence and an owner.
- Visual similarity is not used as a substitute for content/layout correspondence.

For `reference_to_theme`:

- Every stable source section ID exists exactly once in the target.
- Target section order matches the Source Page Specification.
- Every captured visible text, media role, control, and repeated item is bound; item counts match.
- Desktop and Mobile layout classes, media/content placement, grouping, controls, and responsive transformations match.
- Every section uses the exact evidenced theme Section, Blocks, and setting values in the Theme Assembly Plan.
- Mapping status is `exact_native` or `composed_native`; no required item is `unresolved`.
- Every deviation is named and explicitly approved; vague `adapted` status is not accepted.
- Section-count, order, content-item, Desktop layout-class, Mobile layout-class, and resolved-mapping coverage are 100% after approved deviations are accounted for.

## Regression integrity

- Baseline and result structure signatures include root IDs, stable section order, Y positions, heights, child counts, and text/content digests.
- Every declared expected changed section has a real change in geometry, tree, or content.
- If expected changes exist but the affected signatures are unchanged, the result is `blocked_no_op`.
- A new page name, wrapper, matrix, or percentage without a changed target structure is not a successful regression.

## PDP coverage

- Product archetypes and representative/edge states are recorded.
- The primary preview product does not define the only valid content length or module set.
- Long title, variants/options, gallery count, rating/proof absence, optional modules, and Mobile stacking are tested when relevant.
- Optional product-specific modules collapse without empty bands.
- A single base template is called reusable only after scenario validation.
- Multiple templates have evidenced platform/theme assignment support.
- Limited catalog evidence is reported as `coverage_partial`, not universal coverage.

## Client preview separation

- No visible `THEME NATIVE`, `SECTION CUSTOM`, `CONFIGURATION`, source-warning, or replacement-instruction labels appear inside client-preview frames.
- Implementation notes and placeholder provenance live in the manifest or project/handoff documentation.
- Customer screenshots are exported only from client-preview frames.

## Blocking result

Mark QA blocked when any of these fail:

- Theme evidence or mapping.
- Missing Product and Competitor Analysis or untraceable generated sections.
- Route custom budget.
- Text-style binding.
- Grid and equal-height integrity.
- Mobile clipping or carousel contract.
- Client-preview separation.
- Unexplained `structure_target` responsibility, order, or layout divergence.
- Any unresolved or unapproved `reference_to_theme` section, content, order, layout-class, or theme-setting mismatch.
- A `reference_to_theme` fidelity metric below 100% after approved deviations.
- A regression that triggers `blocked_no_op`.
- False PDP universality or failed required product state.
