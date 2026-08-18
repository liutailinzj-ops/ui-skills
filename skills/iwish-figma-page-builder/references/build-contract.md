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
- Apply the foundation page gutter, named container mode, and `alignment_group_id` before sizing children. Do not select margins independently inside each Section.
- Align content edges and grid spans to the applied layout grid within 1 px.
- Use equal-height siblings for cards in the same row unless intentional asymmetry is documented in the blueprint.
- Prefer HUG section height with tokenized top and bottom padding. Use a fixed section height only when the reference or interaction requires it.
- Do not leave unexplained remainder space inside a grid row; use FILL or exact grid-derived widths.
- Use Auto Height/HUG for any text that can wrap. A fixed-height Text node is allowed only for a verified single-line label or an intentionally clamped component state.
- After inserting real or placeholder copy, reflow the parent and verify that text bounds do not intersect non-overlay siblings.
- Apply canonical copy, media, controls, and final styles before fixing dependent heights or positions. Read actual rendered bounds after every font/style change; never assume the previous text height remains valid.
- Reject a fixed-height section when its unused vertical band exceeds both 240 px and 25% of section height without a source-backed composition reason.
- Require every normal child bound to remain inside its parent bound. Overflow is allowed only inside a named viewport with explicit `clip`, `scroll`, or `visible` behavior and evidenced controls or affordance.

## Visual direction inheritance

- Inspect the approved representative responsive Section families and breakpoint proof states before building the full page.
- Match their typography hierarchy, color behavior, imagery, media ratios, density, spacing rhythm, control language, and responsive transformation.
- Record a reason when a section needs a different composition; do not silently fall back to a house component.
- Reject repeated black boxes, generic card grids, or a fixed palette/rhythm that is not supported by project evidence.
- Use real or tracked temporary imagery so the result can be judged as UI, not only as information architecture.
- Complete the Visual-Asset Coverage Matrix for every decision-critical media slot. Verify subject, environment, crop, scale, density, and required variation from actual screenshots.
- Reject duplicated generic media when products, configurations, features, or scenes are supposed to differ visually.
- Compare the completed page with the selected seven-dimension visual signature. Typography, first-screen topology, page rhythm, and component grammar require project evidence; construction convenience is not evidence.

## Content preflight

Before creating full-page wrappers:

- Resolve every visible text, media, and control to one stable content-slot ID and `canonical_client_value`.
- Confirm Desktop and Mobile share Section order, slot IDs, and canonical values. Record only exact evidenced content variants.
- Reject any rendered value that contains internal approval, placeholder, implementation, QA, source-warning, test, scope, or replacement instructions.
- Keep status/provenance in manifest fields or internal layer metadata; do not build visible badges or suffixes from them.
- Instantiate one representative responsive-risk Section pair with final content and Text Styles, then inspect actual bounds, wrapping, navigation, repeated items, media crop, and overflow before full-page assembly.
- Validate the full representative set before wrappers: first screen or primary conversion, one semantic-differentiation module, and one imagery-led module. All decision-critical media must use the intended temporary assets rather than empty frames or repeated primitives.

## Page composition preflight

Before creating final preview wrappers:

- Resolve the passed internal page-composition board.
- Verify actual Section order, container modes, alignment groups, color/media distribution, density curve, primary conversion focus, and selected-module positions.
- Confirm the board uses realistic content volume and intended temporary media rather than anonymous blocks.
- Confirm representative Sections fit the complete-page rhythm without forcing unrelated Sections into one repeated grammar.
- Reject final assembly when UI would still need to redesign the first screen, reorder most Sections, redistribute major color/media fields, or choose the page grid.
- Reject a board composed only of anonymous color/density blocks, empty media rectangles, or generic cards. It must expose judgeable media/thumbnail roles, text hierarchy, controls, surfaces, Section order, and approximate final proportions.

## Component-library preflight

- Resolve the component-library root, active categories, family rows, and component sets.
- Verify Auto Layout, shared origins, row/category alignment within 1 px, top-aligned paired breakpoint variants, consistent variant ordering, tight set bounds, and no overlap.
- Do not assemble the page from a library that UI must first rearrange.

## Editability

- Do not flatten sections.
- Do not use a full-page screenshot as the final design.
- Keep text as Text nodes.
- Keep images as replaceable fills or component properties.
- Keep repeated content as instances.
- Preserve clear section boundaries for Shopify Sections or WordPress Blocks.
- Bind every client-facing text node to an approved text style.
- Keep visible implementation labels, replacement warnings, and internal source notes outside client-preview frames.
- Keep visible node values equal to the canonical customer-visible ledger; internal layer names may retain `Placeholder /` without changing rendered content.

## Responsive behavior

- Desktop and Mobile are paired breakpoint previews of the same responsive page, Section identities, component families, order, and shared content bindings.
- Build the shared Section family once. Use the smallest necessary viewport variants or Auto Layout states, then place paired instances in the preview frames.
- Keep customer-facing copy and controls identical by default. Do not rewrite headings, body text, labels, or CTAs by viewport unless the Responsive Section Contract records an evidenced content variant.
- Reorder, simplify, stack, change columns, alter crop, or change interaction only when listed in the Responsive Section Contract. For theme-based work, the difference must come from documented theme settings or observed automatic theme behavior.
- Do not detach one viewport instance or replace it with an unrelated composition.
- Ensure touch targets, text size, image crops, and navigation behavior remain practical.
- Do not clip content accidentally. Any child outside a clipping parent blocks the Section unless a named evidenced overflow contract requires it.
- For carousels, define viewport width, card width, gap, next-card preview, indicator or controls, and intended swipe behavior. A clipped card alone is not a carousel.

## Theme feasibility and customization freedom

