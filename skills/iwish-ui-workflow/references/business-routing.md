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

## Chinese intent mapping

- “没有指定结构、由我们策划、根据品类设计” -> `research_led`.
- “按这个网站的内容和布局做、照结构做” -> `reference_led` plus `reference_to_theme` for theme routes.
- “参考这个网站的结构逻辑” -> `reference_led` plus `structure_target`.
- “只参考其中几个模块、多个网站组合” -> `hybrid_led`; classify every selected section separately.
- “只参考视觉、感觉、风格” -> `visual_inspiration` without section fidelity.
- “基于客户旧站改版” -> `existing_site_led`.

`strategy_mode` controls where page strategy comes from. `build_route` controls implementation freedom. `site_model` controls DTC/B2B analysis. Do not multiply these into separate duplicated workflows.

## Route behavior

- `research_led`: let product, category, competitor, and journey analysis determine the hierarchy. Select or audit a theme after analysis.
- `reference_led`: analyze the product and market, then translate the specified source at the approved fidelity. Report relevance or conversion risks without silently restructuring it.
- `hybrid_led`: preserve explicitly selected reference sections; use analysis to design the remaining responsibilities.
- `existing_site_led`: inventory current content, URLs, useful proof, and reusable assets; use analysis to decide what to retain, revise, relocate, or replace.

For `template`, remain inside native/configuration/style scope. For `theme_customization`, apply the approved custom budget. For `custom`, use analysis, requirements, references, VI, and platform feasibility without theme-module constraints.

## Chinese Project Recognition Card

Display this compact card once, then continue unless a blocking ambiguity exists:

```text
项目识别结果
网站类型：DTC / B2B / 混合
平台：Shopify / WordPress
建站方式：模板建站 / 模板二开 / 纯定制
设计方式：自主策划 / 指定结构 / 混合参考 / 旧站改版
主题状态：待选择 / 只有预览 / 已有代码 / 现有网站
内容状态：正式 / 部分占位 / 占位
参考网站作用：无 / 竞品研究 / 指定结构 / 部分模块 / 视觉参考
本次页面：{page}
接下来：{analysis and build sequence}
```

Keep internal enum values out of this user-facing card.
