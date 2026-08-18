# Theme Capability Map

Create this artifact before the page blueprint for theme-customization work.

## Target theme contract

Resolve the target before mapping Sections:

- `provided`: use the exact provided target theme. Do not replace it with a more convenient or familiar theme.
- `not_provided`: research current official theme-store and vendor evidence, compare suitable paid candidates, and automatically select one best-fit target. Score category/catalog fit, required commerce and content responsibilities, selected competitor-module topology, functional needs, responsive behavior, visual-direction brief, evidence quality, and expected customization burden.
- `not_applicable`: use only for fully custom work; skip this artifact and do not impose theme constraints.

Record the candidate list, selection criteria, selected reason, and concise rejection reasons. Do not model who selected, purchased, confirmed, or approved the theme, and do not pause for that workflow. Do not choose Dawn or another free theme because its code is public; a free theme is eligible only when it was provided as the target or the project explicitly permits free themes.

## Theme evidence

```yaml
theme:
  input_state: provided | not_provided
  name:
  preset:
  selection_basis: provided | matched
  is_paid: true | false
  matching:
    candidate_themes: []
    criteria: []
    selected_reason:
    rejected_reasons: []
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
- Inspect the closest native primitive as an implementation baseline, then compare it with the required content responsibility, topology, hierarchy, interaction, responsive behavior, and approved visual direction. If native behavior causes material loss and the contracted scope allows it, map to style, CSS, Liquid, or a scoped new Section instead of treating the native approximation as the target design.
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
- Map the complete page system, including required header, commerce, content, cross-sell, global, and footer responsibilities. Mapping three representative Sections is a preflight result, not a complete Theme Capability Map or final page assembly.

## Route gates

### Theme customization

- Prefer the lowest-complexity implementation that preserves the required content, layout relationship, interaction, and responsive behavior.
- Do not treat native Section availability as a visual ceiling or use limited customer assets as a reason to lower fidelity.
- Classify every Section as `theme_native`, `configuration`, `style`, `custom_css`, `custom_liquid`, `section_custom`, `app_or_third_party`, `custom`, or `pending_engineering`.
- Use the contracted development scope and engineering estimate; do not enforce a universal Section-count or page-height percentage.
- Record scope status, evidence, implementation owner, and unresolved estimate dependencies for non-native work.

### Custom

- Theme budgets do not apply, but platform feasibility and component contracts still apply.

Do not continue to Figma when required theme evidence is unavailable, a selected module's capture or identity/fingerprint fails, a theme demo was promoted to selected-module source, a critical responsibility has no feasible route, or a material route gate remains unresolved. Non-critical evidenced native adaptations continue to Figma.
