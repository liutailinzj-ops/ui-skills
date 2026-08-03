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
- Theme/platform implementation notes.

## QA Sequence

1. Inspect file/page/frame metadata and compare it with the manifest.
2. Run the structural checklist in [references/qa-checklist.md](references/qa-checklist.md).
3. Capture each major section at a useful scale; do not rely only on a reduced full-page screenshot.
4. Compare screenshots with the page blueprint and available visual references.
5. Repair deterministic, low-risk problems such as naming, accidental groups, missing layout sizing, placeholder labels, obvious clipping, and safe variable bindings.
6. Re-run metadata and screenshot checks for every repaired section.
7. Report creative, factual, theme, or implementation decisions that require UI or engineering judgment using [references/report-template.md](references/report-template.md).

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
- Repeated content follows the component map or has an explicit exception.
- Remaining risks have an owner: UI, client, or engineering.
- The report is concise enough for UI to act on directly.

