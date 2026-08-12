# Theme Capability Map

Create this artifact before the page blueprint for theme-customization work.

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
selected_module_sources:
  - module_id:
    structure_source_url:
    module_signature:
    fingerprint_status: pass | blocked_source_identity
available_sections:
  - exact_name:
    block_types: []
    relevant_settings:
      - exact_name:
        supported_values: []
        evidence_url:
        evidence_quality: editor | vendor_docs | current_theme | demo_observation | marketing_only
    responsive_behavior:
      automatic:
      desktop_settings: {}
      mobile_settings: {}
      allowed_transformations: []
    limitations: []
    evidence_url:
page_mappings:
  - page_section_id:
    stable_source_id:
    responsibility:
    reference_source_section:
    source_order:
    source_content_bindings: []
    source_responsive_layout_class:
      shared_identity:
      desktop_state:
      mobile_state:
    source_composition_group_id:
    source_topology_signature:
    responsive_section_contract:
    product_applicability: []
    chosen_theme_section:
    chosen_blocks: []
    chosen_settings: {}
    setting_evidence: {}
    conversion_status: exact_native | composed_native | native_adaptation | requires_custom | unresolved
    priority: critical | structural | presentational
    implementation_level: theme_native | configuration | style | custom_css | custom_liquid | section_custom | app_or_third_party | custom | pending_engineering
    scope_status: in_scope | needs_estimate | approved | excluded
    implementation_owner:
    evidence_url:
    structure_source_url:
    theme_capability_url:
    divergence:
    adaptation_decision:
      status: proposed_adaptation | approved_adaptation | rejected_adaptation | not_applicable
      exact_difference:
      approved_by:
      approval_source:
      approved_at:
```

## Mapping rules

- Prefer the exact section and block names used by the theme editor or vendor documentation.
- Verify exact settings individually. `demo_observation` can support visible behavior but does not prove an editable setting; `marketing_only` cannot support `exact_native` or `composed_native`.
- Treat the live demo as visual evidence and vendor documentation as capability evidence.
- Treat all theme store, vendor documentation, demo, and current-theme URLs as theme capability evidence. They must not define page content, selected-module structure, or product identity unless the user explicitly selected the same URL as a module source.
- Map the content responsibility to the closest native primitive before changing layout geometry.
- Record unsupported settings instead of inventing them.
- Mark evidence as `partial` when only a screenshot or marketing feature list is available; do not promote partial evidence to an exact mapping.
- Do not classify a section as custom merely because its copy or art direction is project-specific.
- For `selected_structure_modules`, map source responsibility and source layout anatomy separately. A theme section may cover the responsibility while requiring a documented geometry adaptation or scoped custom implementation.
- For selected competitor-module work, create one cross-source mapping for every stable selected-module ID. Record the structure-source URL, local order and shared content bindings, one responsive layout class with Desktop/Mobile states, exact target-theme Section/Blocks/settings, theme-capability evidence URL, priority, mapping status, and any proposed adaptation or scoped custom route. Do not use semantic similarity or theme-demo self-mapping as evidence.
- Keep one target Section identity across breakpoints. Record Mobile as theme settings or automatic behavior of that Section, not as a separately invented component or content layout.
- Validate the source topology and composition group as a separate axis from content responsibility. A theme primitive that covers the same topic but changes grouping, region proportions, visible-item count, interaction, overflow, or responsive transformation is not an exact mapping.
- Accept `composed_native` only when all contributing native primitives and settings are evidenced and their combined rendered output preserves one source boundary and topology. Otherwise mark it `unresolved`.
- Do not use invented names such as `approved modular composition` or `static prototype` as theme evidence. `approved` is valid only when the manifest contains explicit approval provenance for the exact deviation.
- In `theme_adaptation`, `native_adaptation` and feasible in-scope custom implementations continue. A critical `unresolved` row blocks until engineering confirms a route or UI changes the selected module.
- For PDP work, verify conditional visibility, block ordering, product-template assignment, and empty-state behavior where the proposed template strategy depends on them.

## Route gates

### Theme customization

- Prefer the lowest-complexity implementation that preserves the required content, layout relationship, interaction, and responsive behavior.
- Classify every Section as `theme_native`, `configuration`, `style`, `custom_css`, `custom_liquid`, `section_custom`, `app_or_third_party`, `custom`, or `pending_engineering`.
- Use the contracted development scope and engineering estimate; do not enforce a universal Section-count or page-height percentage.
- Record scope status, evidence, implementation owner, and unresolved estimate dependencies for non-native work.

### Custom

- Theme budgets do not apply, but platform feasibility and component contracts still apply.

Do not continue to Figma when required theme evidence is unavailable, a selected module's capture or identity/fingerprint fails, a theme demo was promoted to selected-module source, a critical responsibility has no feasible route, or a material route gate remains unresolved. Non-critical evidenced native adaptations continue to Figma.
