# QA Report Template

```markdown
## Result

- Figma file:
- Desktop frame:
- Mobile frame:
- Status: pass | pass_with_followups | blocked
- Build Truth URL:
- Structure source URL:
- Theme capability URLs:
- Competitor evidence URLs:
- Visual inspiration URLs:
- Source identity status: pass | blocked_source_identity
- Product/category identity:
- Source fingerprint match:
- Theme-demo promotion check:
- Text-style binding:
- Grid integrity:
- Equal-height groups:
- Mobile overflow:
- Multi-line text sizing:
- Unexpected overlaps:
- Parent-child containment:
- Overflow contracts:
- Oversized blank bands:
- Media/gallery balance:
- Sticky/anchor navigation match:
- Custom section count ratio:
- Custom section height ratio:
- Reference mode:
- Reference responsibility coverage:
- Source sections mapped:
- Source order match:
- Visible content-item coverage:
- Composition-group coverage:
- Desktop topology coverage:
- Mobile topology coverage:
- Unresolved mappings:
- Approved deviations:
- Approval provenance:
- Exact theme setting evidence:
- Baseline structure signature:
- Result structure signature:
- Baseline topology signature:
- Result topology signature:
- No-op guard: pass | blocked_no_op | not_applicable
- Analysis status:
- Strategy mode:
- Product model coverage:
- Competitors analyzed:
- Conversion/buying responsibilities covered:
- Evidence gaps:
- PDP template strategy: single_template_validated | template_family | coverage_partial
- PDP states tested:

## Theme Mapping

- {source URL + stable source section}: {exact target theme section/block/settings, theme capability evidence URL, implementation level}

## Product and Competitor Analysis

- {visitor question or journey responsibility}: {section, evidence status, source or placeholder}
- {competitor/category observation}: {page implication}

## Reference Fidelity

- {source section}: {preserved/adapted/omitted, target section, order/layout divergence and reason}
- {stable source ID}: {composition group, exact_native/validated composed_native/unresolved, exact theme Section/Blocks/settings and evidence, content bindings, Desktop/Mobile topology result, approved deviation provenance}

## PDP Coverage

- {product archetype/state}: {pass/fail/not tested, affected modules}

## Repaired

- {node/section}: {repair}

## UI Review

- {creative or brand decision}

## Client Content Needed

- {placeholder}: {required replacement}

## Engineering Check

- {section}: {theme/platform risk and required decision}

## Remaining Blockers

- {blocker and owner}
```

Keep empty sections out of the final report.
