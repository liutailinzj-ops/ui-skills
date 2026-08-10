---
name: iwish-figma-foundation
description: Inspect, create, or reconcile the project-level Figma file structure, variables, styles, grids, and foundation documentation for IWISH website UI work. Use before creating components or pages in a blank, starter-based, or existing Shopify/WordPress design file. A prebuilt Starter File or company component library is not required.
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
- Set appropriate variable scopes and code syntax.
- Create text/effect styles required by the current project.
- Do not build a large speculative company library.
- Do not add Dark Mode unless the project requires it.
- Return and record every created or mutated node, page, variable, collection, and style ID.
- Validate foundations with metadata and screenshots before component creation.
- Create or reuse an internal visual-direction page when representative compositions will be written.
- Do not create a customer-visible QA page. Internal QA defaults to the Codex conversation or internal artifact; create an internal Figma QA page only when requested and use Chinese visible labels.
- When the customer will receive the whole Figma file, keep internal QA in a separate file.

## Output

Update the project manifest with:

- Page IDs.
- Collection and variable IDs.
- Text/effect style IDs.
- Grid and frame defaults.
- Existing-library findings.
- Conflicts and resolutions.
- Foundation screenshots and validation status.
- Visual-direction page ID and internal-QA location when applicable.
