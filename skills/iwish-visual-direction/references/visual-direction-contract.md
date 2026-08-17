# Visual Direction Contract

Record a compact contract that is specific enough to guide page production without freezing creative judgment.

```yaml
visual_direction:
  authority_version:
  authority_state: draft | active | superseded
  brand_input_state: full_vi | logo_and_color | logo_only | no_brand_assets
  brand_authorship_mode: customer_led | constrained_authoring | open_concept
  asset_route: brand_ready_product_ready | brand_ready_product_missing | brand_missing_product_ready | brand_missing_product_missing
  preserved_customer_invariants: []
  project_authored_brand:
    name_or_wordmark_treatment:
    creative_thesis:
    authored_fields: []
    evidence: []
  concept_statement:
  brand_character: []
  audience_impression:
  direction_candidates:
    - candidate_id:
      concept_statement:
      signature_summary:
      supporting_evidence: []
      conflicts_or_weaknesses: []
  selected_candidate_id:
  selection_rationale:
  rejected_candidate_rationale:
  default_risk_audit:
    familiar_safe_defaults: []
    evidenced_fields: []
    unsupported_combination_count:
    third_candidate_required: true | false
  visual_signature:
    color_behavior:
      decision:
      evidence: []
    typography:
      decision:
      evidence: []
    first_screen_topology:
      decision:
      evidence: []
    page_rhythm:
      decision:
      evidence: []
    component_grammar:
      decision:
      evidence: []
    imagery:
      decision:
      evidence: []
    interaction:
      decision:
      evidence: []
  typography:
    display:
    heading:
    body:
    scale_behavior:
  color:
    primary:
    secondary:
    neutral:
    accent_usage:
    contrast_rules:
  imagery:
    subject:
    environment:
    lighting:
    crop_behavior:
    product_scale:
    temporary_asset_route:
  visual_asset_coverage:
    - slot_id:
      communication_job:
      subject:
      environment:
      viewpoint:
      crop_and_ratio:
      product_scale:
      lighting_or_render_style:
      required_variation:
      source_class:
      replacement_rule:
      asset_or_node_ids: []
  temporary_product_consistency_anchor:
    product_form:
    finish_or_material:
    control_or_detail_language:
    environment_rules:
  composition:
    container_behavior:
    alignment_groups: []
    density:
    spacing_rhythm:
    alignment_logic:
    media_content_relationship:
    card_language:
    data_display_language:
  interaction:
    control_language:
    carousel_or_scroll_behavior:
    motion_cues:
  responsive:
    section_contract_ids: []
    shared_content_policy:
    breakpoint_states: {}
    allowed_transformations: []
    prohibited_viewport_rewrites: []
  evidence:
    customer_brand:
    structure_source:
    visual_references: []
    competitor_or_category: []
    target_theme: []
  source_precedence:
    - customer_confirmed_brand_and_requirements
    - approved_scoped_override
    - active_project_master_rules
    - evidence_backed_candidate
  project_invariants: []
  page_overrides:
    page_or_section_id:
      scope:
      changed_fields: []
      reason:
      evidence: []
      approval_state: proposed | approved | rejected
      approval_record:
  candidate_decisions: []
  conflict_check:
    status: pending | pass | needs_resolution | blocked
    findings: []
  revision_log: []
  prohibited_defaults: []
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
    screenshot_status: pending | pass | needs_revision
```

## Authority and override rules

- This contract is the project visual authority, not a generic style recommendation. Persist it in the production manifest and reuse it across pages and later revisions.
- Apply source precedence only inside each source's assigned role. Customer-confirmed brand/VI and requirements are binding. An approved page override outranks master rules only for its named scope and fields. Active project master rules govern everything else. Retrieved recommendations, competitor observations, and creative inferences remain candidates until deliberately accepted.
- Structure sources can bind selected layout relationships; target-theme sources can bind implementation feasibility. Neither source role may silently replace the customer's brand identity, copy, or product truth.
- Do not overwrite an active authority because a search produced a new style, palette, font pair, animation recipe, or component pattern. Record the proposal under `candidate_decisions`, run the conflict check, and either reject it, approve a scoped override, or revise the master rules explicitly.
- A page override must contain only deviations. It records exact scope, changed fields, reason, evidence, approval state, and approval record. Missing fields continue to inherit the project master.
- A project-wide rule change increments `authority_version`, appends the old and new values plus reason to `revision_log`, and invalidates every dependent variable, style, representative composition, component, and page for targeted review.

