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
  fidelity_profile: strict_replication | theme_adaptation
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
  proposed_adaptations: []
  approved_adaptations: []
  source_capture_status: pending | pass | blocked_source_capture
  theme_mapping_status: pending | exact | adapted | blocked
  section_count_coverage:
  order_match:
  content_item_coverage:
  composition_group_coverage:
  desktop_topology_coverage:
  mobile_topology_coverage:
  resolved_mapping_coverage:
  approved_deviations: []
  topology_signature:
  baseline_structure_signature:
  result_structure_signature:
  baseline_topology_signature:
  result_topology_signature:
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
      composition_group_id:
      source_section:
      source_responsibility:
      source_layout_anatomy:
      disposition: preserved | adapted | omitted | added
      priority: critical | structural | presentational
      conversion_status: exact_native | composed_native | native_adaptation | requires_custom | unresolved
      content_bindings: []
      desktop_layout_class:
      mobile_layout_class:
      topology_contract:
      topology_match: exact | deviation | unavailable
      adaptation_decision:
        status: proposed_adaptation | approved_adaptation | rejected_adaptation | not_applicable
        exact_difference:
        approved_by:
        approval_source:
        approved_at:
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

Every page section must trace to Product and Competitor Analysis, a required platform responsibility, or a captured source section. For PDP work, a page blueprint is incomplete without product applicability and a template strategy. For specified-structure work, a blueprint is incomplete until every unique stable source section has exact content bindings, composition-group membership, Desktop/Mobile topology, and a Theme Assembly Plan mapping. In `strict_replication`, only `exact_native`, validated `composed_native`, or an explicitly approved deviation can build. In `theme_adaptation`, an evidenced `native_adaptation` can build and must enter UI review; a critical `unresolved` mapping blocks.

For `reference_to_theme`, the blueprint header must repeat the Build Truth URL and Source Identity Fingerprint, list theme capability URLs separately, and carry the topology signature and composition groups. Reject the blueprint when its product/category, H1, hero signature, stable section sequence, or topology comes from a theme demo or any URL other than the specified structure source.
