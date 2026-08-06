# Page Blueprint

```yaml
page:
  name:
  strategic_concept:
  audience_priority:
  site_model: dtc | b2b | mixed
  strategy_mode: research_led | reference_led | hybrid_led | existing_site_led
  content_mode: final | mixed | placeholder
  content_mode_label: 正式内容 | 混合内容 | 占位内容
  build_route: template | theme_customization | custom
  reference_mode: reference_to_theme | structure_target | visual_inspiration | competitor_evidence | none
analysis:
  product_model:
  category_context:
  competitor_matrix:
  conversion_or_buying_chain:
  content_priorities: []
  evidence_gaps: []
  page_implications: []
  theme_criteria: []
reference_fidelity:
  target_url:
  source_page_specification:
  theme_assembly_plan:
  source_section_order: []
  source_content_inventory:
  unresolved_mappings: []
  section_count_coverage:
  order_match:
  content_item_coverage:
  desktop_layout_class_coverage:
  mobile_layout_class_coverage:
  resolved_mapping_coverage:
  approved_deviations: []
  baseline_structure_signature:
  result_structure_signature:
  expected_changed_sections: []
  no_op_guard: pass | blocked_no_op | not_applicable
  content_layout_matrix:
  responsibility_coverage:
  order_divergences: []
  layout_divergences: []
pdp:
  template_strategy: single_template_validated | template_family | coverage_partial
  product_archetypes: []
  representative_products: []
  coverage_matrix:
  conditional_modules: []
  template_assignments: []
theme:
  name:
  reference_url:
  capability_map:
  custom_section_count_ratio:
  custom_section_height_ratio:
direction:
  visual_principles: []
  differentiation: []
sections:
  - id:
    name:
    responsibility:
    journey_stages: []
    analysis_evidence: []
    required_content_types: []
    asset_status: final | available | placeholder
    desktop_priority:
    mobile_priority:
    likely_components: []
    implementation:
      level: theme_native | configuration | style | custom_css | custom_liquid | section_custom | custom
      theme_section:
      theme_blocks: []
      evidence_url:
      allowed_settings: []
      desktop_behavior:
      mobile_behavior:
      divergence:
      approval_required: false
    notes:
    reference_correspondence:
      stable_source_id:
      source_section:
      source_responsibility:
      source_layout_anatomy:
      disposition: preserved | adapted | omitted | added
      conversion_status: exact_native | composed_native | unresolved
      content_bindings: []
      desktop_layout_class:
      mobile_layout_class:
      approved_deviation:
      reason:
    product_applicability:
      required_for: []
      optional_for: []
      hidden_for: []
risks: []
research_sources: []
```

Keep section IDs stable so later Skills can map Figma nodes and resume safely.

For theme-based work, every section requires an exact implementation mapping and evidence URL. Do not use `section_custom` or `custom` as a generic fallback.

Every page section must trace to Product and Competitor Analysis, a required platform responsibility, or an approved strict source section. For PDP work, a page blueprint is incomplete without product applicability and a template strategy. For `structure_target`, a blueprint is incomplete without source-to-target correspondence. For `reference_to_theme`, a blueprint is incomplete until every stable source section has exact content bindings, Desktop/Mobile layout classes, a Theme Assembly Plan mapping, and either `exact_native`, `composed_native`, or an explicitly approved deviation. Any `unresolved` mapping blocks Figma.

For `reference_to_theme`, the blueprint header must repeat the Build Truth URL and Source Identity Fingerprint and list theme capability URLs separately. Reject the blueprint when its product/category, H1, hero signature, or stable section sequence comes from a theme demo or any URL other than the specified structure source.
