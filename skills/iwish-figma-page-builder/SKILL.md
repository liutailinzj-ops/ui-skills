---
name: iwish-figma-page-builder
description: Build or update one complete editable responsive IWISH Figma website system from passed content strategy, visual authority, representative Sections, page-composition board, aligned component library, asset route, foundations, and theme/source contracts. Use for Shopify/WordPress partially customized or fully custom DTC/B2B production across complete or missing brand/product assets.
---

# IWISH Figma Page Builder

Extend an established project-specific visual direction into the requested complete Figma page. Load the available Figma use and screen-generation Skills before Figma calls.

## Required Inputs

- Production project manifest and website language.
- Approved page blueprint and Product/Competitor Analysis.
- Active Visual Direction Contract, authority version, and applicable approved page override.
- Selected visual-signature record, signature evidence, selected candidate ID, and selection rationale.
- Representative Section-family and breakpoint-proof node IDs.
- Responsive Section Contracts, alignment groups, shared content bindings, and allowed breakpoint differences.
- Canonical customer-visible content ledger with stable text/media/control slot IDs and internal marker policy.
- Foundation IDs and component map.
- Customer assets and temporary-asset policy.
- Visual-Asset Coverage Matrix with decision-critical media specifications, asset/node IDs, variation requirements, and replacement rules.
- Theme Capability Map and Theme Assembly Plan for theme-based work.
- Source specification, content-layout matrix, topology contract, composition groups, and source-role table when applicable.
- Product Coverage Matrix and template strategy for PDP work.
- Passed Content Strategy Contract and Section Content Cards.
- Passed page-composition board with alignment groups, section order, color/media distribution, density curve, and screenshot status.
- Passed component-library presentation with root/category/family-row node IDs.

If the Visual Direction Contract or representative compositions are missing, generic, or inconsistent, return the missing dependency to `$iwish-visual-direction`. Do not invent a fallback house layout.

For a targeted revision, representative compositions remain valid unless the changed master rule or scoped override invalidates them. Resolve the exact target and dependency set from the manifest rather than requiring a full-page rebuild.

## Build Rules

Read [references/build-contract.md](references/build-contract.md) and [references/asset-policy.md](references/asset-policy.md).

1. Inspect the representative Section families and extract their actual typography, colors, imagery, media ratios, density, grid, spacing rhythm, component language, and responsive transformations. Confirm they correspond to the selected visual signature rather than a rejected candidate or generic fallback.
2. Resolve whether this is complete production or a targeted revision. For a revision, record target IDs, responsive counterparts, shared instances, immediate containment/alignment boundaries, invalidated dependencies, and preserved scope before mutation.
3. Run a content preflight before mutation: resolve every visible text/media/control slot to the canonical customer-visible ledger, reject visible internal markers, confirm one Section order for both breakpoints, and record the exact evidenced content variants.
4. Validate the selected representative set with canonical content, final Text Styles, and the actual temporary media from the Visual-Asset Coverage Matrix. Apply content/styles before measuring; read actual text bounds, reflow parents, and repair navigation, wrapping, media crop, repeated-item, semantic differentiation, and overflow behavior before assembling the full page.
5. Validate the component-library presentation and page-composition board. Do not create full-page wrappers until the first screen, one differentiation module, one imagery-led module, the aligned component library, and the complete-page composition all pass. Return to strategy, visual direction, or foundation when content, macro rhythm, color/media distribution, grid, or alignment remains unresolved.
6. Create paired Desktop and Mobile customer-preview wrapper frames as vertical Auto Layout `FRAME` nodes with no visible internal annotations. Append every Section instance to the wrapper flow; `layoutMode=NONE` or manually maintained Section y positions are invalid. For targeted revision, preserve existing wrappers and unrelated Sections only when this structural contract already passes.
7. Build one responsive Section/component family per sequential Figma mutation, then place or update its paired Desktop and Mobile instances before continuing to the next Section.
8. Complete the entire blueprint inside both wrappers, including required header, commerce, content, global, cross-sell, footer, and sticky responsibilities. Representative families are preflight evidence only; never stop complete production after placing only those families.
9. Reuse resolved component instances and project-local components; keep editorial sections editable without forcing every unique composition into a generic card family.
10. For theme-based work, use evidenced native Section/Block geometry where it preserves the design responsibility. When native geometry materially weakens the approved hierarchy, media relationship, interaction, or responsive behavior and development scope allows it, use styling, CSS, Liquid, or a scoped new Section and record the route. Theme capability is an implementation inventory, not a requirement to imitate the demo or accept a weaker composition.
11. For selected competitor-module work, build the selected modules from source specifications and visual correspondence rather than topics or memory. Preserve requested content, connected compositions, hierarchy, reading flow, and documented theme adaptation; derive the rest of the page from the approved research-led blueprint.
12. For research-led work, preserve each section's trace to product, competitor, and journey evidence without adding generic ecommerce filler.
13. Use customer imagery first. When material is missing, use licensed, generated, or tracked temporary imagery that preserves intended crop, density, product scale, and composition.
14. Bind each decision-critical media node to its Visual-Asset Coverage Matrix row. Semantically different products, configurations, features, or scenes must be visibly different; do not satisfy distinct media slots by duplicating one generic illustration and changing text.
15. For PDP and other transaction pages, render decision-critical commerce states even when factual data is missing. Use neutral presentation-only sample values tracked internally for price hierarchy, discount/compare-at state, rating present/absent, inventory, shipping, variants/options, quantity, purchase actions, and sticky purchase behavior; never present them as verified facts.
   For unsupported specifications, certifications, dimensions, performance, warranty, or proof, do not render rows of em dashes, empty values, `N/A`, or pseudo-table placeholders. Omit and collapse the optional field group, replace it with truthful qualitative decision support, or keep the incomplete structure internal.
