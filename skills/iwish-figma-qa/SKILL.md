---
name: iwish-figma-qa
description: Run silent internal quality checks and safe deterministic repairs for IWISH editable responsive Figma website designs, covering paired breakpoint identity, content parity, alignment groups, containment/clipping, visual-direction inheritance, source/theme fidelity, client-preview separation, variables/styles, components, assets, and Shopify/WordPress implementation risks. Use after production page generation or UI revision; report visible internal QA in Chinese and never expose QA inside customer-preview frames.
---

# IWISH Figma QA

Inspect rendered screenshots and node structure as an internal safeguard. Load the available Figma use Skill before Figma calls.

## Inputs

- Production project manifest and delivery-visibility policy.
- Desktop and Mobile customer-preview root node IDs.
- Responsive Section Contracts, paired Section instance IDs, alignment groups, shared content bindings, and overflow contracts.
- Page blueprint, Visual Direction Contract, representative compositions, and component map.
- Product and Competitor Analysis.
- Theme Capability Map and implementation notes when applicable.
- Source specification, topology contract, composition groups, theme assembly, and adaptation decisions when applicable.
- Product coverage and template strategy for PDP work.

## Internal QA Sequence

1. Verify that requested customer-preview frames exist and contain only rendered website content.
2. Compare major-section screenshots with the Visual Direction Contract and representative compositions. Check typography hierarchy, color behavior, imagery, media ratios, density, spacing rhythm, component language, and responsive transformation.
3. Detect generic visual fallback: repeated black boxes, repeated equal-card grammar, default accent color, or a house long-page rhythm unsupported by project evidence.
4. Verify source identity, source content/layout correspondence, connected compositions, and target-theme evidence for specified-reference work.
5. Verify theme route, Section/Block/Setting support, responsive behavior, and approved customization scope for theme-based work.
6. Verify product/competitor analysis traceability for research-led or hybrid sections.
7. Read [references/responsive-geometry-audit.md](references/responsive-geometry-audit.md) and run its node-level paired identity, content parity, alignment, containment, clipping, sizing, and preview-isolation checks.
8. Run [references/qa-checklist.md](references/qa-checklist.md) for Figma structure, typography, components, assets, source/theme fidelity, and implementation risks.
9. Capture each major section at useful scale. Do not rely only on a reduced full-page thumbnail.
10. Repair deterministic low-risk problems such as accidental visible annotations, obvious clipping, safe layout sizing, naming, or variable/style bindings. Do not auto-rewrite one breakpoint's content or design.
11. Re-run the geometry audit and screenshots for repaired sections.
12. Return the concise internal report from [references/report-template.md](references/report-template.md).

## Language and Visibility

- Use the agreed website language inside rendered website frames.
- Use Chinese for every visible internal QA heading, status, finding, implementation note, replacement list, and risk label.
- Keep internal enum values in the manifest only. Display `通过`, `需要调整`, or `阻塞` to UI.
- Default to returning QA in the Codex conversation or an internal artifact without creating Figma nodes.
- If an internal Figma QA page is explicitly required, use `内部检查 / QA` and keep it outside customer-preview pages.
- If the customer receives the whole Figma file, write QA to a separate internal file.
- Never place QA status, Rxx labels, theme mappings, source warnings, or replacement instructions inside customer-preview frames.

## Safety

- Never delete or replace user-owned nodes by broad name matching.
- Use manifest IDs or exact validated identities.
- Do not silently change brand direction, page strategy, customer facts, or approved content.
- Do not detach components to make a check pass.
- Keep Figma mutations sequential.
- Stop on an unclear tool error, inspect state, then retry a corrected operation.
- Do not run repository regression fixtures or technical visual gates in this production QA Skill.

## Completion Criteria

- The full page visibly inherits the Visual Direction Contract rather than a generic house template.
- Requested Desktop and Mobile previews are complete, visually inspectable, and paired to the same responsive Section/component families.
- Shared Section identity, order, content bindings, controls, and copy match across breakpoints; every difference is evidenced and allowed.
- Alignment groups, containment, clipping, and fixed-size checks pass from actual node geometry.
- No unexplained missing sections, required blank imagery, cropped text, overlaps, containment errors, or accidental overflow remain.
- Customer-preview text, components, variables, grids, cards, and responsive behaviors pass the relevant structural checks.
- Theme mappings and custom scope match the requested route.
- Source/reference responsibilities and topology are preserved or truthfully documented at the requested fidelity.
- Temporary material remains presentable, replaceable, and correctly tracked.
- Customer-preview frames contain no visible internal QA, implementation, source, Rxx, or replacement content.
- Remaining decisions have a clear UI, client, or engineering owner.

Report internal fields separately, but summarize them in Chinese. Use `通过` only when no production-impacting issue remains, `需要调整` for non-blocking internal follow-ups, and `阻塞` for a real source, route, design, Figma, or implementation failure.
