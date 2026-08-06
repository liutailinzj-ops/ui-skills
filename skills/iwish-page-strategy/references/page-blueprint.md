# Page Blueprint

```yaml
page:
  name:
  strategic_concept:
  audience_priority:
  content_mode: final | mixed | placeholder
  build_route: template | theme_customization | custom
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
risks: []
research_sources: []
```

Keep section IDs stable so later Skills can map Figma nodes and resume safely.

For theme-based work, every section requires an exact implementation mapping and evidence URL. Do not use `section_custom` or `custom` as a generic fallback.
