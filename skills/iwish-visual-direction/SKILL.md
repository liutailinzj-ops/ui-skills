---
name: iwish-visual-direction
description: Translate an IWISH product/competitor analysis, page blueprint, light or complete brand inputs, references, theme-customization constraints, and Responsive Section Contracts into a project-specific website visual direction and representative editable Figma section families with breakpoint proof states. Use between page strategy and full-page production for Shopify or WordPress partially theme-customized and fully custom DTC/B2B work, especially when customers provide only a Logo or brand color, assets are incomplete, or competitor-section translation could collapse into generic UI.
---

# IWISH Visual Direction

Create the visual design contract that the full Figma page must inherit. Load the available Figma use and screen-generation Skills before writing representative compositions.

## Inputs

- Project manifest and website language.
- Product and Competitor Analysis.
- Page blueprint and conversion or buying responsibilities.
- Customer brand assets and existing VI when available.
- Structure sources, visual references, and current site when applicable.
- Theme Capability Map and Theme Assembly Plan for theme-based work.
- Responsive Section Contracts, alignment groups, shared content bindings, and evidenced breakpoint behavior.
- Content mode and temporary-asset policy.

## Process

1. Read [references/visual-direction-contract.md](references/visual-direction-contract.md).
2. Separate customer facts, source observations, industry conventions, visual inspiration, and creative decisions. Do not turn one regression fixture into a default style.
3. Define one primary art direction: brand character, typography, color behavior, imagery, media crop, density, spacing rhythm, grid behavior, card language, controls, motion or interaction cues, and responsive transformation.
4. For selected competitor-module work, preserve each selected module's visual hierarchy, media/content relationship, connected composition, repeated-item behavior, and reading flow. Express these decisions through evidenced target-theme behavior or a named scoped custom Section.
5. For research-led work, derive composition from product comprehension, category differentiation, proof, evaluation, objection handling, and action without imposing a house sequence or house visual language.
6. For custom work, use references as evidence or inspiration without copying their identity.
7. Read [references/representative-compositions.md](references/representative-compositions.md) and create representative editable Section families on an internal visual-direction page. Build one primary state and only the derived breakpoint proof states needed to validate responsive-risk behavior. Use shared website content across states, the actual website language for rendered content, and Chinese for visible internal annotations.
8. Validate that the representative compositions visibly express the contract. Revise them before full-page production when they remain generic, under-designed, or disconnected from source/theme evidence.

## Non-Negotiable Design Rules

- Do not use repeated black rectangles, empty generic card grids, or neon accent defaults as the dominant visual language unless the project evidence explicitly requires them.
- Do not call a content inventory, Rxx list, theme map, grayscale skeleton, or styled wireframe a visual direction.
- Use customer imagery first. When assets are missing, use licensed, generated, or clearly tracked temporary category imagery with realistic crops and density.
- Missing assets may change content provenance, not composition quality.
- Do not invent claims, specifications, reviews, certifications, prices, or guarantees.
- Do not create independent Desktop and Mobile art directions, rewrite content by viewport, or detach one breakpoint state from the shared Section/component family.
- Use one foundation-defined container and alignment system. A different section width requires a named container mode and theme or design evidence.
- Do not pause for a technical visual gate. That gate belongs to the repository evaluation path, not UI production.
- Keep internal rationale, QA, source labels, and implementation notes outside customer-preview frames.

## Output

Update the manifest with:

- Visual Direction Contract.
- Primary typography, color, imagery, density, grid, spacing, component, and responsive decisions.
- Reference/source principles used and deliberately rejected.
- Theme-native visual constraints and allowed adaptations when applicable.
- Representative Section-family node IDs and paired breakpoint-proof node IDs.
- Shared content bindings, alignment groups, and allowed responsive differences.
- Temporary asset inventory and replacement restrictions.
- Explicit prohibited defaults that would make the project generic.
- `complete` only when the visual contract and representative compositions agree.

Pass this output to `$iwish-component-resolver` and `$iwish-figma-page-builder`. Do not generate the complete page in this Skill.
