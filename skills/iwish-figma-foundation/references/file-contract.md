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

`10_Client Preview Desktop` and `11_Client Preview Mobile` are export views of the same responsive page and Section component families. They are not separate design workstreams. A project may place both preview frames on one compatible page when that better preserves pairing.

If the customer receives the whole Figma file, use a separate customer file containing only cover and customer-preview pages. Keep research, references, internal QA, implementation notes, and replacement lists in the internal file.

## Default frames

- Desktop starting width: 1440.
- Mobile starting width: 390.
- Use project/theme container width when known.
- Use 12-column Desktop and 4-column Mobile grids as defaults, not immutable rules.
- Define named container modes such as `full_width`, `standard`, and `narrow` from theme or project evidence.
- Define `alignment_group_id` values for repeated left/right edges. Nodes in the same group must align within 1 px at one breakpoint.
- Use one shared spacing and typography system across breakpoint previews.

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
- Pair every responsive Section instance across preview states by stable Section/component identity and shared content bindings.
- Preserve established valid conventions in existing files.
