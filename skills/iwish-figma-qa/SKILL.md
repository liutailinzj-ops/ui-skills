---
name: iwish-figma-qa
description: Run silent internal quality checks and safe deterministic repairs for IWISH Figma delivery across component-library arrangement, Section visual quality, complete-page composition, product-specific content, asset consistency, paired breakpoints, geometry, source/theme fidelity, and client-preview separation. Use after page generation or revision; report internal QA in Chinese outside customer-preview frames.
---

# IWISH Figma QA

Inspect rendered screenshots and node structure as an internal safeguard. Load the available Figma use Skill before Figma calls.

## Inputs

- Production project manifest and delivery-visibility policy.
- Desktop and Mobile customer-preview root node IDs.
- Responsive Section Contracts, paired Section instance IDs, alignment groups, shared content bindings, and overflow contracts.
- Page blueprint, active Visual Direction Contract, applicable page override, representative compositions, and component map.
- Selected visual signature with evidence records and selected/rejected candidate rationale.
- Canonical customer-visible content ledger and internal marker policy.
- Product and Competitor Analysis.
- Theme Capability Map and implementation notes when applicable.
- Source specification, topology contract, composition groups, theme assembly, and adaptation decisions when applicable.
- Product coverage and template strategy for PDP work.
- Visual-Asset Coverage Matrix and project-authored brand record.
- Four-way asset-input route and temporary product consistency anchor when applicable.
- Content Strategy Contract, Section Content Cards, and content sufficiency result.
- Page-composition board node ID and passed macro-composition record.
- Component-library root/category/family-row node IDs and presentation contract.

## Internal QA Sequence

1. Verify that requested customer-preview frames exist and contain only rendered website content.
2. Inspect the component-library page at readable scale. Check aligned root/category/family rows, common origins, captions, variant order, paired breakpoint top alignment, tight component-set bounds, spacing, overlap, and archive separation. A usable page preview cannot compensate for a disordered component library.
3. Compare major-section screenshots with the Visual Direction Contract, selected seven-dimension visual signature, signature evidence, project-authored brand record, Visual-Asset Coverage Matrix, and representative compositions. Check typography hierarchy, color behavior, first-screen topology, imagery, media ratios, product/scene differentiation, density, page rhythm, component grammar, interaction, and responsive transformation.
4. Compare the completed page with the page-composition board. Check shared grid, alignment groups, Section order, macro color/media distribution, density curve, primary conversion focus, complete-page rhythm, and selected-module placement. Isolated good Sections cannot compensate for a weak complete page.
5. Check the Content Strategy Contract against visible copy and media. Verify unique visitor questions, product-specific angles, message hierarchy, competitor presentation logic, conversion/buying coverage, and absence of internal production status. Return `需要调整` when three or more Sections remain generic or repetitive even if the layout is correct.
6. Detect generic visual fallback: repeated black boxes, repeated equal-card grammar, repeated abstract product primitives, duplicated media for semantically different items, default accent color, or a house long-page rhythm unsupported by project evidence. If decision-critical media is missing/repeated or three or more identity-bearing dimensions form an unsupported fixed combination, return `需要调整` to `$iwish-visual-direction`; do not auto-redesign it in QA and do not report the page as complete.
7. Verify selected-module source identity, content/layout correspondence, connected compositions, and target-theme evidence for selected competitor-module work.
8. Verify theme route, Section/Block/Setting support, responsive behavior, and approved customization scope for theme-based work.
9. Verify product/competitor analysis traceability for research-led or hybrid sections.
10. Read [references/responsive-geometry-audit.md](references/responsive-geometry-audit.md) and run its node-level paired identity, canonical content-slot parity, alignment, containment, clipping, sizing, and preview-isolation checks.
11. Run [references/qa-checklist.md](references/qa-checklist.md) for Figma structure, typography, components, assets, source/theme fidelity, and implementation risks.
12. Capture each major section at useful scale. Do not rely only on a reduced full-page thumbnail.
13. Repair deterministic low-risk problems such as removing accidental internal annotations, obvious clipping, safe layout sizing, naming, or variable/style bindings. Do not invent replacement storefront copy, auto-rewrite one breakpoint's content, or change the visual direction.
14. Re-run the geometry audit and screenshots for repaired sections.
15. Return the concise internal report from [references/report-template.md](references/report-template.md).

