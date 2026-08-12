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
- Multi-line or variable-content Text uses Auto Height/HUG; fixed-height text is limited to verified single-line labels or documented clamps.
- Elements do not overlap unexpectedly.
- Every normal child bound is contained by its parent bound. A child may exceed only a named overflow viewport whose clip, scroll, or visible behavior and affordance are documented.
- Non-overlay sibling bounding boxes do not intersect after text reflow. Intentional overlays live in a named overlay container and remain legible.
- Image crops and aspect ratios are usable.
- Applied grid edges and spans differ by no more than 1 px.
- Nodes in one named alignment group share left and right edges within 1 px at the same breakpoint.
- Section gutters and container widths use foundation-defined modes; any exception has theme or project evidence.
- Same-row comparison or decision cards are equal height unless intentional asymmetry is documented.
- Section height uses HUG plus tokenized padding where possible; fixed heights have a reference-backed reason.
- A fixed-height section has no unexplained unused vertical band larger than both 240 px and 25% of section height.
- Media and content columns have a source-backed height/aspect balance; galleries do not continue far below an otherwise empty primary media area without evidence.
- Grid rows have no unexplained remainder space caused by manually rounded widths.

## Visual direction inheritance

- Major sections visibly inherit the approved typography, colors, imagery, density, spacing rhythm, media/content relationship, control language, and responsive behavior.
- Representative responsive Section families and the completed breakpoint previews use the same project-specific visual grammar.
- Repeated black boxes, generic card grids, default accent colors, or fixed long-page rhythms are not used without project evidence.
- A technically complete wireframe is not reported as a client-ready UI draft.
- Temporary imagery preserves the intended crop, product scale, density, and composition quality.

## Responsive

- Desktop and Mobile preview frames both exist as states of one responsive page system.
- Every paired Section keeps the same stable identity, order, component family, content bindings, controls, and shared copy.
- Mobile behavior is derived from the Responsive Section Contract, not independently redesigned or merely scaled.
- Every breakpoint difference is listed and supported by theme evidence or the custom responsive plan.
- Navigation, touch targets, text sizing, wrapping, and stacking are practical.
- A Mobile child is not wider than its viewport unless an evidenced native interaction requires it.
- Carousels define viewport, card width, gap, next-card preview, indicator or controls, and swipe behavior.
- Clipping is intentional and does not cut the active card.
- A clipping parent has no out-of-bounds normal child unless an explicit overflow contract names that relationship and affordance.
- Customer-facing headings, body copy, labels, and CTAs do not differ across breakpoints without an evidenced content variant.

## Content and assets

- Temporary layers use `Placeholder /` names and are recorded in the manifest.
- The client preview uses presentable sample content; visible internal placeholder instructions do not dominate the composition.
- Unapproved factual claims are not presented as final.
- Competitor/reference imagery is not presented as customer-owned production material.
- Missing content and replacement responsibility are recorded.

## Platform feasibility

- Every theme-based section maps to an exact documented theme section/block and evidence URL.
- Every required setting uses its exact target-theme name and has field-level editor, vendor-documentation, or current-theme evidence. Demo observation alone does not prove an editable setting.
- Implementation levels use theme-native, configuration, style, custom CSS, custom Liquid, section-custom, app/third-party, custom, or pending-engineering.
- Shopify/WordPress implementation risks are visible.
- Theme-based designs do not silently exceed known theme constraints.
- Production contains no `template` route; theme-based work is classified as `theme_customization`.
- Every theme-customization Section has an implementation level and scope status. Custom work follows the contracted scope or named engineering estimate, not a universal percentage.

## Product, competitor, and journey analysis

- Product model, competitor matrix, and DTC conversion chain or B2B buying path exist.
- Decision-critical statements distinguish customer facts, research observations, inferences, unknowns, and placeholders.
- Each section traces to a visitor question, journey responsibility, selected source module, platform responsibility, or approved requirement.
- Competitor observations explain presentation and conversion logic rather than visual similarity alone.
- The page does not invent proof, reviews, certifications, results, specifications, prices, or guarantees.
- Relevant conversion/buying gaps are reported. Do not fail a page merely because a responsibility belongs on another scoped page.

## Reference fidelity

For selected competitor-module work, verify source roles:

- The report lists the exact 指定结构来源、主题能力来源、竞品研究来源和视觉参考来源 URLs.
- Each selected module's source URL and local signature match its structure-source record.
- Theme store, vendor docs, demo, and current-theme URLs are used only as capability evidence unless explicitly assigned another role.
- No mapping counts a theme demo section mapped back to the same theme demo as source fidelity.

For `selected_structure_modules`:

- Only explicitly selected source modules are checked for source-layout correspondence.
- Selected modules preserve their named content responsibilities, connected boundaries, major layout relationships, interaction, and responsive behavior or document the exact adaptation/custom route.
- Unselected source modules are not treated as required coverage; remaining page Sections trace to product, competitor, and journey research.

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
- No QA heading, status, issue list, Rxx identifier, theme mapping, or internal risk label is visible in a client-preview frame.
- Any visible internal QA content uses Chinese and exists only in the Codex report, internal artifact, `内部检查 / QA`, or a separate internal file.
- If the customer receives the whole Figma file, internal QA is kept in a separate file.

## Blocking result

Mark QA blocked when any of these fail:

- Selected-module source URL, product/category identity, module fingerprint, or source-role integrity.
- A theme-capability source is silently promoted to a selected-module source or self-mapped as proof of correspondence.
- Theme evidence or mapping.
- Missing Product and Competitor Analysis or untraceable generated sections.
- Missing implementation classification, scope status, or required engineering estimate for theme-customization work.
- Text-style binding.
- Grid and equal-height integrity.
- Text Auto Height/HUG, overlap, oversized blank-band, media-balance, or source-navigation integrity.
- Parent-child containment or an undocumented overflow viewport.
- Mobile clipping or carousel contract.
- Missing paired Section identity, unexplained cross-breakpoint content difference, or an unapproved independent viewport composition.
- Alignment-group edge mismatch above 1 px or an unexplained container-width change.
- Client-preview separation.
- Missing or duplicate required selected-module rows, unexplained critical-function loss, or a selected-module difference without evidenced native adaptation or a documented custom route.
- A critical `theme_adaptation` row with no feasible evidenced native or approved custom route.
- False PDP universality or failed required product state.

Do not block `theme_adaptation` solely because columns, visible-item count, section boundaries, interaction form, spacing, crop, or micro-layout differ from the source. Those differences must be measured, evidenced, and reported to UI.
