# Asset Input Routing

Classify brand and product material independently before strategy. Do not infer design quality from material quantity.

## Primary matrix

| Customer state | Internal route | Production responsibility |
| --- | --- | --- |
| Brand assets present + product assets present | `brand_ready_product_ready` | Preserve approved brand rules and use approved product media first. Fill only page-specific gaps. |
| Brand assets present + product assets missing | `brand_ready_product_missing` | Preserve brand invariants; create a coherent temporary product/media system inside that brand. |
| Brand assets missing + product assets present | `brand_missing_product_ready` | Preserve product truth and media; author a reversible project website identity around the product, market, and journey. |
| Brand assets missing + product assets missing | `brand_missing_product_missing` | Author a reversible working brand and one consistent temporary product/media identity before page design. This is a stress route, not permission to lower fidelity. |

Treat partial product media as `product_assets_partial`, then resolve every decision-critical gap through the Visual-Asset Coverage Matrix. Treat Logo-only or Logo-plus-color as brand assets present but incomplete; preserve them and author only the missing system.

## Required manifest fields

```yaml
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
```

## Routing rules

- Inspect actual files, URLs, and Figma assets. A textual claim that a VI or product pack exists does not make it usable.
- Never redraw, recolor, rename, or reinterpret supplied brand invariants without approval.
- Never create a second product form for another Section. When product media is missing, define the temporary product identity once, then generate all views and scenes from that anchor.
- Missing material changes provenance, replacement work, and factual authority. It does not change the required page alignment, content specificity, visual hierarchy, or client-review fidelity.
- Do not ask the customer for page structure, detailed art direction, or marketing strategy. The five-category customer input contract remains sufficient.
- If temporary media is prohibited and a decision-critical visual role cannot be shown, report the exact blocked role instead of silently using an empty frame.

## Recognition output

Show these Chinese fields in the project-recognition card:

```text
品牌素材：完整 VI / Logo + 品牌色 / 只有 Logo / 无品牌素材
产品素材：可直接使用 / 部分可用 / 无产品素材
素材处理：继承品牌与产品 / 继承品牌并补临时产品视觉 / 保留产品并补网站品牌方向 / 创建工作品牌与统一临时产品视觉
```

Do not expose the internal route value to UI.
