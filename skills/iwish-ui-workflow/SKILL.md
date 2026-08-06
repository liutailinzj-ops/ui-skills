---
name: iwish-ui-workflow
description: Orchestrate IWISH website UI production from a Chinese natural-language launch package through automatic business routing, mandatory product/competitor analysis, theme selection or audit, editable Figma generation, and QA. Use for Shopify or WordPress template, theme-customized, or fully custom DTC/B2B projects, including specified-reference, hybrid-reference, current-site revision, and placeholder-first work.
---

# IWISH UI Workflow

Run one user-facing workflow while applying the specialized Skills in sequence. Keep intermediate checks internal unless a hard blocker or genuine design fork requires input.

## Required Inputs

Read [references/input-contract.md](references/input-contract.md). Accept files, links, folders, or concise Chinese text. Do not require UI to remember internal English enum values. Apply [references/business-routing.md](references/business-routing.md) and [references/interaction-policy.md](references/interaction-policy.md).

## Readiness Rules

Treat only these as hard blockers:

- The brand or project cannot be identified.
- The product/service category is unknown.
- The target market or customer type is unknown.
- The internal project scope does not identify which page to generate.
- No editable Figma target is available and creating one is not authorized.
- The route is template or theme customization, theme selection is not in scope, and no current theme/demo/current-site reference can be inspected.

Missing product selections, final copy, product images, brand guidelines, or a Starter File are not blockers. Apply [references/placeholder-policy.md](references/placeholder-policy.md).

## Workflow

1. Normalize customer facts and internal scope into the manifest defined in [references/project-manifest.md](references/project-manifest.md).
2. Infer `site_model`, `build_route`, `strategy_mode`, `theme_state`, `content_state`, and each reference's role. Display the short Chinese Project Recognition Card defined in [references/business-routing.md](references/business-routing.md). Continue automatically when the route is clear.
3. Apply exception-driven interaction. Ask at most one grouped round of up to three questions only when an unresolved choice would materially change design strategy, implementation scope, or the Figma target.
4. Load and apply `$iwish-page-strategy`. Before page structure or theme selection, produce the mandatory Product and Competitor Analysis, including the DTC conversion chain or B2B buying path. Use it differently according to `research_led`, `reference_led`, `hybrid_led`, or `existing_site_led`.
5. Classify every supplied reference URL as `reference_to_theme`, `structure_target`, `visual_inspiration`, or `competitor_evidence`. Use `reference_to_theme` when the approved page must retain the reference page's visible content inventory, section order, and Desktop/Mobile layout anatomy. Do not silently downgrade it.
6. When `theme_state` is `to_be_selected`, research and select the best-supported theme candidate before the Theme Capability Map. When a theme is already specified, audit it. For `reference_to_theme`, produce the Source Page Specification and Theme Assembly Plan; otherwise produce the applicable reference matrix and project-specific page blueprint.
7. Enforce the build-route gate before Figma work. For template work, block unapproved custom Liquid, section-custom, and custom sections. For theme customization, block when section-custom and custom work exceeds 20% of section count or estimated page height without approval.
8. For PDP work, approve one of `single_template_validated`, `template_family`, or `coverage_partial`. Never call a layout universal because it fits one sampled product.
9. Load and apply `$iwish-figma-foundation` to inspect or create the target file structure, variables, styles, grids, and project status. A Starter File is optional.
10. Load and apply `$iwish-component-resolver` to reuse, extend, wrap, or create only the components needed by the page blueprint, product-content states, conversion responsibilities, and Theme Capability Map.
11. Load and apply `$iwish-figma-page-builder` to create native editable Desktop and Mobile client-preview pages section by section and validate the approved product scenarios and conversion responsibilities.
12. Load and apply `$iwish-figma-qa` to inspect metadata and screenshots, safely repair deterministic problems, and block measurable analysis, theme, reference-fidelity, product-coverage, structure, or client-preview failures.
13. Return the Figma link, recognition card, short analysis summary, created page/frame names, placeholder list, theme mapping, reference-fidelity result, PDP coverage result, custom-budget result, implementation risks, and the short UI review checklist.

## Execution Contract

- Continue automatically between capabilities.
- Keep Figma mutations sequential and retain every returned node ID in the project manifest.
- Resume from recorded node IDs and completed capabilities instead of rebuilding successful work.
- Use Chinese labels in user-facing messages; keep English enum values internal to the manifest.
- Do not pause merely to confirm a high-confidence route. Ask only when two materially different directions remain valid or a hard blocker exists.
- Limit interactive clarification to one grouped round with no more than three decision-changing questions. Do not turn the workflow into a questionnaire.
- Never present temporary claims, certifications, prices, reviews, specifications, or competitor assets as customer-approved facts.
- Never treat `section_custom` or `custom` as the automatic fallback for a creative idea on a theme-based project.
- Do not treat a reference URL as visual mood only when the client asked to reproduce its content structure through the selected theme.
- In `reference_to_theme`, treat the captured source page specification as build truth. Do not add, omit, reorder, rewrite, or redesign visible source content unless the manifest contains explicit approval.
- In `reference_to_theme`, stop before Figma when any source section lacks an evidenced theme mapping. Return the exact gap and the choices: accept a named deviation, change theme, or approve theme customization.
- In `reference_to_theme`, do not run open-ended page strategy or propose an alternative creative direction. Translate the approved source page.
- Do not infer a catalog-wide PDP from one product page. Validate the base template against representative or edge-case product states.
- Do not begin content hierarchy or theme selection until Product and Competitor Analysis is recorded. For DTC, include product comprehension, competitive presentation logic, and the full relevant conversion chain.
- In `reference_led` strict work, use analysis to identify product-fit and conversion risks, but do not change the approved source structure without explicit approval.
- Keep internal theme labels, source warnings, and replacement instructions out of client-preview frames.
- Do not stop after producing a textual Figma specification when Figma write access is available; write the editable design.

## Completion Criteria

Complete only when:

- The requested Desktop and Mobile frames exist in Figma.
- Repeated elements use valid components or documented exceptions.
- Foundations and component bindings are inspectable.
- Placeholder layers are clearly tagged while the rendered client preview remains presentable.
- Theme Capability Map, exact section mappings, and build-route budget pass.
- Product and Competitor Analysis exists, evidence gaps are labeled, and every planned section traces to a relevant DTC conversion responsibility or B2B buying responsibility. Strict reference work may report gaps instead of adding unapproved sections.
- A structure-target reference has a section-by-section content/layout correspondence and every unexplained omission or reorder is reported.
- A `reference_to_theme` run has a verified Source Page Specification and Theme Assembly Plan; source section count, order, content-item coverage, Desktop/Mobile layout-class coverage, and mapping status pass at 100% unless a deviation is explicitly approved.
- A regression with expected structural changes has a changed Figma structure signature. An unchanged target is blocked as a no-op regression.
- PDP work has a Product Coverage Matrix and a truthful coverage status; conditional modules and additional templates are documented where required.
- Client-preview Text nodes use approved Text Styles.
- Grid, equal-height, overflow, and Mobile carousel checks pass.
- Client-preview frames contain no visible implementation or replacement notes.
- Structural and visual QA have run.
- The UI designer receives a concise list of creative decisions still requiring human judgment.
