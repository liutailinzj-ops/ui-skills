# Responsive Geometry Audit

Run this deterministic read-only audit before reporting QA as passed. Inspect the actual Figma nodes; do not infer geometry from layer names or a reduced screenshot.

## Required inputs

- Desktop and Mobile preview root IDs.
- Responsive Section Contract IDs.
- Canonical customer-visible content ledger and internal marker policy.
- Paired Section instance IDs.
- Alignment-group definitions and expected container modes.
- Explicit overflow contracts.

## Checks

### Paired section identity

For every responsive Section pair:

- Resolve both instance IDs.
- Confirm the stable Section ID, source Rxx when applicable, order, component family, content-slot names, shared text/media bindings, and controls match.
- Resolve every visible text/media/control node to its stable content-slot ID and canonical client value. A missing slot, value difference, extra visible node, or breakpoint difference fails unless the exact field is an approved `content_variant` in the Responsive Section Contract.
- Confirm every layout, crop, repetition, visibility, or interaction difference appears in `allowed_differences` with theme evidence or the custom responsive plan.

### Alignment groups

- Resolve the major nodes assigned to each `alignment_group_id` at one breakpoint.
- Compute left and right edges relative to the preview root.
- Fail when edges in one group differ by more than 1 px.
- Fail an unexplained container change. `full_width`, `standard`, `narrow`, or project-specific modes require foundation or theme evidence.
- Report the node IDs, expected edge, actual edge, and delta.

### Containment and clipping

- Traverse each preview root from the smallest known subtree.
- For every normal child, compare `x`, `y`, `x + width`, and `y + height` with its parent bounds.
- If the child exceeds the parent and the parent clips content, fail unless the exact parent/child is covered by an explicit overflow contract.
- If the parent does not clip, still report the overflow unless it is an intentional named overlay or visible-overflow composition.
- Never treat a hidden or clipped node as proof that the layout is correct.

### Sizing and grid remainder

- Check HUG/FILL/FIXED values on layout containers and wrapping text.
- Fail fixed-height wrappers that crop content or leave source-unjustified dead space.
- Fail manually fixed child widths that cause an unexplained row remainder or inconsistent right edge.
- Check same-row equal-height requirements and 1 px grid-span tolerance.

### Customer-preview isolation

- Compare visible values with the canonical customer-visible ledger and inspect visible annotations/layer context. Fail undeclared visible content and explicit internal markers such as `Placeholder`, `TBD`, `TODO`, `待替换`, `未批准`, `待确认`, `概念预览`, `内部检查`, `QA`, `Rxx`, `Theme Native`, `Section Custom`, `source warning`, or `replacement instruction` when they are not intentional canonical storefront copy.
- Do not fail legitimate storefront words through broad single-word searches such as `test`, `source`, `scope`, or `approval`; use ledger correspondence and phrase/context evidence.
- Treat any internal note in either preview state as blocking.

## Output

Return a Chinese finding for every failure with:

```text
问题类型 | 断点 | Section/节点 | 预期 | 实际 | 差值或溢出 | 是否可安全自动修复
```

Do not report `通过` when any paired identity, content-slot parity, alignment, containment, clipping, or preview-isolation check fails.
