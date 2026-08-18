# Delivery Structure Gate

Run this deterministic read-only gate against the final Figma node IDs before any delivery can be reported as `通过` or `完成`. Recompute from the live file; never accept a manifest flag, prior `issues=[]`, screenshot alignment, or the producing task's own summary as evidence.

## Required IDs

- every live Figma page ID;
- component-library root;
- active category and family-row roots;
- responsive Section Component Set IDs;
- complete Desktop and Mobile preview roots.

Missing or unresolved IDs are blocking.

## File-page hygiene assertions

1. Enumerate every live `PAGE` node from the file root. Do not trust a planned page list or prior manifest.
2. A page with zero visible top-level nodes is blocking. Optional research, reference, QA, and archive pages must not exist merely as empty placeholders.
3. Flag a page containing only setup placeholders, debug output, obsolete captures, or superseded residue for scoped review. Do not classify intentional final placeholder media inside an active design as page residue.
4. A deterministic cleanup may remove only an exact page ID that was re-read immediately before mutation, has zero visible top-level nodes, and is not the file's sole remaining page. Record every removed page ID.
5. Re-enumerate the file after cleanup. Delivery passes only when `empty_page_ids` is empty and no unresolved placeholder-only page remains.

## Component-library assertions

1. The library root resolves to `FRAME`, not `PAGE`, `SECTION`, or a loose collection of page-level nodes, and `layoutMode` is `VERTICAL`.
2. Every active category and family row is a descendant of that root and uses Auto Layout. Active masters may not sit directly on the page outside the root.
3. Every responsive Section Component Set contains exactly one `Viewport=Desktop` and one `Viewport=Mobile` component. Desktop is left of Mobile and their top edges differ by no more than 1 px.
4. For every child variant, require:
   - `x >= -1` and `y >= -1`;
   - `x + width <= componentSet.width + 1`;
   - `y + height <= componentSet.height + 1`.
   A variant extending outside its Component Set is blocking even when instances render correctly elsewhere.
5. Category and family-row shared left/right origins differ by no more than 1 px. Rows and Component Sets do not overlap.
6. Unexplained fixed empty space is blocking. Component Set, row, and category bounds must be recomputed after variant height changes.

## Complete-preview assertions

1. Both roots resolve to `FRAME` and use `layoutMode=VERTICAL`. `layoutMode=NONE` is blocking even when manually positioned Sections are pixel-aligned.
2. Direct page children are instances of the recorded responsive Section families. No detached or unrelated Section frame may replace one breakpoint state.
3. Every direct child has `x=0`, matches the root width, remains inside the root, and participates in Auto Layout rather than absolute positioning.
4. Desktop and Mobile contain the same stable Section order and canonical content identities. Height differences are allowed; missing, duplicated, or reordered Section identities are not.
5. The final root bound contains the final Section completely. A root or Component Set that clips a valid child is blocking.

## Evidence record

Return a compact machine-readable result before the Chinese summary:

```yaml
delivery_structure_gate:
  total_page_count:
  populated_page_count:
  empty_page_ids: []
  placeholder_only_page_ids: []
  removed_empty_page_ids: []
  library_root_id:
  library_root_type:
  library_layout_mode:
  category_count:
  family_row_count:
  responsive_set_count:
  variant_bound_failures: []
  floating_master_ids: []
  desktop_root_id:
  desktop_layout_mode:
  mobile_root_id:
  mobile_layout_mode:
  section_pair_count:
  preview_structure_failures: []
  issues: []
  status: pass | blocked
```

Set `status: pass` only when the live-node `issues` array is empty. Do not manually waive a failed assertion; repair the structure and rerun the read-only gate.
