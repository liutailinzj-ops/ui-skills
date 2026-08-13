---
name: iwish-figma-page-builder
description: Build or update one complete native editable responsive Figma website system with paired Desktop and Mobile preview states from an IWISH page blueprint, Visual Direction Contract, responsive Section contracts, representative compositions, project foundations, and component map. Use for Shopify or WordPress partially theme-customized or fully custom DTC/B2B production after visual direction is established, including projects with only a Logo or brand color and incomplete copy or imagery.
---

# IWISH Figma Page Builder

Extend an established project-specific visual direction into the requested complete Figma page. Load the available Figma use and screen-generation Skills before Figma calls.

## Required Inputs

- Production project manifest and website language.
- Approved page blueprint and Product/Competitor Analysis.
- Active Visual Direction Contract, authority version, and applicable approved page override.
- Representative Section-family and breakpoint-proof node IDs.
- Responsive Section Contracts, alignment groups, shared content bindings, and allowed breakpoint differences.
- Foundation IDs and component map.
- Customer assets and temporary-asset policy.
- Theme Capability Map and Theme Assembly Plan for theme-based work.
- Source specification, content-layout matrix, topology contract, composition groups, and source-role table when applicable.
- Product Coverage Matrix and template strategy for PDP work.

If the Visual Direction Contract or representative compositions are missing, generic, or inconsistent, return the missing dependency to `$iwish-visual-direction`. Do not invent a fallback house layout.

For a targeted revision, representative compositions remain valid unless the changed master rule or scoped override invalidates them. Resolve the exact target and dependency set from the manifest rather than requiring a full-page rebuild.

## Build Rules

Read [references/build-contract.md](references/build-contract.md) and [references/asset-policy.md](references/asset-policy.md).

1. Inspect the representative Section families and extract their actual typography, colors, imagery, media ratios, density, grid, spacing rhythm, component language, and responsive transformations.
2. Resolve whether this is complete production or a targeted revision. For a revision, record target IDs, responsive counterparts, shared instances, immediate containment/alignment boundaries, invalidated dependencies, and preserved scope before mutation.
3. Create paired Desktop and Mobile customer-preview wrapper frames with no visible internal annotations for complete production. For targeted revision, preserve existing wrappers and unrelated Sections.
4. Build one responsive Section/component family per sequential Figma mutation, then place or update its paired Desktop and Mobile instances before continuing to the next Section.
5. Reuse resolved component instances and project-local components; keep editorial sections editable without forcing every unique composition into a generic card family.
6. For theme-based work, reproduce evidenced native Section/Block geometry and content slots, then apply the Visual Direction Contract through supported tokens, settings, and styling.
7. For selected competitor-module work, build the selected modules from source specifications and visual correspondence rather than topics or memory. Preserve requested content, connected compositions, hierarchy, reading flow, and documented theme adaptation; derive the rest of the page from the approved research-led blueprint.
8. For research-led work, preserve each section's trace to product, competitor, and journey evidence without adding generic ecommerce filler.
9. Use customer imagery first. When material is missing, use licensed, generated, or tracked temporary imagery that preserves intended crop, density, product scale, and composition.
10. Bind project colors, spacing, radii, text, and effects to variables/styles. Keep client-facing text editable and styled.
11. Keep both preview states editable through the shared component family. Do not detach or rewrite one state independently; change only the breakpoint fields allowed by the Responsive Section Contract.
12. Validate each paired Section at useful screenshot scale before proceeding. Compare content parity, alignment groups, parent containment, clipping, and theme-evidenced breakpoint behavior; repair deterministic layout problems immediately.
13. Keep theme mappings, source warnings, Rxx identifiers, implementation notes, temporary-asset provenance, and QA results outside customer-preview frames.
14. Return every created or mutated node ID, explicitly preserved node IDs, and update the production manifest.

## Visual Continuity Rules

- Every section must inherit identifiable decisions from the Visual Direction Contract or record a justified section-specific exception.
- Apply only active project master rules and approved scoped overrides. Never convert a retrieved recommendation or unapproved candidate directly into a project token, component rule, or page-wide style.
- Do not generate repeated black rectangles, generic equal-card rows, default lime accents, or a fixed long-page rhythm unless project evidence explicitly calls for them.
- Do not use the same component grammar for unrelated content responsibilities merely because it is easy to generate.
- Do not call a structurally complete wireframe a client preview.
- If the same output could fit an unrelated brand after text substitution, revise the visual composition before continuing.
- Auto Layout, components, Rxx coverage, and style binding are implementation requirements, not substitutes for visual design.

## Client and Internal Separation

- Rendered website content uses the agreed website language.
- Visible internal annotations, when needed outside client frames, use Chinese.
- Do not create a QA panel in a client-preview page or frame.
- Default to reporting internal QA in the Codex conversation or an internal artifact.
- If the customer receives the whole Figma file, place internal QA and implementation documentation in a separate file.

## Completion

Return:

- Figma file and customer-preview frame URLs.
- Desktop and Mobile preview root IDs, completed responsive Section-family IDs, and paired instance IDs.
- Visual Direction Contract correspondence and justified exceptions.
- Temporary asset inventory.
- Theme/platform mapping and implementation risks.
- Product scenario result when applicable.
- Concise internal handoff in Chinese.

Do not return regression-suite, baseline, no-op, or technical visual-gate results from this production Skill.
