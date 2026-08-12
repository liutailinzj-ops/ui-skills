# Visual Direction Contract

Record a compact contract that is specific enough to guide page production without freezing creative judgment.

```yaml
visual_direction:
  brand_input_state: full_vi | logo_and_color | logo_only | no_brand_assets
  concept_statement:
  brand_character: []
  audience_impression:
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
  prohibited_defaults: []
```

## Evidence rules

- Explain how each major decision relates to customer material, research, source composition, target-theme capability, or a clearly named creative inference.
- Keep source structure and theme capability evidence separate.
- Do not copy a competitor's brand identity, protected copy, or distinctive assets.
- Treat `logo_and_color` as a normal production input, not an exception. Use supplied brand assets first, verify contrast and digital usability, then build only the minimum project-local website system needed for the page.
- When only one brand color exists, use neutral colors for most surfaces and the supplied color as the primary candidate accent. Add another saturated brand-like color only when customer material or an explicitly assigned visual reference supports it.
- When only a Logo exists, derive restrained candidates from its form and color, record the inference, and keep them easy to revise through variables and styles.
- Do not describe a project-local website color, type, spacing, or component system as the customer's formal VI.

## Route rules

- `theme_customization`: use evidenced native behavior where suitable and explicitly name CSS, Liquid, new Section, app, or other custom expression required by each module. Do not apply a universal custom-work ratio.
- `custom`: define an original visual system without theme-module constraints.
- `hybrid_led` with `selected_structure_modules`: preserve only the selected modules' responsibility and layout relationships; do not promote the whole competitor page to a production requirement.
- `research_led`: derive hierarchy and expression from product, category, competitors, and journey evidence.
- `custom_led`: define an original visual system from requirements, research, references, and available brand inputs without theme-module constraints.
