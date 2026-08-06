# Theme Capability Map

Create this artifact before the page blueprint for template and theme-customization work.

## Theme evidence

```yaml
theme:
  name:
  preset:
  reference_url:
  vendor_docs_url:
  demo_url:
  checked_at:
  evidence_status: verified | partial | unavailable
available_sections:
  - exact_name:
    block_types: []
    relevant_settings: []
    desktop_behavior:
    mobile_behavior:
    limitations: []
    evidence_url:
page_mappings:
  - page_section_id:
    responsibility:
    chosen_theme_section:
    chosen_blocks: []
    implementation_level: theme_native | configuration | style | custom_css | custom_liquid | section_custom | custom
    evidence_url:
    divergence:
    approval:
```

## Mapping rules

- Prefer the exact section and block names used by the theme editor or vendor documentation.
- Treat the live demo as visual evidence and vendor documentation as capability evidence.
- Map the content responsibility to the closest native primitive before changing layout geometry.
- Record unsupported settings instead of inventing them.
- Mark a mapping as `partial` when only a screenshot or marketing feature list is available.
- Do not classify a section as custom merely because its copy or art direction is project-specific.

## Route gates

### Template

- Allow `theme_native`, `configuration`, and `style`.
- Allow `custom_css` only when included in internal scope.
- Block `custom_liquid`, `section_custom`, and `custom` unless explicitly approved.

### Theme customization

- Prefer native sections, configuration, style, CSS, and small Liquid composition.
- Keep `section_custom` and `custom` at or below 20% of both section count and estimated page height by default.
- Record approval and implementation owner for every custom exception.

### Custom

- Theme budgets do not apply, but platform feasibility and component contracts still apply.

Do not continue to Figma when required theme evidence is unavailable or a route gate fails.
