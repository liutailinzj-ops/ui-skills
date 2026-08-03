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
  theme_reference:
figma:
  file_key:
  file_url:
  pages: {}
  frames: {}
  components: {}
  variables: {}
content:
  mode: final | mixed | placeholder
  placeholders: []
workflow:
  completed: []
  pending_validations: []
risks: []
```

Persist exact Figma node IDs returned by tools. Never guess or reconstruct IDs. Resume from this manifest after interruption.

