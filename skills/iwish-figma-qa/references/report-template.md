# QA Report Template

```markdown
## Result

- Figma file:
- Desktop frame:
- Mobile frame:
- Status: pass | pass_with_followups | blocked
- Text-style binding:
- Grid integrity:
- Equal-height groups:
- Mobile overflow:
- Custom section count ratio:
- Custom section height ratio:
- Reference mode:
- Reference responsibility coverage:
- Source sections mapped:
- Source order match:
- Visible content-item coverage:
- Desktop layout-class coverage:
- Mobile layout-class coverage:
- Unresolved mappings:
- Approved deviations:
- Baseline structure signature:
- Result structure signature:
- No-op guard: pass | blocked_no_op | not_applicable
- PDP template strategy: single_template_validated | template_family | coverage_partial
- PDP states tested:

## Theme Mapping

- {page section}: {exact theme section/block, evidence, implementation level}

## Reference Fidelity

- {source section}: {preserved/adapted/omitted, target section, order/layout divergence and reason}
- {stable source ID}: {exact_native/composed_native/unresolved, exact theme Section/Blocks/settings, content bindings, Desktop/Mobile layout-class result, approved deviation}

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
