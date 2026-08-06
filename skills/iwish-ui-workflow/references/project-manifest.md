# Project Manifest

Maintain one state object throughout the workflow:

```yaml
project:
  name:
  brand:
  product_category:
  target_market:
  audience_type: dtc | b2b | mixed
  platform: shopify | wordpress
  build_route: template | theme_customization | custom
scope:
  requested_page:
  features: []
sources:
  customer_facts:
  customer_assets:
  competitor_urls: []
  reference_urls: []
  reference_modes: {}
  theme_reference:
theme:
  name:
  preset:
  capability_map:
  evidence_urls: []
  custom_section_count_ratio:
  custom_section_height_ratio:
  route_gate: pass | blocked
figma:
  file_key:
  file_url:
  pages: {}
  frames: {}
  components: {}
  variables: {}
  client_preview_frames: {}
  handoff_nodes: {}
content:
  mode: final | mixed | placeholder
  placeholders: []
pdp:
  product_sources: []
  product_archetypes: []
  representative_products: []
  coverage_matrix:
  template_strategy: single_template_validated | template_family | coverage_partial
  template_assignments: []
reference_fidelity:
  target_url:
  content_layout_matrix:
  responsibility_coverage:
  order_divergences: []
  layout_divergences: []
workflow:
  completed: []
  pending_validations: []
qa:
  text_style_binding:
  grid_integrity:
  equal_height_groups:
  mobile_overflow:
  client_preview_separation:
risks: []
```

Persist exact Figma node IDs returned by tools. Never guess or reconstruct IDs. Resume from this manifest after interruption.

For theme-based work, keep one mapping record per page section with the exact theme section/block, evidence URL, implementation level, divergence, approval, and owner.

For `structure_target` work, keep one correspondence record per source section: source responsibility, source content type, source Desktop/Mobile layout anatomy, target theme mapping, preserved/adapted/omitted status, and reason.

For PDP work, record which product archetypes were tested. `single_template_validated` requires evidence that the base template survives the approved representative and edge states; otherwise use `template_family` or `coverage_partial`.
