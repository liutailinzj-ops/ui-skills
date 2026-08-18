# Page Composition Gate

The board is a judgeable miniature of the intended page, not a density diagram. Every Section miniature must show its media role or temporary thumbnail, text hierarchy, controls, surface behavior, container/alignment mode, and approximate final proportion. When final media is missing, use a generated/licensed temporary image or a faithful media-role block that names subject, crop, scale, and scene; anonymous monochrome rectangles cannot carry the board.

A board made primarily of color bands, density blocks, generic cards, or empty image boxes is `needs_revision` even when its Section order is correct. UI must be able to compare the board with the eventual full-page screenshot without redesigning the first screen, major media distribution, or page rhythm.

Validate the complete page as one visual system before building final wrappers. Representative Sections prove local quality; this gate proves page-level composition.

## Composition board

Create one internal `整页构图 / {Page}` board after representative Sections and before full-page assembly. Use the selected typography, real headline lengths, color roles, intended media, actual Section order, and approximate final proportions. This is a compact page composition, not a grayscale wireframe and not a second customer page.

Record:

```yaml
page_composition_gate:
  board_node_id:
  section_order: []
  container_modes: []
  alignment_groups: []
  color_distribution:
  media_distribution:
  density_curve:
  primary_conversion_focus:
  source_module_positions: []
  responsive_risk_sections: []
  default_risk_audit:
  screenshot_status: pending | pass | needs_revision
```

## Review dimensions

Check the board without reading the written rationale:

- one stable page grid and named container modes;
- a clear first-screen or primary-conversion focus;
- intentional progression of dense and spacious Sections;
- controlled distribution of light, dark, brand, and accent surfaces;
- decision-critical media appears where the visitor needs it, not merely where the layout has space;
- image scale and crop vary by communication job without becoming visually inconsistent;
- repeated card, split, full-bleed, numbered, and FAQ patterns do not create a mechanical long-page rhythm;
- selected competitor modules retain their connected relationships and do not break the rest of the page rhythm;
- fully custom work has one recognizable creative thesis beyond correct spacing and clean components;
- the page remains identifiable as this project when internal labels are hidden.

## Anti-default audit

For light or missing brand assets, candidate directions must differ in at least four of the seven visual-signature dimensions. If the selected direction combines three or more familiar safe defaults—such as a neutral background, charcoal text, muted green/terracotta accents, Manrope or another common geometric sans, left-copy/right-image Hero, low-radius cards, and alternating light/dark chapters—require direct project evidence for each repeated field or create a third materially different candidate.

Do not use recent project output as a style reference. Do not solve the audit by randomizing colors; change the underlying creative thesis, topology, rhythm, typography, imagery, or interaction when evidence supports it.

## Exit gate

Do not create final Desktop/Mobile page wrappers until:

- the composition-board screenshot is visually aligned and complete;
- all Section edges resolve to foundation alignment groups;
- the macro color/media/density rhythm is intentional;
- representative Sections fit the same page language;
- content volume is realistic enough to test hierarchy;
- UI would not need to reorder most Sections or redesign the first screen after seeing the complete page.

Return to page strategy for content gaps, visual direction for art-direction or rhythm gaps, and foundation for grid/alignment gaps.
