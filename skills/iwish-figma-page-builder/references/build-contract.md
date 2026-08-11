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
- Reject a fixed-height section when its unused vertical band exceeds both 240 px and 25% of section height without a source-backed composition reason.
- Require every normal child bound to remain inside its parent bound. Overflow is allowed only inside a named viewport with explicit `clip`, `scroll`, or `visible` behavior and evidenced controls or affordance.

## Visual direction inheritance

- Inspect the approved representative responsive Section families and breakpoint proof states before building the full page.
- Match their typography hierarchy, color behavior, imagery, media ratios, density, spacing rhythm, control language, and responsive transformation.
- Record a reason when a section needs a different composition; do not silently fall back to a house component.
- Reject repeated black boxes, generic card grids, or a fixed palette/rhythm that is not supported by project evidence.
- Use real or tracked temporary imagery so the result can be judged as UI, not only as information architecture.

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

- Desktop and Mobile are paired breakpoint previews of the same responsive page, Section identities, component families, order, and shared content bindings.
- Build the shared Section family once. Use the smallest necessary viewport variants or Auto Layout states, then place paired instances in the preview frames.
- Keep customer-facing copy and controls identical by default. Do not rewrite headings, body text, labels, or CTAs by viewport unless the Responsive Section Contract records an evidenced content variant.
- Reorder, simplify, stack, change columns, alter crop, or change interaction only when listed in the Responsive Section Contract. For theme-based work, the difference must come from documented theme settings or observed automatic theme behavior.
- Do not detach one viewport instance or replace it with an unrelated composition.
- Ensure touch targets, text size, image crops, and navigation behavior remain practical.
- Do not clip content accidentally. Any child outside a clipping parent blocks the Section unless a named evidenced overflow contract requires it.
- For carousels, define viewport width, card width, gap, next-card preview, indicator or controls, and intended swipe behavior. A clipped card alone is not a carousel.

## Theme fidelity

- Use the exact section/block mapping approved in the Theme Capability Map.
- Use exact target-theme Section, Block, and Setting names with field-level evidence. Descriptive or generated aliases are not mappings.
- Keep layout, ordering, controls, and responsive behavior within documented theme settings.
- Record every visual divergence and its implementation level.
- Do not auto-promote a section to custom. In `theme_adaptation`, use the best evidenced native fallback when higher fidelity crosses the route budget, and record the optional custom route. Stop only when the critical function itself cannot be represented or an explicit exact requirement needs a route decision.

## Analysis traceability

- For `research_led`, `hybrid_led`, and `existing_site_led`, every customer-facing section must trace to Product and Competitor Analysis, a platform responsibility, or an approved project requirement.
- Preserve the visitor question and DTC conversion/B2B buying responsibility recorded in the blueprint.
- Use placeholders for missing proof or content; do not invent factual claims to make the conversion chain appear complete.
- Do not force the entire journey onto one page when the analysis assigns responsibilities to connected pages.
- For strict `reference_to_theme`, report analysis gaps without adding or reordering source sections unless a deviation is approved.

## Reference fidelity

For `structure_target` with `theme_adaptation`:

- Build from the Reference Content-Layout Matrix, not visual memory.
- Preserve every unique relevant `Rxx` row, content binding, and critical responsibility; missing final material uses placeholders rather than omission.
- Preserve section order unless the blueprint records a product, theme, responsive, or scope reason to change it.
- Compare layout anatomy: column ratio, media/content placement, grouping, repeated item count, interaction, and Mobile transformation. Name evidenced native differences as `native_adaptation` and continue.
- Do not count matching colors or section names as structural fidelity.

For `strict_replication`:

- Verify the Build Truth URL, product/category identity, H1, hero signature, and stable section sequence before creating wrapper frames.
- Build from the Source Page Specification and Theme Assembly Plan, never from a generic PDP pattern or visual memory.
- Preserve every stable source section ID, exact section order, visible content item and repeated-item count.
- Match the recorded Desktop and Mobile topology: composition groups, major-region normalized bounds, media/content placement, item and visible-item counts, grouping, controls, overflow, and responsive transformation.
- Use only `exact_native` or `composed_native` mappings. Any `unresolved` mapping blocks the build.
- Treat `composed_native` as valid only when evidenced native primitives render as one source section with matching topology; semantic coverage across separate generic sections fails.
- Apply the recorded theme section, blocks, and concrete setting values. Do not invent settings unsupported by evidence.
- Preserve provenance in the manifest: source content and order come from `structure_source_url`; Section/Block/Settings feasibility comes from `theme_capability_url`. Do not substitute theme-demo content or map a demo section back to itself.
- Require 100% section-count, order, content-item, composition-group, Desktop topology, Mobile topology, and resolved-mapping coverage unless the manifest contains a deviation with explicit approval provenance.
- Do not add, omit, reorder, rewrite, or redesign source content under the label of adaptation.
- Do not place `Approved` in a layer name or implementation note unless the manifest contains approval provenance for the exact deviation.

## Topology-first build order

For all specified-structure work, build in this order:

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
- Every child is contained by its parent or covered by a named, evidenced overflow contract; no hidden overflow is used to conceal sizing errors.
- Any clipping parent with an out-of-bounds normal child fails, even when the child is visually hidden in the screenshot.
- Composition groups, normalized major-region geometry, repeated-item counts, and interaction viewports match the topology contract.
- Sticky or anchor navigation labels, order, and destinations match the specified structure source when included.
- Text styles and component instances are bound.
- The client preview contains no visible internal annotations.
- Theme mapping still matches the approved capability map.
- Reference responsibility, order, and layout-anatomy correspondence still matches the approved matrix when applicable.
- `reference_to_theme` Build Truth identity, source fingerprint, source sections, content items, composition groups, order, topology, and exact evidenced theme settings still match the approved specifications when applicable.
- PDP scenario states pass without detaching components, clipping content, or leaving empty modules when applicable.
- Analysis-backed page responsibilities remain represented, or strict-reference gaps are explicitly reported.