16. Bind project colors, spacing, radii, text, and effects to variables/styles. Keep client-facing text editable and styled.
17. Keep both preview states editable through the shared component family. Do not detach or rewrite one state independently; change only the breakpoint fields allowed by the Responsive Section Contract.
18. Validate each paired Section at useful screenshot scale before proceeding. Compare content-slot IDs and values, visual-asset roles, alignment groups, parent containment, clipping, and theme-evidenced breakpoint behavior; repair deterministic layout problems immediately.
19. Keep theme mappings, source warnings, Rxx identifiers, implementation notes, temporary-asset provenance, and QA results outside customer-preview frames. Never render internal content status beside website copy.
20. Capture and inspect full Desktop and Mobile screenshots after the last Section. Set both complete-preview states before requesting final QA; a component-library screenshot, composition board, or representative Section screenshot cannot substitute.
21. Read back both preview roots. Require `type=FRAME`, `layoutMode=VERTICAL`, direct children as recorded Section instances, full-width non-absolute children, and complete final-child containment before requesting QA.
22. Return every created or mutated node ID, explicitly preserved node IDs, and update the production manifest.

## Visual Continuity Rules

- Every section must inherit identifiable decisions from the Visual Direction Contract or record a justified section-specific exception.
- Apply only active project master rules and approved scoped overrides. Never convert a retrieved recommendation or unapproved candidate directly into a project token, component rule, or page-wide style.
- Do not generate repeated black rectangles, generic equal-card rows, default lime accents, or a fixed long-page rhythm unless project evidence explicitly calls for them.
- Do not use the same component grammar for unrelated content responsibilities merely because it is easy to generate.
- Do not call a structurally complete wireframe a client preview.
- Do not let the amount of customer material determine visual fidelity. Generate or license missing decision-critical visuals, track them, and keep them replaceable.
- Preserve the asset-input route: supplied brand/product assets remain authoritative, and missing product media follows one recorded consistency anchor across all generated views.
- Treat the page-composition board as a macro contract. A Section may refine internally, but it may not silently change the shared grid, order, dominant color/media distribution, density curve, or primary conversion focus.
- Do not reuse one product silhouette or abstract illustration across different comparison cards, configurations, features, or contexts when the visual is meant to communicate the difference.
- If the same output could fit an unrelated brand after text substitution, revise the visual composition before continuing.
- If three or more identity-bearing signature dimensions cannot be traced to project evidence, return to `$iwish-visual-direction`; do not let full-page assembly turn an unsupported candidate into the de facto direction.
- Auto Layout, components, Rxx coverage, and style binding are implementation requirements, not substitutes for visual design.

## Client and Internal Separation

- Rendered website content uses the agreed website language.
- Visible internal annotations, when needed outside client frames, use Chinese.
- Do not create a QA panel in a client-preview page or frame.
- Create visible content only from `canonical_client_value`. Keep `evidence_status`, approval, provenance, replacement owner, publication restriction, and internal-marker fields out of rendered nodes.
- Default to reporting internal QA in the Codex conversation or an internal artifact.
- If the customer receives the whole Figma file, place internal QA and implementation documentation in a separate file.

## Completion

For `complete_production`, completion is invalid unless both full-page preview roots exist, contain the complete approved Section sequence, use paired responsive families, and pass screenshot/structure QA. If work intentionally stops at design exploration, return `代表性模块预检通过` and `整体状态：进行中`; do not use `完成` or `通过` for the production result.

Return:

- Figma file and customer-preview frame URLs.
- Desktop and Mobile preview root IDs, completed responsive Section-family IDs, and paired instance IDs.
- Visual Direction Contract correspondence and justified exceptions.
- Content-strategy and page-composition correspondence, including any justified macro deviation.
- Component-library presentation status and root node ID.
- Temporary asset inventory.
- Visual-Asset Coverage Matrix completion and any unresolved media role.
- Theme/platform mapping and implementation risks.
- Product scenario result when applicable.
- Concise internal handoff in Chinese.

Do not return regression-suite, baseline, no-op, or technical visual-gate results from this production Skill.
