---
name: iwish-ui-workflow
description: Orchestrate IWISH website UI production for Shopify or WordPress DTC/B2B projects from a concise Chinese launch package through business routing, product and competitor analysis, page strategy, visual direction, editable Figma production, and silent internal QA. Use for template, theme-customized, or fully custom projects with specified references, mixed references, current-site revision, or incomplete content. This is the UI production workflow, not the Skill regression or technical visual-evaluation workflow.
---

# IWISH UI Workflow

Run one UI-facing production workflow. Keep internal routing, evidence checks, and deterministic QA automatic unless a hard blocker or material design fork requires input.

## Required Inputs

Read [references/input-contract.md](references/input-contract.md), [references/business-routing.md](references/business-routing.md), and [references/interaction-policy.md](references/interaction-policy.md). Accept files, links, folders, or concise Chinese text. Never require UI to remember internal English enum values.

## Production Workflow

1. Normalize customer facts and internal scope into [references/project-manifest.md](references/project-manifest.md).
2. Infer site model, build route, strategy source, reference role, fidelity expectation, theme state, content state, requested page, and website language. Display one compact Chinese project-recognition card and continue when the route is clear.
3. Ask at most one grouped round of up to three questions only when an unresolved choice materially changes the design, implementation route, or Figma target.
4. Load `$iwish-page-strategy`. Complete product, category, competitor, DTC conversion-chain or B2B buying-path analysis before selecting page structure. For specified-reference work, separate the structure source from theme-capability and competitor sources, then produce the source specification, theme capability map, and page blueprint appropriate to the requested fidelity.
5. Load `$iwish-visual-direction`. Translate the approved strategy into a project-specific Visual Direction Contract and representative Desktop/Mobile compositions. Do not continue to full-page production from a generic wireframe, repeated black boxes, or an undocumented house style.
6. Load `$iwish-figma-foundation` only as needed to inspect, create, or reconcile the minimum project variables, styles, grids, pages, and local-component area. A Starter File is optional.
7. Load `$iwish-component-resolver` to resolve only the components required by the page blueprint and Visual Direction Contract. Theme-based components must represent evidenced native sections, blocks, settings, and responsive behavior.
8. Load `$iwish-figma-page-builder` to extend the representative visual language into complete editable Desktop and Mobile pages. Build section by section and preserve brand, source, theme, content, and responsive decisions from upstream contracts.
9. Load `$iwish-figma-qa` as a silent internal safeguard. Inspect screenshots and structure, repair deterministic low-risk problems, and return a concise Chinese internal report. Do not create a visible QA panel in customer-preview frames.
10. Return the Figma links, recognition card, short analysis, visual-direction summary, page/frame names, placeholder list, theme implementation notes, internal risks, and the concise UI adjustment list.

## Route Behavior

- For research-led work, derive structure from the product, market, competitors, and conversion or buying path.
- For specified-structure theme work, preserve the source content, order, connected compositions, and reading flow while translating them into evidenced target-theme behavior at the requested fidelity.
- For hybrid work, preserve explicitly selected reference modules and design the remaining responsibilities from research.
- For current-site revision, identify what to retain, revise, relocate, or replace.
- For custom work, use customer requirements, research, references, VI, and platform feasibility without imposing theme-module constraints.

## Production Boundaries

- Do not run regression cases, baseline signatures, no-op checks, fixture assertions, or technical visual gates in this production Skill. Those belong under `evals/`.
- Do not inherit a fixture brand, product vocabulary, section count, color palette, component family, or visual rhythm.
- Do not begin full-page Figma production without a Visual Direction Contract and representative Desktop/Mobile compositions.
- Do not treat Auto Layout, Rxx coverage, component counts, or Text Style binding as proof of design quality.
- Do not expose internal enum values to UI. Use Chinese labels in recognition cards, questions, summaries, and internal QA.
- Use the agreed website language for rendered website content. For an English storefront, visible page navigation, commerce labels, headings, body copy, and CTAs remain English.
- Use Chinese for visible internal Figma annotations, QA panels, implementation notes, replacement lists, and risk labels.
- Keep Rxx identifiers, theme mappings, QA results, source warnings, replacement instructions, and approval provenance outside customer-preview frames.
- Default to returning QA in the Codex conversation or internal artifact. If Figma QA panels are explicitly required, place them on `内部检查 / QA`; if the whole Figma file will be shared with a customer, use a separate internal file.
- Never show `Approved` unless the manifest records the exact decision, approver, source, and date.
- Never present temporary claims, certifications, prices, reviews, specifications, competitor assets, or generated content as customer-approved facts.
- Missing final content or a Starter File is not a blocker. Apply [references/placeholder-policy.md](references/placeholder-policy.md).
- Do not stop after a textual specification when authorized Figma write access exists.

## Completion Criteria

Complete only when:

- Product and competitor analysis, page blueprint, and the project-specific Visual Direction Contract exist.
- Representative visual compositions are not generic wireframes and are traceable to brand, research, source, or theme evidence.
- Complete editable Desktop and Mobile customer-preview frames exist.
- Theme-based sections stay within the approved route and evidence; custom work is identified internally.
- Missing content uses presentable temporary assets or treatments without visible internal instructions.
- Client-preview frames contain only website design content and no visible QA, Rxx, mapping, implementation, or replacement labels.
- Internal QA has checked rendered screenshots and Figma structure and returned Chinese results outside the client preview.
- The handoff tells UI what remains adjustable without asking UI to reconstruct the page design.
