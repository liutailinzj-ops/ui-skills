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

Create stable IDs `R01`, `R02`, and so on in rendered order. Capture every visible in-scope module, including headings, attached controls, repeated items, headers, announcement bars, product information, below-fold sections, recommendations, and footer. Do not merge multiple visible modules into one semantic summary.

Read [layout-topology-contract.md](layout-topology-contract.md). After the complete `Rxx` list exists, create composition-group IDs `G01`, `G02`, and so on for connected source experiences. Every group lists existing `member_section_ids`; it never replaces an `Rxx` row. Section boundaries must follow rendered composition and interaction, not a semantic content checklist.

For each source section record:

```yaml
- source_id: R01
  composition_group_id:
  order: 1
  visible_text: []
  media_roles: []
  controls: []
  repeated_items: []
  content_item_count:
  priority: critical | structural | presentational
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
  topology:
    container_width_ratio:
    major_regions: []
    normalized_bounds: {}
    media_aspect_ratios: []
    total_item_count:
    initially_visible_item_count:
    overflow_contract:
    responsive_transformation:
  topology_evidence: observed | inferred | unavailable
```

Use layout classes such as `single_column`, `split_media_content`, `gallery_purchase_split`, `card_grid`, `carousel`, `accordion`, `tabbed`, and `full_bleed_media` consistently. Record actual visible content; do not replace it with a semantic summary.

Reference text and media may be temporary design evidence only when authorized. Record provenance and replacement responsibility. Never represent competitor material as customer-owned or production-approved.

## 2. Build the Theme Assembly Plan

Map every source section in the same order to separate theme capability evidence:

```yaml
- source_id: R01
  composition_group_id:
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
  setting_evidence: {}
  content_bindings: []
  mapping_status: exact_native | composed_native | native_adaptation | requires_custom | unresolved
  adaptation_state: not_applicable | proposed_adaptation | approved_adaptation | rejected_adaptation
  desktop_topology_match: exact | deviation | unavailable
  mobile_topology_match: exact | deviation | unavailable
  composed_native_proof:
  deviation:
  structure_source_url:
  theme_capability_url:
  evidence_url:
```

- `exact_native`: one evidenced theme section and its evidenced settings reproduce the source content slots, section boundary, topology, interaction, and responsive transformation.
- `composed_native`: two or more evidenced native sections/blocks reproduce one source section at the requested fidelity profile.
- `native_adaptation`: an evidenced native substitute preserves content bindings, critical function, and reading order but changes a documented non-critical topology or interaction detail.
- `requires_custom`: the requested higher-fidelity form needs custom code. Record the estimated route/budget and the best evidenced native fallback.
- `unresolved`: evidence is insufficient or no feasible native/custom route is known. A critical unresolved row blocks.

Do not use vague `adapted` as an unmeasured success state. A `native_adaptation` must name the exact difference, preserved responsibility, evidence, consequence, and UI owner.

Each row must express `structure_source Rxx -> chosen theme Section/Blocks/Settings`. The `structure_source_url` must match the Source Identity Fingerprint. The `theme_capability_url` and `evidence_url` must prove the chosen target theme primitive. A theme demo row mapped back to the same demo is invalid unless that demo is explicitly the structure source.

Every claimed setting must have field-level evidence from the target theme editor, vendor documentation, or an inspectable current theme. Marketing copy or visual similarity may establish a candidate, but cannot prove an exact setting. Use the exact published Section and Block names; descriptive labels such as `approved composition`, `static prototype`, or `native-like` are invalid mappings.

For each `composed_native` row, record the contributing native primitives, their rendered adjacency, shared container and spacing behavior, interaction continuity, and Mobile transformation. In `strict_replication`, changed source geometry is unresolved unless approved. In `theme_adaptation`, it may become `native_adaptation` when critical function and reading flow remain intact.

Record approval only as:

```yaml
adaptation_decision:
  status: proposed_adaptation | approved_adaptation | rejected_adaptation
  exact_difference:
  approved_by:
  approval_source:
  approved_at:
```

Do not infer approval from a prompt, generated report, layer name, or previous output unless it contains an explicit decision about that exact difference.

## 3. Route Gate

For `template`, allow only evidenced native sections, blocks, configuration, and approved styling/CSS scope.

- In `theme_adaptation`, use `exact_native`, `composed_native`, or `native_adaptation` and continue to Figma. If higher fidelity would require custom code, keep that route as an optional engineering note and build the best evidenced native fallback.
- In `strict_replication`, if a mapping remains unresolved or requires unapproved custom work, return these choices:

1. Accept the named layout/content deviation.
2. Change to a theme with a matching primitive.
3. Approve `theme_customization` or custom implementation.

Do not generate a conventional unrelated page as a fallback. A native adaptation must still trace every relevant `Rxx` row and content item.

## 4. Build Contract

- Build source sections in stable `Rxx` order. A production adaptation may realize one source row with adjacent native primitives, but each row remains traceable exactly once.
- Preserve every composition group and its connected boundary behavior.
- Use the captured visible content inventory or approved replacements.
- Reproduce Desktop and Mobile topology separately. In `theme_adaptation`, preserve critical regions and reading flow while documenting permitted native differences in proportions, visible-item counts, overflow, controls, or transformation.
- Apply the Theme Assembly Plan settings before brand polish.
- Do not add best-practice sections, omit low-value sections, rewrite content hierarchy, or substitute generated creative direction.

## 5. Fidelity Gate

Source capture passes only when:

- Build Truth URL identity is 100%.
- Product/category identity matches the specified structure source.
- Source fingerprint matches across specification, assembly plan, Figma manifest, and QA.
- Source section coverage is 100%.
- Source order match is 100%.
- Visible content-item coverage is 100%.
- Every `Rxx` is unique and mapped exactly once.
- Every composition group references existing `Rxx` members and does not replace them.

For `strict_replication`, fidelity passes only when:

- Composition-group coverage is 100%.
- Desktop topology coverage is 100%.
- Mobile topology coverage is 100%.
- Theme mappings contain no `unresolved` item.
- Every deviation has explicit approval provenance.
- No theme-capability URL was silently promoted to Build Truth.

For `theme_adaptation`, completion requires:

- Critical responsibility and content coverage are 100%.
- Every non-exact row has an evidenced `native_adaptation`, feasible approved custom route, or explicit omission decision.
- Exact and adapted Desktop/Mobile topology results are reported separately.
- Proposed adaptations are listed for UI review and are not represented as approved.
- Figma build and QA statuses are reported independently from theme-mapping fidelity.

These checks measure source correspondence, not visual mood or semantic responsibility.

## 6. No-Op Regression Guard

Before rebuilding, record a baseline structure signature: root IDs, ordered section names, Y positions, heights, child counts, and text/content digests. Record expected changed `Rxx` sections from the new Source Page Specification.

After rebuilding, record the same signature plus the topology signature from [layout-topology-contract.md](layout-topology-contract.md). If expected changes exist but the affected section order, geometry, child structure, content digests, and topology remain unchanged, mark the regression `blocked_no_op`. Do not report success based only on a new page name, new matrix, or higher coverage percentage.
