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
- Research-led partial theme customization, selected competitor-module partial theme customization, or fully custom.
- DTC, B2B, or mixed.
- Contracted page and feature scope.
- Website language and market.
- Theme store, vendor documentation, demo, or current-site URL when applicable.
- Target Figma file or authorization to create one.
- Whether missing material may use temporary assets.
- Explicit role for each URL: selected structure modules, theme capability, competitor evidence, or visual inspiration.
- Selected module names or screenshots when only part of a competitor page is required. Natural-language descriptions are sufficient.
- For selected-reference work, confirm which modules are selected; the default is theme adaptation plus scoped custom implementation, not full-page replication.
- Available catalog or product records for PDP work; a complete catalog is not required.
- Whether the customer will receive a full Figma file or only preview frames/exports.

For theme-customization routes, obtain theme evidence internally. Do not ask the customer to research theme capabilities.

## Accepted launch package

UI may provide Chinese natural language instead of enums:

```text
客户资料：{飞书链接、文件或文字}
客户素材：{目录、网盘链接或“无”}
内部项目范围：{平台、建站方式、页面范围、网站语言}
指定结构网站：{只需要转换其中部分模块的网站；没有则写“无指定”}
指定参考模块：{填写模块名称、截图或描述；无指定时可省略}
主题能力资料：{主题商店、开发商文档、演示站或现有网站；未选择则写“允许 AI 选择”}
竞品研究网站：{客户竞品或“由 AI 补充”}
视觉参考网站：{只参考风格的网站；没有则写“无”}
项目场景：{自主策划 + 模板部分二开 / 指定竞品部分结构 + 模板部分二开 / 纯定制}
主题情况：{未选择 / 只有预览 / 已购买 / 现有网站}
目标 Figma：{链接或允许新建}
本次页面：{页面名称}
内容模式：{正式内容 / 混合内容 / 占位内容}
客户是否会获得完整 Figma 文件：{是 / 否}
```

When UI writes “按 A 的结构用 B 主题做”, normalize B into `theme_capability_urls` and ask which A modules are selected when the module scope is missing. Do not silently convert the whole A page into a production requirement.
