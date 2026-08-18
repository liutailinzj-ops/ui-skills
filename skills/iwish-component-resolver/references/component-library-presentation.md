# Component Library Presentation Contract

## Responsive family geometry

- One Section family occupies one horizontal family row.
- Variant order is always `Viewport=Desktop | Viewport=Mobile`, left to right.
- Align both variant origins to the top edge even when their heights differ.
- Use the foundation variant gap and stable column starts; do not use per-family ad hoc spacing.
- Component-set and family-row bounds must Hug Content tightly enough that no unexplained empty band remains.
- Vertical breakpoint stacking, overlapping component sets, or loose absolute placement blocks page assembly. Repair the library before using its instances.

The component page is an internal working surface, but it must be orderly enough for UI to find, compare, and edit component families without rearranging the file.

## Required structure

Use one root Auto Layout frame on the local-component page:

```text
组件库 / {Project}
  00_基础组件
  10_导航与全局
  20_商业与转化
  30_内容与媒体
  40_产品与比较
  50_表单与交互
  90_项目专用 Section
```

Create only categories consumed by the current project. Each category is a vertical Auto Layout frame. Each component family occupies one row with:

- Chinese family title and short editability note outside the component set;
- master component or component set aligned to the same row origin;
- Desktop and Mobile Section variants top-aligned when both are required;
- states/variants ordered left to right by one declared axis order;
- consistent gap and row padding from foundation spacing tokens;
- enough row height for the largest variant plus padding; no manual overlap or loose canvas placement.

## Alignment and sizing

- Bind the library root, category frames, and rows to Auto Layout.
- Use one library content width or a named wide mode. All category and row left/right edges must align within 1 px.
- Keep captions, masters, and variant sets on shared column starts. Do not center one family and left-align another without a documented reason.
- For full-width Section masters, keep real component size and place each family on its own row. Do not scale masters into illegible thumbnails or overlap rows to save canvas space.
- Keep actual component-set bounds tight to their children. Remove accidental empty bands caused by stale fixed heights.
- Use one spacing token between variants and one larger token between families. Do not position components with arbitrary canvas coordinates.
- Keep deprecated or superseded components in a separate archive area, never mixed with active families.

## Editability and naming

- Use stable names and variant property order across families.
- Keep component properties visible and meaningful; do not expose arbitrary visual constants as variants.
- Keep customer copy out of master defaults when a neutral editable value is sufficient, but do not use internal approval or placeholder instructions as visible component text.
- Do not detach instances on the library page.
- Record the library root, category, row, component-set, and paired breakpoint node IDs in the manifest.

## Presentation gate

Before page assembly, capture the active component library at readable scale and fail when:

- category or family rows are not aligned;
- component sets overlap, float freely, or use inconsistent origins;
- paired Desktop/Mobile variants are visually unrelated or not top-aligned;
- component-set bounds contain unexplained large empty areas;
- captions, variant order, or component names are inconsistent;
- UI must rearrange the library before normal editing.

This gate evaluates library usability, not customer-facing art direction. Keep the page outside customer preview and use Chinese for its visible internal labels.
