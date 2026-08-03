---
name: iwish-figma-page-builder
description: Build or update native editable Figma Desktop and Mobile website pages from an IWISH page blueprint, project foundations, and component map. Use for Shopify/WordPress template, theme-customized, or fully custom DTC/B2B pages, including placeholder-first projects with incomplete copy or imagery.
---

# IWISH Figma Page Builder

Write the requested composed page into Figma. Load the available Figma use and screen-generation Skills before calling Figma tools.

## Inputs

- Project manifest.
- Approved page blueprint.
- Foundation IDs.
- Component map.
- Customer assets and placeholder policy.
- Theme/current-site reference when applicable.

## Build Rules

Read [references/build-contract.md](references/build-contract.md) and [references/asset-policy.md](references/asset-policy.md).

1. Create the Desktop and Mobile wrapper frames first.
2. Build one major section per sequential Figma mutation.
3. Append sections directly to the target wrapper; do not build orphaned top-level sections for later reparenting.
4. Use component instances for resolved components and project-local components for repeated unsupported patterns.
5. Bind colors, spacing, radii, text, and effects to existing project variables/styles where appropriate.
6. Keep Desktop and Mobile separately editable. Use shared component APIs where useful; do not force identical composition.
7. Set real or placeholder content through component properties rather than detaching instances.
8. Return every created or mutated node ID and update the project manifest after each section.
9. Validate each section screenshot before continuing.

## Reference Capture

For a renderable theme demo/current page, a web-to-Figma capture may be used as temporary visual truth. Keep it on `90_References`, transfer only permitted imagery, rebuild the final design with native nodes and component instances, and never treat the capture as the final page.

## Completion

Return:

- Figma file and page/frame URLs.
- Desktop and Mobile root node IDs.
- Completed section IDs.
- Placeholder inventory.
- Theme/platform implementation labels.
- Section validation results.

