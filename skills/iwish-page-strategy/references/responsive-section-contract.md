# Responsive Section Contract

Use one responsive contract for every page section. Desktop and Mobile are breakpoint previews of the same section system, not separate creative deliverables.

## Contract

```yaml
responsive_sections:
  - section_id:
    source_section_id:
    order:
    component_family:
    shared:
      responsibility:
      content_bindings: []
      theme_section:
      theme_blocks: []
      alignment_group_id:
      container_mode:
    breakpoints:
      desktop:
        viewport_width:
        theme_settings: {}
        layout_state:
        media_state:
        repetition_state:
        interaction_state:
      mobile:
        viewport_width:
        theme_settings: {}
        layout_state:
        media_state:
        repetition_state:
        interaction_state:
    allowed_differences: []
    content_variants: []
    overflow_contract:
      mode: none | clip | scroll | carousel | visible
      evidence:
      affordance:
    evidence_urls: []
```

## Shared identity

- Keep `section_id`, source correspondence, responsibility, content bindings, order, component family, and theme Section/Blocks shared across breakpoints.
- Keep customer-facing copy and controls shared by default. Do not rewrite headings, body copy, labels, or CTAs merely to make Mobile easier to compose.
- Allow a breakpoint-specific content variant only when the customer requirement or evidenced theme behavior requires it. Record the exact field, reason, evidence, and fallback.
- Preserve connected composition groups and transaction flow across breakpoints.

## Breakpoint behavior

- Record only responsive differences: stacking, order within the same section, columns, media ratio, crop, visible item count, swipe/carousel behavior, navigation treatment, spacing, and controls.
- For `theme_customization`, use documented theme behavior for native/configured Sections and an explicit responsive implementation plan for custom Sections. Do not present an invented Mobile composition as native theme behavior.
- For `custom`, define intentional breakpoint behavior, but keep one section/component identity and shared content contract.
- Treat Desktop and Mobile Figma frames as rendered verification states. Do not use them as permission to create unrelated layouts, copy, or component families.

## Figma representation

- Resolve one component family per responsive section. Use Auto Layout, shared nested components, and the smallest necessary `Viewport=Desktop|Mobile` variants.
- Keep shared text/media properties and content-slot names identical across viewport variants.
- Build one section family first, then place its Desktop and Mobile instances into preview frames.
- Record the paired instance IDs in the manifest so QA can compare them directly.
- Do not detach one viewport instance to finish it independently.

## Alignment contract

- Define page gutter, maximum container width, spacing scale, and named alignment groups before section production.
- Give every major section edge an `alignment_group_id`. Nodes in the same group must share left and right edges within 1 px at the same breakpoint.
- Allow `full_width`, `standard`, `narrow`, or another container mode only when the project foundation or theme evidence defines it. A different margin is not a creative exception by itself.
- Prefer grid-derived or `FILL` widths. Reject manually rounded fixed widths that leave an unexplained remainder.

## Overflow contract

- Default to `none`.
- Treat a child outside a clipping parent as an error unless the section declares an evidenced carousel, scroll, clip, or visible-overflow contract with an affordance.
- Never use clipping to conceal incorrect fixed heights, text reflow, card widths, or missing content.

## Parity gate

Before page production or handoff, compare each paired breakpoint instance:

- Section identity, order, content bindings, controls, and shared copy match.
- Every difference appears in `allowed_differences` and is supported by theme evidence or the custom responsive plan.
- Alignment groups pass within 1 px.
- No child is accidentally clipped, outside its parent, or hidden by a fixed-height wrapper.
- Internal QA, source, implementation, or replacement notes are absent from both customer-preview states.
