# Reference Routing

Classify each supplied site before using it. A URL alone does not define how closely the result should follow it. Record its source role, reference mode, and fidelity profile.

## Source roles

- `structure_source`: the page that defines Build Truth. Its identity, content inventory, section order, and responsive anatomy drive the target.
- `theme_capability`: theme store, vendor documentation, demo, or current-site evidence used only to prove Section, Block, Settings, and responsive behavior.
- `competitor_evidence`: category and conversion research evidence.
- `visual_inspiration`: art-direction evidence.

The role invariant is strict: `theme_capability` never becomes `structure_source` unless the user explicitly selected the same URL for both. Preserve the role assignment across research, mapping, Figma build, and QA.

## Modes

### `reference_to_theme`

Use only when the reference page itself is an explicitly exact/no-change content-and-layout target. Pair it with `strict_replication` and follow [reference-to-theme.md](reference-to-theme.md). This is a low-freedom conversion workflow, not page strategy.

Require exactly one primary `structure_source` per page conversion. Multiple URLs may supply theme capability or competitor evidence, but they may not overwrite the primary source.

### `structure_target`

Use when the client expects the selected Shopify or WordPress theme to represent the reference page's content structure and layout logic while remaining theme-feasible. Pair it with `theme_adaptation` by default.

Build a Reference Content-Layout Matrix:

```yaml
reference:
  url:
  page_type:
  desktop_checked: true | false
  mobile_checked: true | false
sections:
  - source_id:
    order:
    responsibility:
    content_types: []
    required_fields: []
    desktop_anatomy:
    mobile_anatomy:
    interaction:
    optionality: always | conditional | product_specific
    priority: critical | structural | presentational
    target_theme_section:
    target_theme_blocks: []
    disposition: preserved | adapted | omitted
    mapping_status: exact_native | composed_native | native_adaptation | requires_custom | unresolved
    adaptation_state: not_applicable | proposed_adaptation | approved_adaptation | rejected_adaptation
    implementation_level:
    divergence_reason:
```

Analyze the source in this order:

1. Identify what question or decision each section serves.
2. Inventory the content required to make the section work.
3. Describe layout anatomy: column ratio, media position, content grouping, order, repetition, and interaction.
4. Inspect Desktop and Mobile as paired states of the same source Sections. Record differences without splitting their identity or content contract.
5. Map the responsibility and anatomy to an evidenced theme section/block.
6. Preserve it exactly or select the closest evidenced theme-native adaptation. Omit only when it is irrelevant, out of scope, or explicitly approved; missing material alone should use a placeholder.

Do not copy source text, branded imagery, proprietary graphics, or a distinctive visual identity. Structural fidelity is not asset copying.

## `visual_inspiration`

Extract visual principles only: hierarchy, density, image treatment, whitespace, typography, card language, and section rhythm. The final page may use a different content sequence.

## `competitor_evidence`

Extract category evidence: buying questions, product education, proof, objections, comparisons, navigation, and conversion paths. Use repeated patterns as evidence, not as a page to trace.

## Fidelity Result

## Fidelity profiles

- `strict_replication`: exact content, order, composition groups, topology, interaction, and Desktop/Mobile transformation. An unresolved or unapproved difference blocks before Figma.
- `theme_adaptation`: preserve complete source inventory, critical content/function, order, composition intent, and reading flow; allow evidenced native differences in columns, visible counts, section boundaries, interaction form, spacing, crop, and micro-layout. Continue to editable Figma and route proposed differences to UI review.

For `structure_target`, report:

- Responsibility coverage: source responsibilities represented / relevant source responsibilities.
- Order divergences and reasons.
- Layout-anatomy divergences and reasons.
- Theme substitutions.
- Omissions caused by missing customer content.
- Exact-native, composed-native, native-adaptation, and requires-custom counts.
- Proposed adaptations awaiting UI review; do not label them approved.

Do not claim close reference fidelity when only colors, typography, or section names are similar.

For every fidelity result, print the role table with URL, Chinese role, permitted use, and actual artifact consuming it. If an artifact consumed a URL outside its permitted role, mark `blocked_source_identity`.
