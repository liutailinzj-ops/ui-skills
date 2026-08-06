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
- Theme store, vendor documentation, demo, or current-site URL used to prove theme capability when applicable.
- Contracted page and feature scope.
- DTC, B2B, or mixed business route.
- Languages/markets already agreed.
- Target Figma file or authorization to create one.
- Whether missing material may use placeholders.
- Source role for each supplied URL: specified structure source, theme capability source, competitor evidence, or visual inspiration. Keep roles separate even when URLs arrive in one reference list. Use `reference_to_theme` only when the specified source's content inventory, order, and layout anatomy are approved targets.
- Strategy source: `research_led`, `reference_led`, `hybrid_led`, or `existing_site_led`. Infer it from Chinese instructions; UI does not need to provide the enum.
- Theme state: `to_be_selected`, `demo_only`, `code_available`, or `current_site`.
- Content mode: ask UI to use `正式内容`, `混合内容`, or `占位内容`. Normalize these internally to `final`, `mixed`, or `placeholder`.
- For PDP work, available catalog/product records and known product differences. A complete catalog is not required.

For `template` and `theme_customization` routes, the theme/demo/current-site reference is required before page strategy can approve implementation mappings. Obtain it internally; do not ask the customer to research the theme.

## Accepted launch package

```text
client_facts: file, link, or text
client_assets: folder/link or none
internal_scope: file, link, or text
structure_source_urls: URLs or none
theme_capability_urls: theme store/vendor docs/demo/current site URLs or none
competitor_evidence_urls: URLs or AI research
visual_inspiration_urls: URLs or none
figma_target: design URL or create_new
requested_page: one page per initial build
content_mode: final | mixed | placeholder
reference_mode: reference_to_theme | structure_target | visual_inspiration | competitor_evidence | none
strategy_mode: research_led | reference_led | hybrid_led | existing_site_led
theme_state: to_be_selected | demo_only | code_available | current_site
```

For `reference_to_theme`, also record whether reference text and media may appear temporarily in the client preview. This permission does not make competitor material customer-owned or production-approved.

UI may use Chinese natural language instead of the enum fields:

```text
客户资料：{文件、飞书链接或文字}
客户素材：{目录、网盘链接或“无”}
内部项目范围：{平台、建站方式、页面范围}
指定结构网站：{需要照内容结构和布局转换的网站；没有则写“无指定”}
主题能力资料：{主题商店、开发商文档、演示站或现站链接；未选择则写“允许 AI 选择”}
竞品研究网站：{客户竞品或“由 AI 补充”}
视觉参考网站：{只参考风格的网站；没有则写“无”}
参考要求：{由我们策划 / 按指定网站结构 / 只参考部分模块 / 只参考视觉 / 基于旧站改版}
主题情况：{未选择 / 只有预览 / 已购买 / 现有网站}
目标 Figma：{链接或允许新建}
本次页面：{页面}
内容模式：{正式内容 / 混合内容 / 占位内容}
```

Do not expose `final`, `mixed`, or `placeholder` in a user-facing launch template or clarification question.

When UI writes “按 A 的结构用 B 主题做”, normalize A into `structure_source_urls` and B into `theme_capability_urls`. Do not store both in one `theme_reference` field. If the sentence is genuinely ambiguous, ask one short internal clarification before analysis.
