# Project Manifest

Maintain one production state object throughout the workflow:

```yaml
project:
  name:
  brand:
  product_category:
  target_market:
  audience_type: dtc | b2b | mixed
  platform: shopify | wordpress
  production_scenario: research_led_theme_customization | selected_modules_theme_customization | custom
  build_route: theme_customization | custom
  strategy_mode: research_led | hybrid_led | custom_led
  brand_input_state: full_vi | logo_and_color | logo_only | no_brand_assets
  brand_authorship_mode: customer_led | constrained_authoring | open_concept
  website_language:
scope:
  requested_page:
  features: []
sources:
  customer_facts:
  customer_assets:
  structure_source_urls: []
  selected_structure_modules: []
  theme_capability_urls: []
  competitor_evidence_urls: []
  visual_inspiration_urls: []
  source_role_assignments: {}
asset_input:
  brand_assets: complete_vi | logo_and_color | logo_only | none
  product_assets: production_ready | partial | none
  route: brand_ready_product_ready | brand_ready_product_missing | brand_missing_product_ready | brand_missing_product_missing
  supplied_brand_invariants: []
  supplied_product_truth: []
  usable_product_media: []
  missing_decision_critical_media: []
  temporary_media_allowed: true | false
  consistency_anchor:
    product_form:
    finish_or_material:
    control_or_detail_language:
    environment_rules:
theme:
  input_state: provided | not_provided | not_applicable
  name:
  preset:
  selection_basis: provided | matched | not_applicable
  state: demo_only | code_available | current_site | matched_from_public_evidence | not_applicable
  is_paid: true | false | not_applicable
  matching:
    candidate_themes: []
    criteria: []
    selected_reason:
    rejected_reasons: []
  capability_map:
  evidence_urls: []
  route_gate: pass | blocked | not_applicable
  customization_scope:
    source:
    approved_capabilities: []
    excluded_capabilities: []
    engineering_review_status: pending | reviewed | not_required
content:
  mode: final | mixed | placeholder
  display_label: 正式内容 | 混合内容 | 占位内容
  placeholders: []
  customer_visible_ledger:
    sections:
      - section_id:
        slots:
          - slot_id:
            kind: text | media | control
            role:
            canonical_client_value:
            evidence_status: fact | inference | placeholder
            required: true | false
            internal_metadata:
              source_class:
              approval_state:
              replacement_owner:
              publication_restrictions: []
  internal_marker_policy:
    forbidden_visible_phrases: []
    internal_only_fields: []
analysis:
  status: pending | complete | blocked
  product_model:
  category_context:
  competitor_matrix:
  conversion_or_buying_chain:
  content_priorities: []
  evidence_gaps: []
  page_implications: []
  sources: []
content_strategy:
  status: pending | pass | needs_revision | blocked
  product_truth:
  audience_questions: []
  category_decision_factors: []
  competitor_presentation_logic: []
  conversion_or_buying_chain: []
  message_hierarchy:
  section_content_cards: []
  coverage:
strategy:
  page_blueprint:
  theme_assembly_plan:
  responsive_section_contract:
  product_coverage_matrix:
  page_composition_gate:
    board_node_id:
    section_order: []
    container_modes: []
    alignment_groups: []
    color_distribution:
    media_distribution:
    density_curve:
    primary_conversion_focus:
    source_module_positions: []
    responsive_risk_sections: []
    default_risk_audit:
    screenshot_status: pending | pass | needs_revision
visual_direction:
  status: pending | complete | blocked
  authority_version:
  authority_state: draft | active | superseded
  source_precedence:
    - customer_confirmed_brand_and_requirements
    - approved_scoped_override
    - active_project_master_rules
    - evidence_backed_candidate
  project_invariants: []
  preserved_customer_invariants: []
  project_authored_brand:
    name_or_wordmark_treatment:
    creative_thesis:
    authored_fields: []
    evidence: []
  page_overrides: {}
  candidate_decisions: []
  direction_candidates: []
  selected_candidate_id:
  selection_rationale:
  visual_signature:
    color_behavior:
    typography:
    first_screen_topology:
    page_rhythm:
    component_grammar:
    imagery:
    interaction:
  signature_evidence: []
  conflict_check:
    status: pending | pass | needs_resolution | blocked
    findings: []
  revision_log: []
  contract:
  representative_section_family_nodes: []
  breakpoint_proof_nodes: []
  typography:
  color_system:
  imagery_direction:
  visual_asset_coverage: []
  composition_rules:
  responsive_rules:
  prohibited_defaults: []
figma:
  file_key:
  file_url:
  pages: {}
  frames: {}
  components: {}
  variables: {}
  breakpoint_preview_frames: {}
  responsive_section_components: {}
  paired_section_instances: {}
  internal_nodes: {}
  component_library:
    root_node_id:
    category_node_ids: {}
    family_row_node_ids: {}
    component_set_node_ids: {}
    archive_node_id:
    presentation_screenshot:
    alignment_status: pending | pass | needs_revision
delivery_visibility:
  customer_preview_contains_internal_qa: false
  customer_preview_contains_rxx: false
  customer_preview_contains_implementation_notes: false
  customer_shares_whole_figma_file: false
  internal_qa_location: conversation | internal_page | separate_file
reference_fidelity:
  mode: selected_structure_modules | visual_inspiration | competitor_evidence | none
  fidelity_profile: theme_adaptation | not_applicable
  selected_module_sources: []
  module_fingerprints: []
  selected_module_specification:
  composition_groups: []
  topology_contract:
  content_layout_matrix:
  theme_assembly_plan:
  source_capture_status: pending | pass | blocked
  theme_mapping_status: pending | exact | adapted | blocked
  proposed_adaptations: []
  approved_adaptations: []
pdp:
  product_sources: []
  product_archetypes: []
  representative_products: []
  template_strategy: single_template_validated | template_family | coverage_partial
workflow:
  entry_mode: complete_production | targeted_revision
  recognition_card:
  interaction_questions: []
  revision_scope:
    target_node_ids: []
    invalidated_dependencies: []
    preserved_dependencies: []
    qa_scope: local | full_page
  completed: []
delivery:
  scope: complete_page | targeted_revision | design_exploration
  representative_preflight_status: not_run | pass | needs_revision | blocked
  complete_desktop_preview_status: not_run | pass | blocked
  complete_mobile_preview_status: not_run | pass | blocked
  overall_completion_status: in_progress | complete | blocked
internal_qa:
  status: not_run | pass | needs_adjustment | blocked
  display_label: 未检查 | 通过 | 需要调整 | 阻塞
  report_location:
  findings: []
quality_gates:
  component_library: not_run | pass | needs_adjustment | blocked
  section_visual: not_run | pass | needs_adjustment | blocked
  page_composition: not_run | pass | needs_adjustment | blocked
  content_strategy: not_run | pass | needs_adjustment | blocked
risks: []
```

