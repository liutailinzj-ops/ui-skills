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

Missing product selections, final copy, product images, brand guidelines, or a Starter File are not blockers. Apply [references/placeholder-policy.md](references/placeholder-policy.md).

## Workflow

1. Normalize customer facts and internal scope into the manifest defined in [references/project-manifest.md](references/project-manifest.md).
2. Load and apply `$iwish-page-strategy` to research the industry, market, competitors, and relevant patterns. Produce a project-specific page blueprint; do not use a fixed section list.
3. Load and apply `$iwish-figma-foundation` to inspect or create the target file structure, variables, styles, grids, and project status. A Starter File is optional.
4. Load and apply `$iwish-component-resolver` to reuse, extend, wrap, or create only the components needed by the page blueprint.
5. Load and apply `$iwish-figma-page-builder` to create native editable Desktop and Mobile pages section by section.
6. Load and apply `$iwish-figma-qa` to inspect metadata and screenshots, safely repair deterministic problems, and report remaining creative or implementation decisions.
7. Return the Figma link, created page/frame names, placeholder list, implementation-risk list, and the short UI review checklist.

## Execution Contract

- Continue automatically between capabilities.
- Keep Figma mutations sequential and retain every returned node ID in the project manifest.
- Resume from recorded node IDs and completed capabilities instead of rebuilding successful work.
- Ask only when two materially different directions remain valid or a hard blocker exists.
- Never present temporary claims, certifications, prices, reviews, specifications, or competitor assets as customer-approved facts.
- Do not stop after producing a textual Figma specification when Figma write access is available; write the editable design.

## Completion Criteria

Complete only when:

- The requested Desktop and Mobile frames exist in Figma.
- Repeated elements use valid components or documented exceptions.
- Foundations and component bindings are inspectable.
- Placeholder content is clearly tagged.
- Structural and visual QA have run.
- The UI designer receives a concise list of creative decisions still requiring human judgment.

