---
name: iwish-figma-qa
description: Validate and safely repair IWISH editable Figma website designs for file structure, variables/styles, components, Auto Layout, Desktop/Mobile completeness, placeholders, visual defects, and Shopify/WordPress implementation risks. Use after page generation or UI revision and before client review or developer handoff.
---

# IWISH Figma QA

Inspect both node structure and rendered screenshots. Load the available Figma use Skill before Figma calls.

## Inputs

- Project manifest.
- Requested Desktop and Mobile root node IDs.
- Page blueprint and component map.
- Theme Capability Map and approved route budget for theme-based work.
- Theme/platform implementation notes.

## QA Sequence

1. Inspect file/page/frame metadata and compare it with the manifest.
2. For theme-based work, validate every section against the Theme Capability Map and calculate custom-section count and estimated-height ratios before visual polish.
3. Run the structural checklist in [references/qa-checklist.md](references/qa-checklist.md).
4. Capture each major section at a useful scale; do not rely only on a reduced full-page screenshot.
5. Compare screenshots with the page blueprint, actual theme reference, and available visual references.
6. Repair deterministic, low-risk problems such as naming, accidental groups, missing layout sizing, visible internal annotations, obvious clipping, and safe variable/style bindings.
7. Re-run metadata and screenshot checks for every repaired section.
8. Report creative, factual, theme, or implementation decisions that require UI or engineering judgment using [references/report-template.md](references/report-template.md).

## Safety

- Never delete or replace user-owned nodes by broad name-prefix matching.
- Use manifest IDs or exact validated identities.
- Do not silently change brand direction, page strategy, customer facts, or approved content.
- Do not detach components to make a structural check pass.
- Keep Figma mutations sequential.
- Stop on an unclear tool error, inspect state, then retry a corrected operation.

## Completion Criteria

- Requested Desktop and Mobile pages exist and are visually inspectable.
- No unexplained missing sections.
- No obvious cropped text, overlap, blank required imagery, or placeholder leakage.
- Client-preview text-style binding is 100%.
- Same-row comparison and decision cards are equal height unless the blueprint documents intentional asymmetry.
- Content edges and spans match the applied grid within 1 px.
- Mobile content is not accidentally clipped; carousels have an evidenced interaction and visible affordance.
- Theme mappings and custom budgets pass the requested build route.
- Client-preview frames contain no visible implementation labels, source warnings, or replacement instructions.
- Repeated content follows the component map or has an explicit exception.
- Remaining risks have an owner: UI, client, or engineering.
- The report is concise enough for UI to act on directly.

Mark the result `blocked` when any measurable criterion above fails. Use `pass_with_followups` only for non-blocking content replacement or creative review.
