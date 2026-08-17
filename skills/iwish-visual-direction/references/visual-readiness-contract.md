# Visual Readiness Contract

Use this contract when customer VI, photography, renders, or product content is incomplete. Missing assets remove factual authority; they do not lower the expected visual fidelity of a client-review draft.

## Brand authorship modes

- `customer_led`: preserve supplied VI and author only missing execution details.
- `constrained_authoring`: preserve supplied brand name, Logo, brand color, and approved rules; author typography, supporting neutrals, form language, imagery, crop, density, layout posture, and interaction from current project evidence.
- `open_concept`: when the project or evaluation explicitly allows brand creation, create a project name, wordmark treatment, palette, typography, form language, imagery system, and creative thesis from the product, audience, market, and journey. Record every field as project-authored, not customer-approved.

Do not rename or recolor a supplied customer brand. Do not reuse the previous project's authored identity as a shortcut.

## Visual-asset coverage matrix

Create one row for every decision-critical media role:

```yaml
visual_asset:
  slot_id:
  communication_job:
  subject:
  environment:
  viewpoint:
  crop_and_ratio:
  product_scale:
  lighting_or_render_style:
  required_variation:
  source_class: customer | licensed | generated | attributed_internal_reference
  replacement_rule:
  asset_or_node_ids: []
```

The matrix must cover the first screen, product/configuration comparison, selected source modules with media, and at least one context or proof-oriented composition when those responsibilities exist.

## Asset independence

- Separate missing factual content from missing visual material. Do not invent performance, certification, price, review, warranty, or product-detail facts.
- Generate or license temporary product, context, crop, rendering, illustration, or diagram assets needed to make the design judgeable.
- Use the image-generation capability when a realistic or controlled product/context visual is required and no usable asset exists. Use editable Figma geometry for overlays, labels, hotspots, diagrams, and simple graphic systems, not as the automatic substitute for all photography or rendering.
- Track temporary provenance outside customer-preview frames and keep assets replaceable.

## Semantic differentiation

- Different configurations must visibly differ in module count, form, footprint, arrangement, or context.
- Different products must visibly differ in product form or state.
- Different features must use distinct product details, diagrams, contexts, or icons when the media carries the distinction.
- Different scenes must change environment, crop, lighting, product placement, or human/context cues.
- Reusing one image with new labels fails when the visual is supposed to explain the difference.

## Representative exit gate

Do not begin full-page production until screenshots prove:

1. the first-screen or primary conversion composition;
2. one module where content differences are visible rather than text-only;
3. one imagery-led or media-dense module with final intended crop, density, and product scale;
4. one responsive-risk transformation using the same content and component identity;
5. the selected brand direction is identifiable without reading internal rationale.

Return to visual direction when the result still reads as a wireframe, repeats generic geometry, could fit an unrelated product after text replacement, or leaves UI to decide the core media composition.
