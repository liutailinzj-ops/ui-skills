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
  competitor_urls: []
  reference_urls: []
  reference_modes: {}
  theme_reference:
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
  target_url:
  desktop_capture:
  mobile_capture:
  source_page_specification:
  source_section_order: []
  source_content_inventory:
  content_layout_matrix:
  theme_assembly_plan:
  unresolved_mappings: []
  responsibility_coverage:
  section_count_coverage:
  order_match:
  content_item_coverage:
  desktop_layout_class_coverage:
  mobile_layout_class_coverage:
  resolved_mapping_coverage:
  order_divergences: []
  layout_divergences: []
  approved_deviations: []
regression:
  baseline_root_ids: []
  baseline_structure_signature:
  expected_changed_sections: []
  result_structure_signature:
  actual_changed_sections: []
  no_op_guard: pass | blocked_no_op | not_applicable
workflow:
  recognition_card:
  interaction_questions: []
  completed: []
  pending_validations: []
qa:
  text_style_binding:
  grid_integrity:
  equal_height_groups:
  mobile_overflow:
  client_preview_separation:
risks: []
```

Persist exact Figma node IDs returned by tools. Never guess or reconstruct IDs. Resume from this manifest after interruption.

Treat `content.mode` as an internal field. Use `content.display_label` in recognition cards, UI questions, and handoff summaries.

For theme-based work, keep one mapping record per page section with the exact theme section/block, evidence URL, implementation level, divergence, approval, and owner.

For `structure_target` work, keep one correspondence record per source section: source responsibility, source content type, source Desktop/Mobile layout anatomy, target theme mapping, preserved/adapted/omitted status, and reason.

For `reference_to_theme`, do not use responsibility coverage as a proxy for fidelity. Record exact visible content items, stable source section IDs, order, Desktop/Mobile layout class, theme section/block/settings, and mapping status. Any unresolved mapping blocks Figma. Any expected change with an unchanged structure signature blocks completion.

For PDP work, record which product archetypes were tested. `single_template_validated` requires evidence that the base template survives the approved representative and edge states; otherwise use `template_family` or `coverage_partial`.
