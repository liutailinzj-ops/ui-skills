# Layout Topology Contract

Use this contract whenever a page or section must preserve a specified reference structure. It records how content is composed, not only which topics appear.

## Source capture

Record one topology object for every stable source section and one composition-group object for source regions that behave as a single experience.

```yaml
composition_groups:
  - group_id: G01
    purpose:
    member_section_ids: []
    boundary_behavior: continuous | visually_connected | independent
    may_split_in_target: false
    split_evidence:
    approved_split_deviation:
sections:
  - source_id: R01
    viewport: desktop | mobile
    source_viewport_width:
    section_bounds_normalized: {x: 0, y: 0, width: 1, height_in_viewports: 1}
    container_width_ratio:
    layout_family:
    major_regions:
      - region_id:
        role:
        normalized_bounds: {x: 0, y: 0, width: 1, height: 1}
        alignment:
        content_order:
    grid: {columns: null, rows: null, gap_ratio: null}
    media: {aspect_ratios: [], crop: null, position: null}
    repetition: {total_items: null, visible_items: null, wrapping: null}
    interaction:
      type: none | carousel | scroll | tabs | accordion | sticky | hotspot | video
      viewport_behavior:
      controls: []
      overflow: none | clip | scroll | visible
    responsive_transformation:
    evidence: observed | inferred | unavailable
```

Use normalized geometry so the comparison remains valid when source and target frame widths differ. Capture major regions and interaction viewports; do not trace decorative pixels.

## Composition groups

Create a composition group when adjacent source areas share one transaction, navigation, comparison, or narrative flow and splitting them would change the experience. A common ecommerce example is a product media, product information, options, purchase controls, and directly attached add-ons region, but never assume this grouping without observing it.

- Preserve group membership, order, connected spacing, and shared interaction.
- Do not convert one connected source group into unrelated full-width sections merely because the target theme exposes separate semantic modules.
- Split a group only when target-theme evidence proves the same rendered topology or an explicit deviation is approved.
- Do not infer a fixed number of sections, cards, tabs, products, or content modules from another benchmark.

## Match rules

For strict `reference_to_theme`, require all of the following unless an approved deviation names the exact difference:

- Major-region count, reading order, grouping, and media/content placement match.
- Desktop and Mobile layout families and responsive transformations match.
- Repeated-item total and initially visible counts match.
- Interaction type, viewport, overflow, controls, and sticky behavior match.
- Major normalized region x and width differ by no more than `0.02`; y and height differ by no more than `0.05` after accounting for approved theme container settings and content reflow. Use a stricter source-observed value when a fixed interaction depends on it.
- Media aspect ratio differs by no more than `5%`.
- A `continuous` or `visually_connected` composition group remains connected.

For `structure_target`, use the same fields but allow a documented product-, theme-, scope-, or responsive-driven adaptation. Semantic responsibility coverage alone never proves a topology match.

For `theme_adaptation`, use priority-aware comparison:

- `critical`: purchase, inquiry, navigation, comparison, legally required, and indispensable interaction/content responsibilities need a functional equivalent and cannot be silently lost.
- `structural`: section order, composition membership, major regions, and reading flow should be preserved; an evidenced native alternative is allowed when the difference is named.
- `presentational`: exact columns, initially visible counts, normalized dimensions, spacing, crop, and decorative treatment may adapt to the theme when content and function remain intact.

Do not apply strict numerical topology tolerances as a production blocker to a `native_adaptation`. Record the measured difference and review it visually instead.

## Evidence and unknowns

- Mark values `observed`, `inferred`, or `unavailable`.
- Do not claim exact fidelity from `inferred` or `unavailable` geometry.
- If Desktop or Mobile evidence is unavailable, exact conversion is blocked for that viewport.
- Placeholder assets may replace source media, but they must retain the recorded aspect ratio, crop role, density, and composition. Generic placeholder cards or black rectangles must not redefine the layout.

## Topology signature

Persist a concise production topology contract for downstream design and implementation continuity:

```yaml
topology_signature:
  composition_groups: []
  ordered_sections: []
  section_layout_families: {}
  major_region_bounds: {}
  repeated_item_counts: {}
  interaction_contracts: {}
  desktop_mobile_transformations: {}
```

An output that preserves section topics but changes this contract is a structural mismatch unless the production mapping records an allowed adaptation or approved deviation.
