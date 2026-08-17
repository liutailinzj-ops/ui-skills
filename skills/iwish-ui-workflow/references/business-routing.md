# Business Routing

Infer the route from natural-language project facts. Do not require UI to remember enum values.

## Internal dimensions

```yaml
site_model: dtc | b2b | mixed
production_scenario: research_led_theme_customization | selected_modules_theme_customization | custom
build_route: theme_customization | custom
strategy_mode: research_led | hybrid_led | custom_led
theme_state: to_be_selected | demo_only | code_available | current_site
content_state: final | mixed | placeholder
brand_input_state: full_vi | logo_and_color | logo_only | no_brand_assets
reference_mode: selected_structure_modules | visual_inspiration | competitor_evidence | none
fidelity_profile: theme_adaptation | not_applicable
```

Use these Chinese labels in every UI-facing field:

| 中文标签 | 内部值 | 含义 |
| --- | --- | --- |
| 正式内容 | `final` | 客户图片、文案和产品信息基本可用 |
| 混合内容 | `mixed` | 客户真实资料与临时内容混合使用 |
| 占位内容 | `placeholder` | 资料不足，使用可替换内容完成可评审设计 |

## Chinese intent mapping

- “只有 Logo/品牌色，没有指定结构，由我们策划” -> `research_led_theme_customization` + `research_led` + `theme_customization`.
- “只有 Logo/品牌色，参考竞品的部分模块、只做这几个结构、多个网站组合” -> `selected_modules_theme_customization` + `hybrid_led` + `theme_customization` + `selected_structure_modules`.
- “纯自定义、没有主题模块约束” -> `custom` + `custom_led` + `custom`.
- “只参考视觉、感觉、风格” -> `visual_inspiration`.

`production_scenario` is the single UI-facing route. The other values are derived internally. Do not ask UI to choose multiple technical dimensions.

## Source roles

| 中文角色 | Manifest 字段 | 用途 |
| --- | --- | --- |
| 指定结构来源 | `structure_source_urls` | 仅对清单中明确选择的竞品模块定义结构证据 |
| 主题能力来源 | `theme_capability_urls` | 证明目标主题的 Section、Block、Setting 和响应式能力 |
| 竞品研究来源 | `competitor_evidence_urls` | 支持产品、行业和转化逻辑研究 |
| 视觉参考来源 | `visual_inspiration_urls` | 支持视觉方向，不自动成为结构目标 |

Never promote a theme demo to the structure source unless the user explicitly assigns that role.

## Route behavior

- `research_led_theme_customization`: derive the page hierarchy from product, category, competitor, and journey evidence, then select and customize a suitable theme.
- `selected_modules_theme_customization`: preserve only the named selected reference modules and design all remaining responsibilities from research.
- `custom`: create an original page system from requirements, research, references, and available brand inputs.

For `theme_customization`, inspect evidenced native capability, then classify configuration, style, CSS, Liquid, new Sections, apps, or other custom work per module. Choose the least complex route that preserves the approved design responsibility; do not lower visual fidelity merely to stay native. Do not enforce a universal custom-section percentage; use the contracted scope and engineering feasibility. For `custom`, use research, requirements, references, brand inputs, and platform feasibility without theme-module constraints.

## Chinese Project Recognition Card

Display once, then continue unless a blocking ambiguity exists:

```text
项目识别结果
网站类型：DTC / B2B / 混合
平台：Shopify / WordPress
建站方式：模板部分二开 / 纯定制
项目场景：自主策划 + 模板部分二开 / 指定竞品部分结构 + 模板部分二开 / 纯定制
参考方式：无指定结构 / 只转换选中模块 / 不适用
主题状态：待选择 / 只有预览 / 已有代码 / 现有网站
内容模式：正式内容 / 混合内容 / 占位内容
品牌资料：完整 VI / Logo + 品牌色 / 只有 Logo / 无品牌素材
网站语言：{language}
来源角色：
- 指定结构来源：{URL + 选中模块清单 / 无}
- 主题能力来源：{URL 或“无 / 待选择”}
- 竞品研究来源：{URL 列表或“由 AI 补充”}
- 视觉参考来源：{URL 列表或“无”}
本次页面：{page}
接下来：产品与竞品分析 → 页面策略 → 视觉方向 → Figma 生成 → 后台内部检查
```

Keep enum values and evaluation case information out of this card.
