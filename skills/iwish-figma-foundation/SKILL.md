---
name: iwish-figma-foundation
description: Inspect, create, or reconcile IWISH Figma file structure, variables, styles, responsive grids, alignment groups, page foundations, and the aligned local-component library layout. Use before creating components or pages in blank, starter-based, or existing Shopify/WordPress files. A Starter File or company library is not required.
---

# IWISH Figma Foundation

Prepare the target Figma file for editable website design. Load the available Figma use and design-system/library Skills before any Figma mutation, and follow their Plugin API safety rules.

## Discovery First

Inspect the target file before writing:

- Existing pages, variables, styles, components, libraries, and naming conventions.
- Whether the file is blank, starter-based, or an active design.
- The product font family and available Figma fonts.
- Existing design-system assets that can be reused.

Never assume an empty local variable list means no library variables exist; search accessible libraries as well.

## Route

- **Blank file:** create the minimum project foundation in [references/file-contract.md](references/file-contract.md).
- **Starter file:** preserve and reuse valid foundations; fill only gaps.
- **Existing project:** match established conventions and document conflicts before changing them.

## Foundation Rules

- Create variables before components.
- Use primitive values and semantic aliases as defined in [references/token-model.md](references/token-model.md).
- Create or reconcile variables and styles from the active project master rules plus the applicable approved page override. Candidate recommendations and unapproved alternatives do not qualify as foundation inputs.
- Set appropriate variable scopes and code syntax.
- Create text/effect styles required by the current project.
- Do not build a large speculative company library.
- Do not add Dark Mode unless the project requires it.
- Return and record every created or mutated node, page, variable, collection, and style ID.
- Validate foundations with metadata and screenshots before component creation.
- Create or reuse an internal visual-direction page when representative compositions will be written.
- Define viewport preview widths, page gutters, maximum container widths, named container modes, spacing scale, and alignment-group rules before Section production.
- Define the local-component library content width, category/family row grid, caption column, variant gap, family gap, and shared row origin before component production. The component page must be an aligned internal system, not a loose canvas.
- Create the component-library root as one `FRAME` with vertical Auto Layout before creating any master. A page, section, or visually aligned set of page-level nodes is not a valid library root.
- Return the actual root node ID and verify from live metadata that `type=FRAME` and `layoutMode=VERTICAL`; do not record a planned or inferred structure as completed.
- Treat Desktop and Mobile pages or frames as paired breakpoint previews of one responsive system. Do not create separate foundations, tokens, content systems, or component libraries for them.
- During a targeted revision, mutate only foundations explicitly invalidated by the authority revision. A page-scoped override should normally use scoped variables/styles or component properties without rewriting unrelated project tokens.
- Do not create a customer-visible QA page. Internal QA defaults to the Codex conversation or internal artifact; create an internal Figma QA page only when requested and use Chinese visible labels.
- When the customer will receive the whole Figma file, keep internal QA in a separate file.

## Output

Update the project manifest with:

- Page IDs.
- Collection and variable IDs.
- Text/effect style IDs.
- Grid and frame defaults.
- Responsive preview widths, container modes, alignment groups, and paired-preview conventions.
- Component-library root layout, category/family row grid, spacing, and alignment conventions.
- Existing-library findings.
- Conflicts and resolutions.
- Foundation screenshots and validation status.
- Visual-direction page ID and internal-QA location when applicable.