Persist exact Figma node IDs returned by tools. Never guess or reconstruct IDs. Resume from recorded IDs after interruption.

Keep the active visual authority stable across pages and sessions. A page override is valid only for its recorded page/Section scope, named fields, reason, evidence, approval state, and revision date. Recommendations, search results, model inferences, and unapproved alternatives remain under `candidate_decisions` and cannot replace active rules. When a project-wide rule changes, increment `authority_version`, append the exact change to `revision_log`, and list every invalidated page, component, variable, or representative composition under `workflow.revision_scope`.

Maintain one canonical customer-visible content ledger before Figma production. Give every visible text, media, and control a stable slot ID, canonical client value, evidence status, and breakpoint visibility. Store approval state, placeholder provenance, replacement owner, source class, and internal instructions beside the slot as internal metadata; never concatenate those fields into the rendered client value. Desktop and Mobile resolve the same slot IDs and values unless the Responsive Section Contract records an evidenced content variant.

Classify brand and product assets independently. Persist the four-way asset route and one temporary product consistency anchor whenever approved product media is missing. Generated views may change environment, crop, state, and viewpoint, but they must not silently change the product form, finish system, controls, or identifying details.

Persist the Content Strategy Contract before visual direction. Each Section Content Card must record one visitor question, unique content job, product-specific angle, media job, proof state, and next action. Generic safe copy is not sufficient.

Persist only the target-theme input state, selected target theme, selection basis, evidence, and matching rationale. Do not persist customer-confirmation workflow, purchaser identity, or approval steps. For `theme_customization`, `provided` uses the exact supplied target and `not_provided` must resolve to one evidence-backed paid target without pausing. For `custom`, use `not_applicable` throughout. A free theme may be matched only when the project explicitly permits free themes.

Persist the page-composition board and component-library presentation before final page wrappers. Do not mark production complete when isolated Sections pass but the complete-page rhythm or component library remains unaligned. A board made only of anonymous density/color blocks does not pass; it must expose judgeable media roles, text hierarchy, controls, surfaces, Section order, and approximate final proportions.

Set `representative_preflight_status` independently from final delivery. For `complete_page`, set `overall_completion_status: complete` only after both complete Desktop and Mobile previews exist, are assembled from the same responsive Section families, and have passed QA. Representative-Section success, a component library, or a composition board cannot substitute for either preview.

For light-brand projects, persist the brand-authorship mode, supplied invariants, project-authored brand fields, two materially different internal visual-direction candidates, and the selected candidate rationale. Record evidence for all seven visual-signature dimensions. Generic adjectives and model preference are not evidence; a named creative inference must connect to the product, audience, journey, content behavior, implementation route, or supplied asset and explain why the rejected candidate fits less well.

Persist a Visual-Asset Coverage Matrix for every decision-critical media role. Missing customer imagery changes `source_class` and replacement work, not the fidelity target. Different products, configurations, features, and scenes must have visibly different temporary media when the media communicates their difference.

Keep regression case IDs, baselines, topology signatures, no-op checks, cross-case results, and technical visual-gate results outside this production manifest. Store them only under `evals/` result artifacts.

Treat `content.mode` and status enums as internal values. Use their Chinese display labels in UI-facing messages and internal Figma annotations.

Keep each selected module's structure-source URL immutable after recognition. Theme selection may append theme-capability sources but may not replace a selected module's source. Record approved deviations with the exact decision, approver, source, and date.

Customer-preview frames may contain only the website design. Internal QA, Rxx labels, theme mappings, source warnings, implementation notes, placeholder provenance, and replacement instructions belong in the conversation, an internal page, or a separate internal file according to `delivery_visibility`.