## Conflict check

Before representative Figma production, check at minimum:

- brand color role versus contrast, surface hierarchy, and supplied Logo usage;
- typography character versus website language, real font availability, hierarchy, and readability;
- structure-reference identity versus customer identity and selected-module scope;
- desired topology or interaction versus evidenced Shopify/WordPress theme capability and engineering route;
- imagery direction and crop versus available or permitted temporary assets;
- density and spacing rhythm versus actual content volume and page responsibility;
- interaction or motion cue versus purpose, usage frequency, platform behavior, performance, and reduced-motion equivalent;
- proposed page override versus project invariants and already-built dependent components.

Mark `pass` only after contradictory candidates are resolved into one coherent direction. Missing evidence is an explicit gap, not permission to fall back to a generic default.

## Candidate and signature gate

- For `logo_and_color`, `logo_only`, or `no_brand_assets`, record at least two compact internal candidates before selecting the primary direction. They must differ in at least four of the seven visual-signature dimensions; changing only color or copy does not create a second direction.
- Run the default-risk audit before selection. When three or more unsupported familiar defaults form one safe bundle, create a third materially different candidate and select from evidence rather than convenience.
- Do not build two complete Figma pages. Compare candidates through the contract and, only when necessary, small representative sketches. Carry only the selected candidate into representative Section families.
- Accept a project-specific creative inference only when it names the product/audience/journey/content/asset/implementation fact that motivated the choice and explains why the alternative fits less well.
- Reject generic rationales such as `premium`, `modern`, `editorial`, `minimal`, `conversion best practice`, `common DTC pattern`, or model preference when they stand alone.
- Treat typography, first-screen topology, page rhythm, and component grammar as identity-bearing. Do not reuse a high-character font, split-hero formula, numbered-trio sequence, pill/rounded-card system, or fixed FAQ/CTA ending without project evidence.
- Mark the gate `needs_resolution` when any signature dimension lacks evidence or when the two candidates collapse to the same fixed combination.
- Mark the gate `needs_resolution` when the complete-page composition board reveals weak alignment, repetitive macro rhythm, uncontrolled color/media distribution, or a page that requires UI to redesign the first screen or reorder most Sections.

## Evidence rules

- Explain how each major decision relates to customer material, research, source composition, target-theme capability, or a clearly named creative inference.
- Keep source structure and theme capability evidence separate.
- Do not copy a competitor's brand identity, protected copy, or distinctive assets.
- Treat `logo_and_color` as a normal production input, not an exception. Use supplied brand assets first, verify contrast and digital usability, then build only the minimum project-local website system needed for the page.
- Treat `constrained_authoring` and `open_concept` as deliberate project work. Record which identity fields were supplied and which were authored; project-authored brand decisions are editable working direction, not customer-approved formal VI.
- When only one brand color exists, use neutral colors for most surfaces and the supplied color as the primary candidate accent. Add another saturated brand-like color only when customer material or an explicitly assigned visual reference supports it.
- When only a Logo exists, derive restrained candidates from its form and color, record the inference, and keep them easy to revise through variables and styles.
- Do not describe a project-local website color, type, spacing, or component system as the customer's formal VI.

## Route rules

- `theme_customization`: use evidenced native behavior where it preserves the approved design responsibility and explicitly name CSS, Liquid, new Section, app, or other custom expression required by each module. Choose the least complex route that preserves the design; native availability is not a requirement to accept material visual loss. Do not apply a universal custom-work ratio.
- `custom`: define an original visual system without theme-module constraints.
- `hybrid_led` with `selected_structure_modules`: preserve only the selected modules' responsibility and layout relationships; do not promote the whole competitor page to a production requirement.
- `research_led`: derive hierarchy and expression from product, category, competitors, and journey evidence.
- `custom_led`: define an original visual system from requirements, research, references, and available brand inputs without theme-module constraints.
