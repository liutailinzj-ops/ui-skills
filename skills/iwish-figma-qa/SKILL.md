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
- Product and Competitor Analysis with DTC conversion or B2B buying responsibilities.
- Theme Capability Map and approved route budget for theme-based work.
- Theme/platform implementation notes.
- Source Page Specification, Theme Assembly Plan, approved deviations, and baseline/result structure signatures for `reference_to_theme` work.
- Source-role table and Source Identity Fingerprint for specified-structure work.
- Reference Content-Layout Matrix and fidelity target when applicable.
- Product Coverage Matrix, representative products, and template strategy for PDP work.

## QA Sequence

1. Inspect file/page/frame metadata and compare it with the manifest.
2. For specified-structure work, run source identity before any percentage calculation: compare Build Truth URL, product/category, H1, hero signature, and stable section sequence across the brief, Source Page Specification, Theme Assembly Plan, Figma manifest, and rendered page. Block `blocked_source_identity` when any artifact uses the theme demo or another source instead.
3. For theme-based work, validate every section against the Theme Capability Map and calculate custom-section count and estimated-height ratios before visual polish. Confirm every mapping is cross-source: structure-source section to target-theme capability evidence.
4. Validate that the page blueprint and rendered sections trace to the Product and Competitor Analysis. Check relevant visitor questions, evidence status, and journey responsibilities without imposing a fixed DTC section sequence.
5. Run the structural checklist in [references/qa-checklist.md](references/qa-checklist.md).
6. Capture each major section at a useful scale; do not rely only on a reduced full-page screenshot.
7. For `structure_target`, compare each section with the Reference Content-Layout Matrix. Measure responsibility coverage and report unexplained ordering or layout-anatomy divergence; do not use overall visual similarity as the only test.
8. For `reference_to_theme`, inspect the structure-source capture and target side by side in stable source-section order. Verify exact visible content items and counts, Desktop/Mobile layout classes, target-theme Section/Block/settings, and approved deviations. Semantic responsibility coverage is not a pass metric. Report analysis-identified conversion gaps without auto-repairing the approved structure.
9. Inspect visual geometry at node level and screenshot level: multi-line text sizing, sibling intersections, underfilled fixed-height sections, media crop/aspect and gallery balance, and sticky/anchor navigation labels/order/destinations.
10. For regression work, compare the baseline and result structure signatures. If expected changed sections retain the same order, geometry, child tree, and content digest, return `blocked_no_op` even when a new page or report exists.
11. For PDP work, test the approved representative and edge states. Confirm that the base template or template family handles optional modules, long content, media/variant differences, and Mobile behavior without product-specific hardcoding.
12. Compare screenshots with the page blueprint, actual structure source, target-theme capability evidence, and available visual references.
13. Repair deterministic, low-risk problems such as naming, accidental groups, missing layout sizing, visible internal annotations, obvious clipping, and safe variable/style bindings.
14. Re-run metadata and screenshot checks for every repaired section and PDP state.
15. Report creative, factual, theme, product-coverage, reference-fidelity, or implementation decisions that require UI or engineering judgment using [references/report-template.md](references/report-template.md).

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
- Multi-line Text nodes are Auto Height/HUG or intentionally clamped; no unexplained sibling collision or oversized blank band remains.
- Client-preview text-style binding is 100%.
- Same-row comparison and decision cards are equal height unless the blueprint documents intentional asymmetry.
- Content edges and spans match the applied grid within 1 px.
- Mobile content is not accidentally clipped; carousels have an evidenced interaction and visible affordance.
- Theme mappings and custom budgets pass the requested build route.
- Product and Competitor Analysis is complete, every non-strict-reference section has analysis or requirement traceability, and missing proof remains labeled rather than invented.
- `structure_target` responsibility coverage is complete for relevant source sections; every order or layout divergence is justified.
- `reference_to_theme` Build Truth URL identity, product/category identity, source fingerprint, section count/order, visible content-item coverage, Desktop/Mobile layout-class coverage, and resolved cross-source theme mapping are each 100% except for named approved deviations.
- A regression with expected changes has a changed result structure signature; unchanged results are `blocked_no_op`.
- PDP work truthfully reports `single_template_validated`, `template_family`, or `coverage_partial`, and all claimed product states pass.
- Client-preview frames contain no visible implementation labels, source warnings, or replacement instructions.
- Repeated content follows the component map or has an explicit exception.
- Remaining risks have an owner: UI, client, or engineering.
- The report is concise enough for UI to act on directly.

Mark the result `blocked` when any measurable criterion above fails. Use `pass_with_followups` only for non-blocking content replacement or creative review.
