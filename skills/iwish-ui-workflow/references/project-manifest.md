# Project Manifest

Maintain one production state object throughout the workflow:

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
  website_language:
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
  route_gate: pass | blocked
content:
  mode: final | mixed | placeholder
  display_label: 正式内容 | 混合内容 | 占位内容
  placeholders: []
analysis:
  status: pending | complete | blocked
  product_model:
  category_context:
  competitor_matrix:
  conversion_or_buying_chain:
  content_priorities: []
  evidence_gaps: []
  page_implications: []
  sources: []
strategy:
  page_blueprint:
  theme_assembly_plan:
  product_coverage_matrix:
visual_direction:
  status: pending | complete | blocked
  contract:
  representative_desktop_nodes: []
  representative_mobile_nodes: []
  typography:
  color_system:
  imagery_direction:
  composition_rules:
  responsive_rules:
  prohibited_defaults: []
figma:
  file_key:
  file_url:
  pages: {}
  frames: {}
  components: {}
  variables: {}
  client_preview_frames: {}
  internal_nodes: {}
delivery_visibility:
  customer_preview_contains_internal_qa: false
  customer_preview_contains_rxx: false
  customer_preview_contains_implementation_notes: false
  customer_shares_whole_figma_file: false
  internal_qa_location: conversation | internal_page | separate_file
reference_fidelity:
  mode: reference_to_theme | structure_target | visual_inspiration | competitor_evidence | none
  fidelity_profile: strict_replication | theme_adaptation
  build_truth_url:
  source_fingerprint:
  source_page_specification:
  composition_groups: []
  topology_contract:
  content_layout_matrix:
  theme_assembly_plan:
  source_capture_status: pending | pass | blocked
  theme_mapping_status: pending | exact | adapted | blocked
  proposed_adaptations: []
  approved_adaptations: []
pdp:
  product_sources: []
  product_archetypes: []
  representative_products: []
  template_strategy: single_template_validated | template_family | coverage_partial
workflow:
  recognition_card:
  interaction_questions: []
  completed: []
internal_qa:
  status: not_run | pass | needs_adjustment | blocked
  display_label: 未检查 | 通过 | 需要调整 | 阻塞
  report_location:
  findings: []
risks: []
```

Persist exact Figma node IDs returned by tools. Never guess or reconstruct IDs. Resume from recorded IDs after interruption.

Keep regression case IDs, baselines, topology signatures, no-op checks, cross-case results, and technical visual-gate results outside this production manifest. Store them only under `evals/` result artifacts.

Treat `content.mode` and status enums as internal values. Use their Chinese display labels in UI-facing messages and internal Figma annotations.

Keep the structure-source URL immutable after recognition. Theme selection may append theme-capability sources but may not replace Build Truth. Record approved deviations with the exact decision, approver, source, and date.

Customer-preview frames may contain only the website design. Internal QA, Rxx labels, theme mappings, source warnings, implementation notes, placeholder provenance, and replacement instructions belong in the conversation, an internal page, or a separate internal file according to `delivery_visibility`.
