# Page Blueprint

```yaml
page:
  name:
  strategic_concept:
  audience_priority:
  content_mode: final | mixed | placeholder
  build_route: template | theme_customization | custom
  reference_mode: structure_target | visual_inspiration | competitor_evidence | none
reference_fidelity:
  target_url:
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
      source_section:
      source_responsibility:
      source_layout_anatomy:
      disposition: preserved | adapted | omitted | added
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

For PDP work, a page blueprint is incomplete without product applicability and a template strategy. For `structure_target`, a blueprint is incomplete without source-to-target correspondence.
