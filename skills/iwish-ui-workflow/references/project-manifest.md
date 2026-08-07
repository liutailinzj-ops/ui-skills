# Project Manifest

Maintain one state object throughout the workflow:

```yaml
project:
  name:
  brand:
  product_category:
  target_market:
  audience_type: dtc | b2b | mixed
  platform: shopify | wordpress
  build_route: template | theme_customization | custom
  strategy_mode: research_led | reference_led | hybrid_led | existing_site_led
scope:
  requested_page:
  features: []
sources:
  customer_facts:
  customer_assets:
  structure_source_urls: []
  theme_capability_urls: []
  competitor_evidence_urls: []
  visual_inspiration_urls: []
  source_role_assignments: {}
theme:
  name:
  preset:
  state: to_be_selected | demo_only | code_available | current_site
  capability_map:
  evidence_urls: []
  custom_section_count_ratio:
  custom_section_height_ratio:
  route_gate: pass | blocked
figma:
  file_key:
  file_url:
  pages: {}
  frames: {}
  components: {}
  variables: {}
  client_preview_frames: {}
  handoff_nodes: {}
content:
  mode: final | mixed | placeholder
  display_label: 正式内容 | 混合内容 | 占位内容
  placeholders: []
analysis:
  status: pending | complete | blocked
  product_model:
  category_context:
  competitor_matrix:
  conversion_chain:
  content_priorities: []
  evidence_gaps: []
  page_implications: []
  sources: []
pdp:
  product_sources: []
  product_archetypes: []
  representative_products: []
  coverage_matrix:
  template_strategy: single_template_validated | template_family | coverage_partial
  template_assignments: []
reference_fidelity:
  mode: reference_to_theme | structure_target | visual_inspiration | competitor_evidence | none
  fidelity_profile: strict_replication | theme_adaptation
  target_url:
  build_truth_url:
  source_identity_status: pass | blocked_source_identity
  source_fingerprint:
    canonical_url:
    page_type:
    product_or_service_name:
    product_category:
    h1:
    hero_signature:
    stable_section_ids: []
    stable_section_labels: []
    desktop_layout_signature:
    mobile_layout_signature:
  mapped_source_fingerprint:
  desktop_capture:
  mobile_capture:
  source_page_specification:
  source_section_order: []
  source_content_inventory:
  composition_groups: []
  topology_contract:
  topology_signature:
  content_layout_matrix:
  theme_assembly_plan:
  source_capture_status: pending | pass | blocked_source_capture
  theme_mapping_status: pending | exact | adapted | blocked
  figma_build_status: not_run | pass | blocked
  figma_qa_status: not_run | pass | pass_with_followups | blocked
  overall_status: pending | pass | pass_with_followups | blocked
  unresolved_mappings: []
  proposed_adaptations: []
  approved_adaptations: []
  responsibility_coverage:
  section_count_coverage:
  order_match:
  content_item_coverage:
  composition_group_coverage:
  desktop_topology_coverage:
  mobile_topology_coverage:
  resolved_mapping_coverage:
  order_divergences: []
  layout_divergences: []
  approved_deviations: []
regression:
  suite_version:
  case_id:
  case_kind: golden | scenario | negative_gate
  baseline_root_ids: []
  baseline_structure_signature:
  baseline_topology_signature:
  expected_changed_sections: []
  expected_changed_topology: []
  result_structure_signature:
  result_topology_signature:
  actual_changed_sections: []
  no_op_guard: pass | blocked_no_op | not_applicable
  cross_case_results: {}
workflow:
  recognition_card:
  interaction_questions: []
  completed: []
  pending_validations: []
qa:
  build_truth_url_identity:
  product_category_identity:
  source_fingerprint_match:
  theme_demo_source_promotion:
  text_style_binding:
  grid_integrity:
  equal_height_groups:
  mobile_overflow:
  client_preview_separation:
risks: []
```

Persist exact Figma node IDs returned by tools. Never guess or reconstruct IDs. Resume from this manifest after interruption.

Treat `content.mode` as an internal field. Use `content.display_label` in recognition cards, UI questions, and handoff summaries.

Treat `sources.structure_source_urls` and `reference_fidelity.build_truth_url` as immutable after the recognition card. Theme selection or later browsing may append `theme_capability_urls` and `competitor_evidence_urls`, but may not replace Build Truth. Record every role change as a blocking decision, not an internal convenience.

For theme-based work, keep one mapping record per page section with the exact theme section/block, evidence URL, implementation level, divergence, approval, and owner.

For `structure_target` work, keep one correspondence record per source section: source responsibility, source content type, source Desktop/Mobile layout anatomy, target theme mapping, preserved/adapted/omitted status, and reason.

For every specified-structure run, record exact visible content items, unique stable source section IDs, composition groups that reference those IDs, normalized layout topology, order, Desktop/Mobile transformation, theme section/block/settings with field-level evidence, and mapping status. The source fingerprint must identify the specified structure source, while theme mapping evidence must identify a theme capability source. Missing or duplicate `Rxx` rows, source-identity mismatch, theme-demo self-mapping, missing required evidence, or an expected change with an unchanged structure signature blocks completion.

For `strict_replication`, any unresolved mapping or unapproved topology difference blocks before Figma. For `theme_adaptation`, use `native_adaptation` when evidenced native behavior preserves the source's essential content and business responsibility. Record the exact difference, consequence, evidence, and UI owner under `proposed_adaptations`, continue to Figma, and never treat that proposal as approval.

Every approved deviation must record the exact difference, approver, approval source, and date. Generated output cannot approve itself, and the word `Approved` must not appear in Figma layer names or reports without this record.

For regression work, record the suite version and case ID. A single benchmark may expose a defect but cannot establish general stability; do not promote example-specific section counts, product language, visual styles, or topology into a general rule.

For PDP work, record which product archetypes were tested. `single_template_validated` requires evidence that the base template survives the approved representative and edge states; otherwise use `template_family` or `coverage_partial`.
