# Figma File Contract

A Starter File is optional. The file contract is mandatory.

## Default pages for a blank internal working file

```text
00_项目与简报
01_研究与策略
02_视觉方向
03_基础样式
04_本地组件
10_Client Preview Desktop
11_Client Preview Mobile
90_参考资料
95_内部检查
99_归档
```

Reuse compatible existing pages instead of creating duplicates. Do not create `95_内部检查` unless internal Figma QA is explicitly requested.

If the customer receives the whole Figma file, use a separate customer file containing only cover and customer-preview pages. Keep research, references, internal QA, implementation notes, and replacement lists in the internal file.

## Default frames

- Desktop starting width: 1440.
- Mobile starting width: 390.
- Use project/theme container width when known.
- Use 12-column Desktop and 4-column Mobile grids as defaults, not immutable rules.

## Naming and language

```text
Page / Homepage / Desktop
Page / Homepage / Mobile
Section / Hero
Component / Product Card
Placeholder / Product Image
内部检查 / 图片替换清单
内部检查 / 开发实现风险
```

- Rendered website content uses the agreed website language.
- Visible internal rationale, QA, implementation, replacement, and risk labels use Chinese.
- Rxx, theme mappings, and QA labels may exist in layer names or internal pages but never as visible customer-preview content.

## Required behavior

- Use frames and Auto Layout for layout containers.
- Keep reusable master components on `04_本地组件` or the compatible existing page.
- Keep reference captures on `90_参考资料`, never as final page layers.
- Keep customer-preview frames visually clean and export only from those frames.
- Preserve established valid conventions in existing files.

