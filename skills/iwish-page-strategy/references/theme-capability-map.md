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
source_identity:
  structure_source_url:
  product_or_service_name:
  product_category:
  h1:
  fingerprint_status: pass | blocked_source_identity
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
    stable_source_id:
    responsibility:
    reference_source_section:
    source_order:
    source_content_bindings: []
    source_layout_class:
      desktop:
      mobile:
    product_applicability: []
    chosen_theme_section:
    chosen_blocks: []
    chosen_settings: {}
    conversion_status: exact_native | composed_native | unresolved
    implementation_level: theme_native | configuration | style | custom_css | custom_liquid | section_custom | custom
    evidence_url:
    structure_source_url:
    theme_capability_url:
    divergence:
    approval:
```

## Mapping rules

- Prefer the exact section and block names used by the theme editor or vendor documentation.
- Treat the live demo as visual evidence and vendor documentation as capability evidence.
- Treat all theme store, vendor documentation, demo, and current-theme URLs as theme capability evidence. They must not define page content, source order, product identity, or Build Truth unless the user explicitly selected the same URL as structure source.
- Map the content responsibility to the closest native primitive before changing layout geometry.
- Record unsupported settings instead of inventing them.
- Mark a mapping as `partial` when only a screenshot or marketing feature list is available.
- Do not classify a section as custom merely because its copy or art direction is project-specific.
- For `structure_target`, map source responsibility and source layout anatomy separately. A theme section may cover the responsibility while requiring a documented geometry adaptation.
- For `reference_to_theme`, create one cross-source mapping for every stable source section ID. Record the structure-source URL, exact source order and content bindings, Desktop/Mobile layout classes, exact target theme Section/Blocks/settings, theme capability evidence URL, and `exact_native | composed_native | unresolved` status. Do not use semantic similarity, theme-demo self-mapping, or `adapted` as a success state.
- Any `reference_to_theme` `unresolved` mapping blocks the page blueprint and Figma. Return the gap and require one decision: accept the named deviation, change theme, or approve theme customization/custom work.
- For PDP work, verify conditional visibility, block ordering, product-template assignment, and empty-state behavior where the proposed template strategy depends on them.

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

Do not continue to Figma when required theme evidence is unavailable, source identity/fingerprint fails, a theme demo was promoted to Build Truth, or a route gate fails.
