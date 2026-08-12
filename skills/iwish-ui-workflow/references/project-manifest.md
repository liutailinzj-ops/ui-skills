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
  production_scenario: research_led_theme_customization | selected_modules_theme_customization | custom
  build_route: theme_customization | custom
  strategy_mode: research_led | hybrid_led | custom_led
  brand_input_state: full_vi | logo_and_color | logo_only | no_brand_assets
  website_language:
scope:
  requested_page:
  features: []
sources:
  customer_facts:
  customer_assets:
  structure_source_urls: []
  selected_structure_modules: []
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
  customization_scope:
    source:
    approved_capabilities: []
    excluded_capabilities: []
    engineering_review_status: pending | reviewed | not_required
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
  responsive_section_contract:
  product_coverage_matrix:
visual_direction:
  status: pending | complete | blocked
  contract:
  representative_section_family_nodes: []
  breakpoint_proof_nodes: []
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
  breakpoint_preview_frames: {}
  responsive_section_components: {}
  paired_section_instances: {}
  internal_nodes: {}
delivery_visibility:
  customer_preview_contains_internal_qa: false
  customer_preview_contains_rxx: false
  customer_preview_contains_implementation_notes: false
  customer_shares_whole_figma_file: false
  internal_qa_location: conversation | internal_page | separate_file
reference_fidelity:
  mode: selected_structure_modules | visual_inspiration | competitor_evidence | none
  fidelity_profile: theme_adaptation | not_applicable
  selected_module_sources: []
  module_fingerprints: []
  selected_module_specification:
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

Keep each selected module's structure-source URL immutable after recognition. Theme selection may append theme-capability sources but may not replace a selected module's source. Record approved deviations with the exact decision, approver, source, and date.

Customer-preview frames may contain only the website design. Internal QA, Rxx labels, theme mappings, source warnings, implementation notes, placeholder provenance, and replacement instructions belong in the conversation, an internal page, or a separate internal file according to `delivery_visibility`.
