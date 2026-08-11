# Page Blueprint

```yaml
page:
  name:
  strategic_concept:
  audience_priority:
  website_language:
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
  build_truth_url:
  source_page_specification:
  theme_assembly_plan:
  source_section_order: []
  source_content_inventory:
  composition_groups: []
  topology_contract:
  content_layout_matrix:
  responsibility_coverage:
  unresolved_mappings: []
  proposed_adaptations: []
  approved_adaptations: []
  source_capture_status: pending | pass | blocked
  theme_mapping_status: pending | exact | adapted | blocked
responsive:
  section_contract:
  alignment_groups: []
  shared_content_policy:
  breakpoint_preview_widths: {}
pdp:
  template_strategy: single_template_validated | template_family | coverage_partial
  product_archetypes: []
  representative_products: []
  coverage_matrix:
  conditional_modules: []
  template_assignments: []
theme:
  name:
  preset:
  capability_map:
  custom_section_count_ratio:
  custom_section_height_ratio:
visual_direction_brief:
  required_brand_impression: []
  content_emphasis: []
  source_visual_principles: []
  target_theme_constraints: []
  imagery_needs: []
  responsive_priorities: []
  prohibited_generic_defaults: []
sections:
  - id:
    name:
    responsibility:
    journey_stages: []
    analysis_evidence: []
    required_content_types: []
    asset_status: final | available | placeholder
    responsive_priority:
    likely_components: []
    implementation:
      level: theme_native | configuration | style | custom_css | custom_liquid | section_custom | custom
      theme_section:
      theme_blocks: []
      evidence_url:
      allowed_settings: []
      responsive_behavior:
        shared_identity:
        desktop_state:
        mobile_state:
        allowed_differences: []
      divergence:
      approval_required: false
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
      responsive_layout_class:
      breakpoint_states: {}
      topology_contract:
      adaptation_decision:
        status: proposed_adaptation | approved_adaptation | rejected_adaptation | not_applicable
        exact_difference:
        approved_by:
        approval_source:
        approved_at:
    product_applicability:
      required_for: []
      optional_for: []
      hidden_for: []
risks: []
research_sources: []
```

Keep section IDs stable so later production Skills can map Figma nodes and resume safely.

Every theme-based section requires an exact implementation mapping and evidence URL. Do not use custom implementation as a generic fallback.

Every page section must trace to Product and Competitor Analysis, a required platform responsibility, or a captured source section. For PDP work, include product applicability and a truthful template strategy. For specified-structure work, include exact shared content bindings, connected composition groups, one Responsive Section Contract with breakpoint states, and Theme Assembly Plan mapping.

The `visual_direction_brief` supplies evidence and required outcomes to `$iwish-visual-direction`; it must not prescribe an unrelated palette, fixed card system, or regression-fixture style.

Keep evaluation baselines, expected changes, no-op checks, and case results out of this production blueprint.
