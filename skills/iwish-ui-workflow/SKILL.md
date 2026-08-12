---
name: iwish-ui-workflow
description: "Orchestrate IWISH website UI production for Shopify or WordPress DTC/B2B projects from a concise Chinese launch package through business routing, product and competitor analysis, page strategy, visual direction, editable Figma production, and silent internal QA. Use for exactly three production scenarios: research-led partial theme customization with light brand inputs, selected competitor-module translation into partial theme customization, and fully custom design. This is the UI production workflow, not the Skill regression or technical visual-evaluation workflow."
---

# IWISH UI Workflow

Run one UI-facing production workflow. Keep internal routing, evidence checks, and deterministic QA automatic unless a hard blocker or material design fork requires input.

## Required Inputs

Read [references/input-contract.md](references/input-contract.md), [references/business-routing.md](references/business-routing.md), and [references/interaction-policy.md](references/interaction-policy.md). Accept files, links, folders, or concise Chinese text. Never require UI to remember internal English enum values.

## Production Workflow

1. Normalize customer facts and internal scope into [references/project-manifest.md](references/project-manifest.md).
2. Infer one of the three production scenarios, then derive site model, build route, strategy source, reference role, theme state, content state, requested page, and website language. Display one compact Chinese project-recognition card and continue when the route is clear.
3. Ask at most one grouped round of up to three questions only when an unresolved choice materially changes the design, implementation route, or Figma target.
4. Load `$iwish-page-strategy`. Complete product, category, competitor, DTC conversion-chain or B2B buying-path analysis before selecting page structure. For selected competitor-module work, keep selected-module sources separate from theme-capability and competitor-evidence sources, then produce the selected-module specification, Theme Capability Map, and complete page blueprint.
5. Load `$iwish-visual-direction`. Translate the approved strategy into a project-specific Visual Direction Contract, representative responsive section families, and only the breakpoint proof states needed to verify their behavior. Do not create independent Desktop/Mobile art directions or continue from a generic wireframe, repeated black boxes, or an undocumented house style.
6. Load `$iwish-figma-foundation` only as needed to inspect, create, or reconcile the minimum project variables, styles, grids, pages, and local-component area. A Starter File is optional.
7. Load `$iwish-component-resolver` to resolve only the components required by the page blueprint and Visual Direction Contract. Theme-based components must represent evidenced native sections, blocks, settings, and responsive behavior.
8. Load `$iwish-figma-page-builder` to extend the representative visual language into one complete editable responsive page system with Desktop and Mobile preview states. Build one Section family at a time and preserve shared content, component identity, brand, source, theme, and evidenced breakpoint behavior.
9. Load `$iwish-figma-qa` as a silent internal safeguard. Inspect screenshots and structure, repair deterministic low-risk problems, and return a concise Chinese internal report. Do not create a visible QA panel in customer-preview frames.
10. Return the Figma links, recognition card, short analysis, visual-direction summary, page/frame names, placeholder list, theme implementation notes, internal risks, and the concise UI adjustment list.

## Route Behavior

- For research-led partial theme customization, derive structure from the product, market, competitors, and conversion or buying path, then classify every Section by its actual theme/native/custom implementation route.
- For selected competitor-module partial theme customization, preserve only the explicitly selected modules' content responsibility, layout relationship, connected composition, and responsive behavior; design the rest from research.
- For fully custom work, use customer requirements, research, references, available brand inputs, and platform feasibility without imposing theme-module constraints.

## Production Boundaries

- Do not run regression cases, baseline signatures, no-op checks, fixture assertions, or technical visual gates in this production Skill. Those belong under `evals/`.
- Do not inherit a fixture brand, product vocabulary, section count, color palette, component family, or visual rhythm.
- Theme-based work records the actual implementation class per Section without a universal percentage cap.
- Do not begin full-page Figma production without a Visual Direction Contract, representative responsive Section families, and breakpoint proof for responsive-risk modules.
- Do not treat Desktop and Mobile previews as separate design briefs. They are rendered states of the same content, Section order, component families, and responsive contract.
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
- Complete editable Desktop and Mobile customer-preview frames exist as paired breakpoint previews of one responsive page system.
- Paired Section instances share identity, content bindings, and order; every breakpoint difference is theme-evidenced or recorded in the custom responsive plan.
- Theme-based sections stay within the approved route and evidence; custom work is identified internally.
- Missing content uses presentable temporary assets or treatments without visible internal instructions.
- Client-preview frames contain only website design content and no visible QA, Rxx, mapping, implementation, or replacement labels.
- Internal QA has checked rendered screenshots and Figma structure and returned Chinese results outside the client preview.
- The handoff tells UI what remains adjustable without asking UI to reconstruct the page design.
