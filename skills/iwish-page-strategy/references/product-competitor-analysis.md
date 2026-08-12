# Product and Competitor Analysis

Produce this artifact for every project before theme selection, page hierarchy, or reference conversion. Missing final copy or images does not block analysis; mark facts, inferences, and placeholders separately.

## Evidence rules

- Start with customer facts, product records, catalogs, current site, supplied competitors, and supplied references.
- Supplement with a compact set of current first-party category and competitor sources when browsing is available.
- Attach evidence URLs and access dates to external observations.
- Never promote inferred benefits, reviews, certifications, results, ingredients, specifications, prices, or guarantees to customer facts.
- Record `fact`, `inference`, `unknown`, and `placeholder` status for decision-critical items.

## Product model

Record what is needed to design the requested page:

```yaml
product_model:
  category:
  product_families: []
  representative_products: []
  customer_need_states: []
  use_contexts: []
  purchase_decision_factors: []
  differentiators: []
  proof_available: []
  objections_or_risks: []
  variants_or_selection_complexity: []
  repeat_purchase_or_retention: []
  evidence_gaps: []
```

Do not require a customer-designated priority product. Select representative and edge states from available evidence and keep the Figma content replaceable.

## Competitor matrix

Use supplied competitors first and supplement only as needed. For each relevant source record:

- Positioning and intended audience.
- Product/category organization and discovery path.
- Page content sequence and the question each section answers.
- Value, benefit, use-context, proof, comparison, objection, offer, and CTA logic.
- Desktop/Mobile differences and interaction patterns.
- Strong category convention, distinctive competitor choice, weakness, and opportunity.
- Relevance to this customer's product and build route.

Do not score visual attractiveness alone. Analyze why information appears in that order and how it moves the visitor toward the next decision.

## DTC conversion chain

Model the relevant chain rather than forcing a fixed page template:

```text
Entry intent
-> Product/category comprehension
-> Personal relevance and desired outcome
-> Differentiation and use context
-> Trust and proof
-> Evaluation, selection, or comparison
-> Objection and risk reduction
-> Purchase action
-> Post-purchase confidence, repeat purchase, or retention when relevant
```

For each applicable stage record:

```yaml
- stage:
  visitor_question:
  available_answer:
  evidence_status: fact | inference | unknown | placeholder
  competitor_patterns: []
  page_responsibility:
  content_or_asset_needed:
  proposed_placement:
```

The chain may span Homepage, Collection, PDP, About, educational, campaign, and post-purchase surfaces. Do not force every responsibility onto one page.

## B2B buying path

For B2B, model the applicable path: business fit, product/category scope, applications, technical suitability, capabilities, operational proof, certification/documentation, cases, service process, and contact/RFQ/sample/distributor action. Extend it with industry-specific pages and evidence; do not invent proof.

## Strategy-mode application

- `research_led`: use the analysis to generate the hierarchy and theme-selection criteria.
- `hybrid_led`: use specified modules where approved and fill uncovered responsibilities from analysis.
- `custom_led`: turn requirements, research, references, and available brand inputs into an original page hierarchy without theme-module constraints.

## Required output

Return:

- Product model.
- Competitor matrix.
- DTC conversion chain or B2B buying path.
- Category conventions versus opportunities.
- Content priority and page implications.
- Evidence gaps and placeholder plan.
- Theme-selection or theme-audit criteria when applicable.

Do not continue to page hierarchy when the product/category cannot be identified or when analysis sources are insufficient to support the proposed strategy. Selected competitor modules do not replace product, category, competitor, and journey analysis for the rest of the page.