- Use the exact section/block mapping approved in the Theme Capability Map.
- Use exact target-theme Section, Block, and Setting names with field-level evidence. Descriptive or generated aliases are not mappings.
- Keep layout, ordering, controls, and responsive behavior within documented theme settings only for rows classified as native/configured. For style, CSS, Liquid, or new-Section rows, follow the recorded scoped implementation contract.
- Record every visual divergence and its implementation level.
- Choose the least complex feasible route that preserves the approved design responsibility. Do not auto-promote a Section to custom for convenience, but do not downgrade hierarchy, media relationships, interaction, or responsive behavior merely to stay native. A scoped new Section is valid when contracted development freedom and evidence support it.

## Analysis traceability

- For `research_led`, `hybrid_led`, and `custom_led`, every customer-facing section must trace to Product and Competitor Analysis, a platform responsibility, a selected source module, or an approved project requirement.
- Preserve the visitor question and DTC conversion/B2B buying responsibility recorded in the blueprint.
- Use placeholders for missing proof or content; do not invent factual claims to make the conversion chain appear complete.
- Do not force the entire journey onto one page when the analysis assigns responsibilities to connected pages.

## Reference fidelity

For `selected_structure_modules` with `theme_adaptation`:

- Apply source-section identity, content bindings, composition-group, topology, interaction, and responsive checks only to the explicitly selected modules.
- Build unselected page responsibilities from the approved research-led blueprint; do not import the rest of the source page by default.
- Resolve each selected module independently as theme-native, configured, styled, custom CSS, custom Liquid, new custom Section, app/third-party, or pending engineering confirmation.

## Topology-first build order

For selected competitor-module work, build in this order:

1. Create section and composition-group skeletons with normalized major-region geometry.
2. Create one Responsive Section family and apply evidenced theme container, grid, alignment, overflow, and breakpoint settings. In `theme_adaptation`, use the documented native target values.
3. Bind visible content items and repeated-item counts.
4. Place paired Desktop and Mobile instances and validate them against the same responsive contract; classify each breakpoint state as exact or adapted.
5. Apply brand styling and placeholders without changing geometry.

Do not use a visually polished semantic checklist as a substitute for steps 1–4.

## PDP coverage

- Build one primary client-preview product without hardcoding its content into the template structure.
- Swap or simulate every approved additional product state through component properties and conditional modules.
- Verify long titles, option wrapping, gallery-count differences, absent ratings/proof, content-rich modules, and Mobile stacking when applicable.
- Collapse absent optional modules without blank section height.
- Use multiple product templates only when the blueprint selects `template_family` and theme/platform assignment is evidenced.
- Report `coverage_partial` when the available product evidence cannot support a catalog-wide claim.
- Keep decision-critical purchase responsibilities visible in the primary composition even when final values are unavailable: price and optional compare-at/discount hierarchy, rating present/absent, inventory, shipping, variants/options and wrapping, quantity, purchase actions, and sticky purchase behavior when included. Use neutral sample values tracked as placeholders; never present them as verified facts.

## Complete-page delivery gate

- Representative responsive Section families, the component library, and the page-composition board are preflight artifacts only.
- Complete production requires full Desktop and Mobile customer-preview roots containing the entire approved Section sequence, including applicable header, commerce, content, global, cross-sell, footer, and sticky responsibilities.
- Both roots must be assembled from the same responsive Section/component families and canonical content ledger. Mobile is a breakpoint state, not a separate redesign.
- Capture and inspect both full-page screenshots after assembly. Do not set overall production complete until both preview states pass.
- If the requested scope intentionally stops at exploration, report only `代表性模块预检通过` and keep overall production in progress.

## Section validation gate

Before continuing, verify:

- Desktop and Mobile screenshots are visually complete.
- Every Section appears as paired instances of one recorded responsive component family; shared Section IDs, order, content bindings, controls, and copy match.
- Every breakpoint difference is listed in the Responsive Section Contract and supported by theme evidence or the custom responsive plan.
- Grid edges, equal heights, HUG/FILL/FIXED behavior, and overflow pass.
- Nodes in one alignment group share left and right edges within 1 px; no unexplained fixed-width remainder exists.
- Every multi-line Text node uses Auto Height/HUG or a documented clamp; no text is cropped or overlapping.
- No unexplained sibling bounding-box collision exists outside an intentional overlay container.
- No section contains a source-unjustified blank vertical band larger than 240 px and 25% of its height.
- Media crop/aspect, gallery height, and content-column balance match the recorded source layout class.
- Every decision-critical media slot matches its Visual-Asset Coverage Matrix row; distinct configurations, products, features, and scenes are visually distinguishable.
- Every child is contained by its parent or covered by a named, evidenced overflow contract; no hidden overflow is used to conceal sizing errors.
- Any clipping parent with an out-of-bounds normal child fails, even when the child is visually hidden in the screenshot.
- Composition groups, normalized major-region geometry, repeated-item counts, and interaction viewports match the topology contract.
- Sticky or anchor navigation labels, order, and destinations match the selected module contract when included.
- Text styles and component instances are bound.
- The client preview contains no visible internal annotations.
- Every visible text/media/control node resolves to a declared canonical content-slot ID; no internal metadata or marker is rendered.
- The representative responsive-risk preflight used final styles/content and passed actual-bound, wrapping, crop, repetition, navigation, and overflow checks before full-page assembly.
- Theme mapping still matches the approved capability map.
- Reference responsibility, order, and layout-anatomy correspondence still matches the approved matrix when applicable.
- Selected-module source identity, module fingerprints, selected scope, content items, composition groups, local order, topology, and exact evidenced theme settings still match the approved specifications when applicable.
- PDP scenario states pass without detaching components, clipping content, or leaving empty modules when applicable.
- Analysis-backed page responsibilities remain represented, and selected-module gaps are explicitly reported.
