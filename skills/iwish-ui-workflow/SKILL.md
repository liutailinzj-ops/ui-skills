---
name: iwish-ui-workflow
description: Orchestrate IWISH website UI production from minimal client facts and internal project scope through industry research, editable Figma foundations, project components, desktop/mobile page generation, and QA. Use when a UI designer asks to create or continue a Shopify or WordPress design for template, theme-customized, or fully custom DTC/B2B work, including projects with missing product copy or images.
---

# IWISH UI Workflow

Run one user-facing workflow while applying the specialized Skills in sequence. Keep intermediate checks internal unless a hard blocker or genuine design fork requires input.

## Required Inputs

Read [references/input-contract.md](references/input-contract.md). Accept files, links, folders, or concise text. Do not require the customer to provide strategy, page structure, priority products, detailed style language, or platform details already known internally.

## Readiness Rules

Treat only these as hard blockers:

- The brand or project cannot be identified.
- The product/service category is unknown.
- The target market or customer type is unknown.
- The internal project scope does not identify which page to generate.
- No editable Figma target is available and creating one is not authorized.
- The route is template or theme customization and no current theme/demo/current-site reference can be inspected.

Missing product selections, final copy, product images, brand guidelines, or a Starter File are not blockers. Apply [references/placeholder-policy.md](references/placeholder-policy.md).

## Workflow

1. Normalize customer facts and internal scope into the manifest defined in [references/project-manifest.md](references/project-manifest.md).
2. Load and apply `$iwish-page-strategy` to audit the current theme first when applicable, then research the industry, market, competitors, and relevant patterns. Produce the Theme Capability Map and a project-specific page blueprint; do not use a fixed section list.
3. Enforce the build-route gate before Figma work. For template work, block unapproved custom Liquid, section-custom, and custom sections. For theme customization, block when section-custom and custom work exceeds 20% of section count or estimated page height without approval.
4. Load and apply `$iwish-figma-foundation` to inspect or create the target file structure, variables, styles, grids, and project status. A Starter File is optional.
5. Load and apply `$iwish-component-resolver` to reuse, extend, wrap, or create only the components needed by the page blueprint and Theme Capability Map.
6. Load and apply `$iwish-figma-page-builder` to create native editable Desktop and Mobile client-preview pages section by section.
7. Load and apply `$iwish-figma-qa` to inspect metadata and screenshots, safely repair deterministic problems, and block measurable theme, structure, or client-preview failures.
8. Return the Figma link, created page/frame names, placeholder list, theme mapping, custom-budget result, implementation-risk list, and the short UI review checklist.

## Execution Contract

- Continue automatically between capabilities.
- Keep Figma mutations sequential and retain every returned node ID in the project manifest.
- Resume from recorded node IDs and completed capabilities instead of rebuilding successful work.
- Ask only when two materially different directions remain valid or a hard blocker exists.
- Never present temporary claims, certifications, prices, reviews, specifications, or competitor assets as customer-approved facts.
- Never treat `section_custom` or `custom` as the automatic fallback for a creative idea on a theme-based project.
- Keep internal theme labels, source warnings, and replacement instructions out of client-preview frames.
- Do not stop after producing a textual Figma specification when Figma write access is available; write the editable design.

## Completion Criteria

Complete only when:

- The requested Desktop and Mobile frames exist in Figma.
- Repeated elements use valid components or documented exceptions.
- Foundations and component bindings are inspectable.
- Placeholder layers are clearly tagged while the rendered client preview remains presentable.
- Theme Capability Map, exact section mappings, and build-route budget pass.
- Client-preview Text nodes use approved Text Styles.
- Grid, equal-height, overflow, and Mobile carousel checks pass.
- Client-preview frames contain no visible implementation or replacement notes.
- Structural and visual QA have run.
- The UI designer receives a concise list of creative decisions still requiring human judgment.
