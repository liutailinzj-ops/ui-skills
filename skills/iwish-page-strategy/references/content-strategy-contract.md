# Content Strategy Contract

Build product-specific page content before visual direction. Safe wording is not sufficient when the page could describe an unrelated product after noun replacement.

## Required analysis

```yaml
content_strategy:
  product_truth:
    confirmed: []
    visually_observable: []
    unknown_or_prohibited: []
  audience_questions: []
  category_decision_factors: []
  competitor_presentation_logic: []
  conversion_or_buying_chain: []
  message_hierarchy:
    primary_promise:
    supporting_messages: []
    proof_needed: []
    objections: []
    actions: []
  section_content_cards:
    - section_id:
      visitor_question:
      content_job:
      product_specific_angle:
      required_information: []
      media_job:
      proof_state: confirmed | observable | temporary | unavailable
      next_action:
  coverage:
    comprehension:
    relevance_or_desire:
    evaluation:
    trust_or_proof:
    objection_reduction:
    action:
```

For B2B, replace desire/consumer trust with application fit, capability, qualification, procurement risk, service, and enquiry responsibility.

## Content rules

- Explain competitor presentation logic: what question a module answers, why its order matters, what media carries, and how the interaction supports evaluation. Do not reduce research to a list of headings.
- Make every Section answer one named visitor question and advance the page journey. Do not add generic ecommerce filler to make a long page.
- Derive wording from confirmed product facts, visually observable form/context, category language, and named project inferences. Keep unverifiable performance, dimensions, materials, certification, price, reviews, warranty, and commercial promises out.
- When facts are missing, use externally readable copy about form, use context, organization, compatibility questions, or intended decision support. Keep `pending`, `placeholder`, `review`, approval, validation, and replacement language in internal metadata only.
- Keep product-specific terms, situations, choices, and objections. If a headline/body pair remains valid for coffee equipment, cat furniture, and a cooker after noun replacement, revise it.
- Avoid repeating the same claim in Hero, benefits, steps, story, CTA, and FAQ. Record the unique content job of each Section.
- Do not force every conversion responsibility onto one page. Record the connected page or unavailable proof when appropriate.

## Content sufficiency gate

Before visual direction, fail or revise when any condition is true:

- Three or more Sections have no unique visitor question or product-specific angle.
- Competitor research records topics but not presentation or conversion logic.
- The primary promise depends on an unconfirmed fact.
- Media jobs are missing for decision-critical Sections.
- The page repeats generic lifestyle language while product comparison, configuration, usage, compatibility, or objection content is absent.
- Client-visible copy contains internal production status or asks the customer to interpret the draft process.

Pass only when the page has enough specific content to judge hierarchy, media, density, and conversion flow before Figma production.
