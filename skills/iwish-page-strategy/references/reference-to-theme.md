# Reference-to-Theme Conversion

Use this low-freedom workflow only when the reference page's visible content inventory, section order, and Desktop/Mobile layout anatomy are approved targets.

## 1. Capture the Source

Inspect the rendered source page at Desktop and Mobile widths. Use DOM/accessibility content when available and screenshots as visual evidence. If either viewport cannot be inspected, block exact conversion.

Before section capture, create a Source Identity Fingerprint from the exact specified structure-source URL:

```yaml
source_identity:
  canonical_url:
  page_type:
  product_or_service_name:
  product_category:
  h1:
  hero_signature:
  stable_section_labels: []
  desktop_layout_signature:
  mobile_layout_signature:
```

Copy this fingerprint into the Source Page Specification, Theme Assembly Plan, build manifest, and QA report. If the URL, product/category, H1, hero, or section sequence describes the theme demo or another site instead, stop as `blocked_source_identity`. Do not start mapping.

Create stable IDs `R01`, `R02`, and so on in rendered order. Capture headers, announcement bars, product information, below-fold sections, recommendations, and footer when they are in scope.

For each source section record:

```yaml
- source_id: R01
  order: 1
  visible_text: []
  media_roles: []
  controls: []
  repeated_items: []
  content_item_count:
  desktop:
    layout_class:
    columns:
    media_position:
    alignment:
    width_behavior:
    interaction:
  mobile:
    layout_class:
    order:
    stacking:
    interaction:
```

Use layout classes such as `single_column`, `split_media_content`, `gallery_purchase_split`, `card_grid`, `carousel`, `accordion`, `tabbed`, and `full_bleed_media` consistently. Record actual visible content; do not replace it with a semantic summary.

Reference text and media may be temporary design evidence only when authorized. Record provenance and replacement responsibility. Never represent competitor material as customer-owned or production-approved.

## 2. Build the Theme Assembly Plan

Map every source section in the same order to separate theme capability evidence:

```yaml
- source_id: R01
  target_order: 1
  theme_section:
  theme_blocks: []
  settings:
    container:
    columns:
    media_position:
    alignment:
    spacing:
    color_scheme:
    mobile_behavior:
  content_bindings: []
  mapping_status: exact_native | composed_native | unresolved
  desktop_layout_match: exact | deviation
  mobile_layout_match: exact | deviation
  deviation:
  structure_source_url:
  theme_capability_url:
  evidence_url:
```

- `exact_native`: one evidenced theme section reproduces the source content slots and layout class.
- `composed_native`: two or more evidenced native sections/blocks reproduce one source section without changing visible order or content.
- `unresolved`: the selected route cannot reproduce the section. Stop before Figma.

Do not use `adapted` as an unmeasured success state. A deviation requires explicit approval.

Each row must express `structure_source Rxx -> chosen theme Section/Blocks/Settings`. The `structure_source_url` must match the Source Identity Fingerprint. The `theme_capability_url` and `evidence_url` must prove the chosen target theme primitive. A theme demo row mapped back to the same demo is invalid unless that demo is explicitly the structure source.

## 3. Route Gate

For `template`, allow only evidenced native sections, blocks, configuration, and approved styling/CSS scope. If a mapping is unresolved, return these choices:

1. Accept the named layout/content deviation.
2. Change to a theme with a matching primitive.
3. Approve `theme_customization` or custom implementation.

Do not generate a conventional PDP as a fallback.

## 4. Build Contract

- Build source sections in exact `Rxx` order.
- Use the captured visible content inventory or approved replacements.
- Reproduce Desktop and Mobile layout classes separately.
- Apply the Theme Assembly Plan settings before brand polish.
- Do not add best-practice sections, omit low-value sections, rewrite content hierarchy, or substitute generated creative direction.

## 5. Fidelity Gate

Pass only when:

- Build Truth URL identity is 100%.
- Product/category identity matches the specified structure source.
- Source fingerprint matches across specification, assembly plan, Figma manifest, and QA.
- Source section coverage is 100%.
- Source order match is 100%.
- Visible content-item coverage is 100%.
- Desktop layout-class coverage is 100%.
- Mobile layout-class coverage is 100%.
- Theme mappings contain no `unresolved` item.
- Every deviation is explicitly approved.
- No theme-capability URL was silently promoted to Build Truth.

These checks measure source correspondence, not visual mood or semantic responsibility.

## 6. No-Op Regression Guard

Before rebuilding, record a baseline structure signature: root IDs, ordered section names, Y positions, heights, child counts, and text/content digests. Record expected changed `Rxx` sections from the new Source Page Specification.

After rebuilding, record the same signature. If expected changes exist but the affected section order, geometry, child structure, and content digests remain unchanged, mark the regression `blocked_no_op`. Do not report success based only on a new page name, new matrix, or higher coverage percentage.