For a targeted revision, inspect the changed nodes, their responsive pairs, shared instances, and immediate alignment/containment boundaries. Run full-page QA only when a project master rule, global foundation, shared component, page order, or cross-page dependency changed.

## Language and Visibility

- Use the agreed website language inside rendered website frames.
- Use Chinese for every visible internal QA heading, status, finding, implementation note, replacement list, and risk label.
- Keep internal enum values in the manifest only. Display `通过`, `需要调整`, or `阻塞` to UI.
- Default to returning QA in the Codex conversation or an internal artifact without creating Figma nodes.
- If an internal Figma QA page is explicitly required, use `内部检查 / QA` and keep it outside customer-preview pages.
- If the customer receives the whole Figma file, write QA to a separate internal file.
- Never place QA status, Rxx labels, theme mappings, source warnings, or replacement instructions inside customer-preview frames.
- Validate visible values against the canonical customer-visible ledger and their semantic purpose, not broad keyword guesses. Draft-process phrases such as placeholder, pending approval, review concept, confirmation/validation requirements, and replacement instructions remain blocking even when they were mistakenly copied into the ledger, unless the scoped product UI explicitly requires that status as real user-facing functionality.

## Safety

- Never delete or replace user-owned nodes by broad name matching.
- Use manifest IDs or exact validated identities.
- Do not silently change brand direction, page strategy, customer facts, or approved content.
- Do not auto-apply subjective visual recommendations, style candidates, new palettes, new fonts, or composition alternatives during QA. Report a concise adjustment brief with exact scope and reason; mutate only after the production route accepts the decision.
- Do not detach components to make a check pass.
- Keep Figma mutations sequential.
- Stop on an unclear tool error, inspect state, then retry a corrected operation.
- Do not run repository regression fixtures or technical visual gates in this production QA Skill.

## Completion Criteria

- The full page visibly inherits the Visual Direction Contract rather than a generic house template.
- The component library is aligned, organized, non-overlapping, and directly usable by UI.
- The completed page matches the passed page-composition board at macro level; good isolated Sections do not hide weak page rhythm or alignment.
- The visible content passes the Content Strategy Contract and is sufficiently product-specific, non-repetitive, and externally readable.
- Requested Desktop and Mobile previews are complete, visually inspectable, and paired to the same responsive Section/component families.
- Shared Section identity, order, content bindings, controls, and copy match across breakpoints; every difference is evidenced and allowed.
- Every visible text/media/control node resolves to the canonical customer-visible content ledger; internal status, provenance, approval, replacement, and publication fields remain outside rendered content.
- Alignment groups, containment, clipping, and fixed-size checks pass from actual node geometry.
- No unexplained missing sections, required blank imagery, cropped text, overlaps, containment errors, or accidental overflow remain.
- Customer-preview text, components, variables, grids, cards, and responsive behaviors pass the relevant structural checks.
- Theme mappings and custom scope match the requested route.
- Source/reference responsibilities and topology are preserved or truthfully documented at the requested fidelity.
- Temporary material remains presentable, replaceable, and correctly tracked.
- Every decision-critical media role is present at client-review fidelity and matches the Visual-Asset Coverage Matrix; different products, configurations, features, and scenes are visually distinguishable where required.
- Customer-preview frames contain no visible internal QA, implementation, source, Rxx, or replacement content.
- Remaining decisions have a clear UI, client, or engineering owner.

Report internal fields separately, but summarize them in Chinese. Use `通过` only when no production-impacting issue remains, `需要调整` for non-blocking internal follow-ups, and `阻塞` for a real source, route, design, Figma, or implementation failure.
