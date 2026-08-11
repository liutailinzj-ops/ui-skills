# Business Routing

Infer the route from natural-language project facts. Do not require UI to remember enum values.

## Internal dimensions

```yaml
site_model: dtc | b2b | mixed
build_route: template | theme_customization | custom
strategy_mode: research_led | reference_led | hybrid_led | existing_site_led
theme_state: to_be_selected | demo_only | code_available | current_site
content_state: final | mixed | placeholder
reference_mode: reference_to_theme | structure_target | visual_inspiration | competitor_evidence | none
fidelity_profile: strict_replication | theme_adaptation
```

Use these Chinese labels in every UI-facing field:

| 中文标签 | 内部值 | 含义 |
| --- | --- | --- |
| 正式内容 | `final` | 客户图片、文案和产品信息基本可用 |
| 混合内容 | `mixed` | 客户真实资料与临时内容混合使用 |
| 占位内容 | `placeholder` | 资料不足，使用可替换内容完成可评审设计 |

## Chinese intent mapping

- “没有指定结构、由我们策划、根据品类设计” -> `research_led`.
- “按这个网站的内容和布局做、用主题模块转换” -> `reference_led` + `structure_target` + `theme_adaptation`.
- “1:1 还原、完全一致、不可调整、像素级复刻” -> `reference_led` + `reference_to_theme` + `strict_replication`.
- “只参考其中几个模块、多个网站组合” -> `hybrid_led`; classify selected sections separately.
- “只参考视觉、感觉、风格” -> `visual_inspiration`.
- “基于客户旧站改版” -> `existing_site_led`.

`strategy_mode` controls where page strategy comes from. `build_route` controls implementation freedom. `site_model` controls DTC/B2B analysis. Do not duplicate them into separate user workflows.

## Source roles

| 中文角色 | Manifest 字段 | 用途 |
| --- | --- | --- |
| 指定结构来源 | `structure_source_urls` | 定义页面身份、共享内容、顺序和响应式断点逻辑 |
| 主题能力来源 | `theme_capability_urls` | 证明目标主题的 Section、Block、Setting 和响应式能力 |
| 竞品研究来源 | `competitor_evidence_urls` | 支持产品、行业和转化逻辑研究 |
| 视觉参考来源 | `visual_inspiration_urls` | 支持视觉方向，不自动成为结构目标 |

Never promote a theme demo to the structure source unless the user explicitly assigns that role.

## Route behavior

- `research_led`: derive hierarchy from product, category, competitor, and journey evidence.
- `reference_led`: analyze product fit, then translate the specified source at the requested fidelity without silently changing it.
- `hybrid_led`: preserve selected reference sections and design remaining responsibilities from research.
- `existing_site_led`: decide what current content and proof to retain, revise, relocate, or replace.

For `template`, stay inside evidenced native/configuration/style scope. For `theme_customization`, respect the approved custom scope. For `custom`, use research, requirements, references, VI, and platform feasibility without theme-module constraints.

## Chinese Project Recognition Card

Display once, then continue unless a blocking ambiguity exists:

```text
项目识别结果
网站类型：DTC / B2B / 混合
平台：Shopify / WordPress
建站方式：模板建站 / 模板二开 / 纯定制
设计方式：自主策划 / 指定结构 / 混合参考 / 旧站改版
还原方式：严格复制 / 主题适配 / 不适用
主题状态：待选择 / 只有预览 / 已有代码 / 现有网站
内容模式：正式内容 / 混合内容 / 占位内容
网站语言：{language}
来源角色：
- 指定结构来源：{URL 或“无”}
- 主题能力来源：{URL 或“无 / 待选择”}
- 竞品研究来源：{URL 列表或“由 AI 补充”}
- 视觉参考来源：{URL 列表或“无”}
本次页面：{page}
接下来：产品与竞品分析 → 页面策略 → 视觉方向 → Figma 生成 → 后台内部检查
```

Keep enum values and evaluation case information out of this card.
