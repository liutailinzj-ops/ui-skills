# Input Contract

## Customer facts

Request only these five categories:

| 类别 | 最少内容 | 是否阻塞 |
| --- | --- | --- |
| 品牌信息 | 品牌或项目名称；有 Logo、现有网站或品牌文件时一并提供 | 品牌身份必需；完整 VI 可缺失 |
| 产品品类 | 经营的产品或服务类型 | 必需 |
| 目标市场 | 国家/地区，以及面向消费者还是企业客户 | 必需 |
| 现有资料 | Logo、文案、图片、目录、视频、产品数据或品牌资料；“无”也是有效答案 | 不阻塞 |
| 竞品与参考 | 竞品网站和客户认为不错的网站；只提供链接即可 | 不阻塞；AI 可补充调研 |

Do not ask the customer to define page sections, CTA strategy, components, detailed visual terminology, platform constraints, or a priority product.

## Internal project facts

Obtain these from sales, project owner, UI, or engineering:

- Shopify or WordPress.
- Template, theme customization, or fully custom.
- DTC, B2B, or mixed.
- Contracted page and feature scope.
- Website language and market.
- Theme store, vendor documentation, demo, or current-site URL when applicable.
- Target Figma file or authorization to create one.
- Whether missing material may use temporary assets.
- Explicit role for each URL: specified structure, theme capability, competitor evidence, or visual inspiration.
- Fidelity expectation for specified-reference work. Infer theme adaptation from ordinary “按结构用主题做”; use strict replication only for explicit 1:1/exact/no-change requests.
- Available catalog or product records for PDP work; a complete catalog is not required.
- Whether the customer will receive a full Figma file or only preview frames/exports.

For template and theme-customization routes, obtain theme evidence internally. Do not ask the customer to research theme capabilities.

## Accepted launch package

UI may provide Chinese natural language instead of enums:

```text
客户资料：{飞书链接、文件或文字}
客户素材：{目录、网盘链接或“无”}
内部项目范围：{平台、建站方式、页面范围、网站语言}
指定结构网站：{需要按内容和布局转换的网站；没有则写“无指定”}
主题能力资料：{主题商店、开发商文档、演示站或现有网站；未选择则写“允许 AI 选择”}
竞品研究网站：{客户竞品或“由 AI 补充”}
视觉参考网站：{只参考风格的网站；没有则写“无”}
参考要求：{由我们策划 / 按指定网站结构 / 只参考部分模块 / 只参考视觉 / 基于旧站改版}
主题情况：{未选择 / 只有预览 / 已购买 / 现有网站}
目标 Figma：{链接或允许新建}
本次页面：{页面名称}
内容模式：{正式内容 / 混合内容 / 占位内容}
客户是否会获得完整 Figma 文件：{是 / 否}
```

When UI writes “按 A 的结构用 B 主题做”, normalize A into `structure_source_urls` and B into `theme_capability_urls`. Ask one short clarification only if the sentence is genuinely ambiguous.
