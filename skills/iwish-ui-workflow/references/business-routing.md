# Business Routing

Infer the route from natural-language project facts. Do not require UI to remember enum values.

## Internal dimensions

```yaml
site_model: dtc | b2b | mixed
build_route: template | theme_customization | custom
strategy_mode: research_led | reference_led | hybrid_led | existing_site_led
theme_state: to_be_selected | demo_only | code_available | current_site
content_state: final | mixed | placeholder
```

Use these Chinese labels in every user-facing field, recognition card, question, and handoff summary:

| Chinese label | Internal value | Meaning |
| --- | --- | --- |
| 正式内容 | `final` | Customer images, copy, and product information are largely usable |
| 混合内容 | `mixed` | Real customer material and temporary content are used together |
| 占位内容 | `placeholder` | Material is insufficient, so build a complete reviewable structure with safe temporary content |

Never display the internal values as options for UI.

## Chinese intent mapping

- “没有指定结构、由我们策划、根据品类设计” -> `research_led`.
- “按这个网站的内容和布局做、照结构做” -> `reference_led` plus `reference_to_theme` for theme routes.
- “参考这个网站的结构逻辑” -> `reference_led` plus `structure_target`.
- “只参考其中几个模块、多个网站组合” -> `hybrid_led`; classify every selected section separately.
- “只参考视觉、感觉、风格” -> `visual_inspiration` without section fidelity.
- “基于客户旧站改版” -> `existing_site_led`.

`strategy_mode` controls where page strategy comes from. `build_route` controls implementation freedom. `site_model` controls DTC/B2B analysis. Do not multiply these into separate duplicated workflows.

## Source role routing

Assign URLs by purpose before using them:

| Chinese role | Manifest field | Permitted use |
| --- | --- | --- |
| 指定结构来源 | `structure_source_urls` | Defines Build Truth: page identity, content inventory, section order, and Desktop/Mobile layout anatomy |
| 主题能力来源 | `theme_capability_urls` | Proves available theme Section, Block, Settings, and responsive behavior only |
| 竞品研究来源 | `competitor_evidence_urls` | Supports product/category and conversion analysis only |
| 视觉参考来源 | `visual_inspiration_urls` | Supports art direction only |

Do not infer role from domain, visual similarity, or which URL was inspected most recently. A URL may hold two roles only when the user explicitly assigns both. In that case, record both roles separately. Never promote a theme demo to 指定结构来源 automatically.

## Route behavior

- `research_led`: let product, category, competitor, and journey analysis determine the hierarchy. Select or audit a theme after analysis.
- `reference_led`: analyze the product and market, then translate the specified source at the approved fidelity. Report relevance or conversion risks without silently restructuring it.
- `hybrid_led`: preserve explicitly selected reference sections; use analysis to design the remaining responsibilities.
- `existing_site_led`: inventory current content, URLs, useful proof, and reusable assets; use analysis to decide what to retain, revise, relocate, or replace.

For `template`, remain inside native/configuration/style scope. For `theme_customization`, apply the approved custom budget. For `custom`, use analysis, requirements, references, VI, and platform feasibility without theme-module constraints.

The route changes how topology gaps are handled, not whether they are detected:

- `template`: block any unapproved topology that exact native settings cannot reproduce.
- `theme_customization`: identify the exact missing topology or interaction, estimate its custom count and height budget, and require approval when the route gate is crossed.
- `custom`: preserve strict-reference topology when requested; otherwise let research and brand strategy define it.

Do not inherit a section count, product vocabulary, component family, or visual language from a regression fixture.

## Chinese Project Recognition Card

Display this compact card once, then continue unless a blocking ambiguity exists:

```text
项目识别结果
网站类型：DTC / B2B / 混合
平台：Shopify / WordPress
建站方式：模板建站 / 模板二开 / 纯定制
设计方式：自主策划 / 指定结构 / 混合参考 / 旧站改版
主题状态：待选择 / 只有预览 / 已有代码 / 现有网站
内容模式：正式内容 / 混合内容 / 占位内容
来源角色：
- 指定结构来源：{URL 或“无”}
- 主题能力来源：{URL 或“无 / 待选择”}
- 竞品研究来源：{URL 列表或“由 AI 补充”}
- 视觉参考来源：{URL 列表或“无”}
本次页面：{page}
接下来：{analysis and build sequence}
```

Keep internal enum values out of this user-facing card.
