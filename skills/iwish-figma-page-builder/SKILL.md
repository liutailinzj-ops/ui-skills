---
name: iwish-figma-page-builder
description: Build or update native editable Figma Desktop and Mobile website pages from an IWISH page blueprint, project foundations, and component map. Use for Shopify/WordPress template, theme-customized, or fully custom DTC/B2B pages, including placeholder-first projects with incomplete copy or imagery.
---

# IWISH Figma Page Builder

Write the requested composed page into Figma. Load the available Figma use and screen-generation Skills before calling Figma tools.

## Inputs

- Project manifest.
- Approved page blueprint.
- Product and Competitor Analysis with the approved DTC conversion chain or B2B buying path.
- Theme Capability Map and approved route budget for theme-based work.
- Foundation IDs.
- Component map.
- Customer assets and placeholder policy.
- Theme/current-site reference when applicable.
- Source Page Specification, Theme Assembly Plan, and baseline structure signature for `reference_to_theme` work.
- Reference Content-Layout Matrix for `structure_target` work.
- Product Coverage Matrix, representative products, and template strategy for PDP work.

## Build Rules

Read [references/build-contract.md](references/build-contract.md) and [references/asset-policy.md](references/asset-policy.md).

1. Create the Desktop and Mobile wrapper frames first.
2. Build one major section per sequential Figma mutation.
3. Append sections directly to the target wrapper; do not build orphaned top-level sections for later reparenting.
4. For theme-based work, reproduce the approved native section geometry and supported content slots before applying brand styling. Do not invent a layout and label it custom afterward.
5. For `research_led`, `hybrid_led`, and `existing_site_led`, preserve the blueprint's trace from each section to product, competitor, and journey evidence. Do not replace analysis-backed responsibilities with generic ecommerce filler.
6. For `structure_target`, build from the approved source-to-target correspondence. Preserve the relevant content responsibility, sequence, and layout anatomy unless the blueprint records an adaptation. Do not approximate from the reference screenshot after strategy is complete.
7. For `reference_to_theme`, verify that all source mappings are `exact_native` or `composed_native` before any Figma mutation. Build a native-node reference skeleton in stable source-section order, bind the captured visible content item by item, apply the evidenced theme settings and Desktop/Mobile layout classes, then apply permitted brand styling. Do not add standard PDP sections, generated content, or a new hierarchy. Keep analysis-identified conversion gaps in the report unless a structural change is approved.
8. For PDP work, build the primary representative product as the client-preview page, then validate the same component/template structure with the additional approved product states. Keep validation states internal unless multiple client-facing templates are approved. In `reference_to_theme`, these edge-state checks must not change the primary source-page contract.
9. Use component instances for resolved components and project-local components for repeated unsupported patterns.
10. Bind colors, spacing, radii, text, and effects to existing project variables/styles. Bind every client-facing text node to a text style.
11. Keep Desktop and Mobile separately editable. Use shared component APIs where useful; do not force identical composition.
12. Set real or placeholder content through component properties rather than detaching instances.
13. Keep theme mappings, implementation notes, source warnings, product-coverage states, and replacement instructions off the rendered client-preview frame. Store them in the manifest and project/handoff documentation.
14. Return every created or mutated node ID and update the project manifest after each section.
15. Validate each section screenshot and metadata against the build contract before continuing.
16. For regression work, calculate the result structure signature and compare it with the baseline. When expected sections were meant to change but their order, geometry, child tree, and content digest did not change, stop with `blocked_no_op`.

## Reference Capture

For a renderable theme demo/current page, a web-to-Figma capture may be used as temporary visual truth. Keep it on `90_References`, transfer only permitted imagery, rebuild the final design with native nodes and component instances, and never treat the capture as the final page.

For placeholder mode, build a client-presentable composition with safe sample copy and generated or licensed category imagery when available. Use `Placeholder /` in layer names and the manifest, not as the dominant visible design language. Read the asset policy before inserting any non-customer material.

## Completion

Return:

- Figma file and page/frame URLs.
- Desktop and Mobile root node IDs.
- Completed section IDs.
- Placeholder inventory.
- Theme/platform mapping report and custom-budget result.
- Section validation results.
- Reference responsibility/layout coverage for `structure_target` work.
- Source section/order/content/layout-class coverage, approved deviations, and baseline/result structure signatures for `reference_to_theme` work.
- PDP scenario-validation result and truthful template strategy for PDP work.
- Analysis traceability result and any unresolved conversion/buying responsibility.
