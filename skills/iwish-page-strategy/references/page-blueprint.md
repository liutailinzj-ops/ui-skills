# Page Blueprint

```yaml
page:
  name:
  strategic_concept:
  audience_priority:
  website_language:
  site_model: dtc | b2b | mixed
  production_scenario: research_led_theme_customization | selected_modules_theme_customization | custom
  strategy_mode: research_led | hybrid_led | custom_led
  content_mode: final | mixed | placeholder
  content_mode_label: 正式内容 | 混合内容 | 占位内容
  build_route: theme_customization | custom
  brand_input_state: full_vi | logo_and_color | logo_only | no_brand_assets
  reference_mode: selected_structure_modules | visual_inspiration | competitor_evidence | none
  fidelity_profile: theme_adaptation | not_applicable
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
  selected_module_sources: []
  selected_structure_modules: []
  module_fingerprints: []
  selected_module_specification:
  theme_assembly_plan:
  selected_module_order: []
  selected_content_inventory:
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
  customization_scope:
    source:
    approved_capabilities: []
    excluded_capabilities: []
    engineering_review_status: pending | reviewed | not_required
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
      level: theme_native | configuration | style | custom_css | custom_liquid | section_custom | app_or_third_party | custom | pending_engineering
      scope_status: in_scope | needs_estimate | approved | excluded
      implementation_owner:
      engineering_notes:
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

Every page section must trace to Product and Competitor Analysis, a required platform responsibility, an approved requirement, or an explicitly selected source module. For PDP work, include product applicability and a truthful template strategy. For selected competitor-module work, include exact shared content bindings, connected composition groups, one Responsive Section Contract with breakpoint states, and Theme Assembly Plan mapping for the selected scope only.

The `visual_direction_brief` supplies evidence and required outcomes to `$iwish-visual-direction`; it must not prescribe an unrelated palette, fixed card system, or regression-fixture style.

Keep evaluation baselines, expected changes, no-op checks, and case results out of this production blueprint.
