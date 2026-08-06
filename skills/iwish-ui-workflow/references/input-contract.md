# Input Contract

## Customer facts

Request only these five categories:

| Category | Minimum content | Blocking |
| --- | --- | --- |
| Brand information | Brand/project name; existing logo, site, or brand files when available | Identity is required; assets may be absent |
| Product category | What kind of product or service the business provides | Required |
| Target market | Country/region and whether the audience is consumers or business buyers | Required |
| Existing materials | Any logo, copy, images, catalog, video, product data, or brand documents; `none` is valid | Not blocking |
| Competitors/references | Competitor sites and sites the customer considers good; links alone are enough | Not blocking; AI may supplement research |

Do not ask the customer to define page sections, CTA strategy, component requirements, detailed visual terminology, technical platform constraints, or a priority product.

## Internal project facts

Obtain these from sales, the project owner, UI, or engineering:

- Shopify or WordPress.
- Template, theme customization, or fully custom.
- Theme/demo/current-site URL when applicable.
- Contracted page and feature scope.
- DTC, B2B, or mixed business route.
- Languages/markets already agreed.
- Target Figma file or authorization to create one.
- Whether missing material may use placeholders.
- Reference intent for each supplied site: `structure_target`, `visual_inspiration`, or `competitor_evidence`. Infer this from the brief or confirm internally; do not ask the customer to provide a design analysis.
- For PDP work, available catalog/product records and known product differences. A complete catalog is not required.

For `template` and `theme_customization` routes, the theme/demo/current-site reference is required before page strategy can approve implementation mappings. Obtain it internally; do not ask the customer to research the theme.

## Accepted launch package

```text
client_facts: file, link, or text
client_assets: folder/link or none
internal_scope: file, link, or text
theme_reference: URL or none
figma_target: design URL or create_new
requested_page: one page per initial build
content_mode: final | mixed | placeholder
reference_mode: structure_target | visual_inspiration | competitor_evidence | none
```
