---
name: iwish-figma-page-builder
description: Build or update one complete native editable responsive Figma website system with paired Desktop and Mobile preview states from an IWISH page blueprint, Visual Direction Contract, responsive Section contracts, representative compositions, project foundations, and component map. Use for Shopify or WordPress template, theme-customized, or fully custom DTC/B2B production after visual direction is established, including projects with incomplete copy or imagery.
---

# IWISH Figma Page Builder

Extend an established project-specific visual direction into the requested complete Figma page. Load the available Figma use and screen-generation Skills before Figma calls.

## Required Inputs

- Production project manifest and website language.
- Approved page blueprint and Product/Competitor Analysis.
- Complete Visual Direction Contract.
- Representative Section-family and breakpoint-proof node IDs.
- Responsive Section Contracts, alignment groups, shared content bindings, and allowed breakpoint differences.
- Foundation IDs and component map.
- Customer assets and temporary-asset policy.
- Theme Capability Map and Theme Assembly Plan for theme-based work.
- Source specification, content-layout matrix, topology contract, composition groups, and source-role table when applicable.
- Product Coverage Matrix and template strategy for PDP work.

If the Visual Direction Contract or representative compositions are missing, generic, or inconsistent, return the missing dependency to `$iwish-visual-direction`. Do not invent a fallback house layout.

## Build Rules

Read [references/build-contract.md](references/build-contract.md) and [references/asset-policy.md](references/asset-policy.md).

1. Inspect the representative Section families and extract their actual typography, colors, imagery, media ratios, density, grid, spacing rhythm, component language, and responsive transformations.
2. Create paired Desktop and Mobile customer-preview wrapper frames with no visible internal annotations. Treat them as breakpoint views of one page system.
3. Build one responsive Section/component family per sequential Figma mutation, then place its paired Desktop and Mobile instances before continuing to the next Section.
4. Reuse resolved component instances and project-local components; keep editorial sections editable without forcing every unique composition into a generic card family.
5. For theme-based work, reproduce evidenced native Section/Block geometry and content slots, then apply the Visual Direction Contract through supported tokens, settings, and styling.
6. For specified-structure work, build from source specifications and visual correspondence rather than topics or memory. Preserve requested content, connected compositions, hierarchy, reading flow, and documented theme adaptation.
7. For research-led work, preserve each section's trace to product, competitor, and journey evidence without adding generic ecommerce filler.
8. Use customer imagery first. When material is missing, use licensed, generated, or tracked temporary imagery that preserves intended crop, density, product scale, and composition.
9. Bind project colors, spacing, radii, text, and effects to variables/styles. Keep client-facing text editable and styled.
10. Keep both preview states editable through the shared component family. Do not detach or rewrite one state independently; change only the breakpoint fields allowed by the Responsive Section Contract.
11. Validate each paired Section at useful screenshot scale before proceeding. Compare content parity, alignment groups, parent containment, clipping, and theme-evidenced breakpoint behavior; repair deterministic layout problems immediately.
12. Keep theme mappings, source warnings, Rxx identifiers, implementation notes, temporary-asset provenance, and QA results outside customer-preview frames.
13. Return every created or mutated node ID and update the production manifest.

## Visual Continuity Rules

- Every section must inherit identifiable decisions from the Visual Direction Contract or record a justified section-specific exception.
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
