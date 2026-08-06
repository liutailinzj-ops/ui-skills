# PDP Coverage

A PDP design represents a template system, not one fixed product screenshot.

## Inspect the Catalog

Use available product records, catalog files, the current site, or supplied examples. Do not require a complete catalog. Group products by layout-relevant differences such as:

- Simple product versus variant-heavy product.
- Short versus long product title and option labels.
- One image versus rich gallery/video.
- Minimal versus deep benefits, specifications, ingredients, sizing, compatibility, or documentation.
- One-time purchase versus subscription, bundle, sample, or RFQ.
- Consumer storytelling versus technical/B2B decision support.
- Complete content versus placeholder-heavy content.

Choose a primary representative product plus at least two different or edge states when available. Do not choose three nearly identical products merely to satisfy the count.

## Product Coverage Matrix

```yaml
product_archetypes:
  - id:
    representative_product:
    content_depth:
    options:
    media_state:
    special_requirements: []
modules:
  - section_id:
    base_required: true | false
    visible_for: []
    hidden_for: []
    content_fallback:
    layout_effect_when_absent:
validation:
  primary_full_page:
  additional_states: []
  unresolved_states: []
```

## Template Strategy

Use one of these results:

- `single_template_validated`: one base template survives the approved representative and edge states through conditional blocks, content-driven height, and editable properties.
- `template_family`: materially different product types require multiple assignable templates, and the theme/platform supports the assignments.
- `coverage_partial`: product evidence is too limited to claim catalog-wide coverage. Build a safe base and list the untested states.

Do not create multiple templates merely because products have different text or images. Create a template family only when information responsibilities or interaction differ materially.

## PDP Layout Rules

- Keep the purchase area stable while allowing title, price, variants, badges, subscription, shipping, and CTA states to grow or collapse safely.
- Make below-fold modules conditional when their content is product-specific.
- Define what happens when a module has no content; do not leave empty bands.
- Validate long titles, option wrapping, absent ratings, different gallery counts, missing proof, and Mobile stacking.
- For theme-based work, every conditional state and additional template must have evidenced theme support.

The Figma client preview may show one primary product, but the internal validation must test the additional states before declaring the template reusable.
