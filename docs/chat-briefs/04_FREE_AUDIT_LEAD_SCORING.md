# Chat Brief 04 — Free Audit and Lead Scoring

**Role:** Owner of the free questionnaire, AI Opportunity Score, result logic, and lead segmentation  
**Required context:** Master Brief, Product Blueprint, Website UX requirements, Legal consent requirements

## Mission

Create a short, consistent, cross-industry free diagnostic that collects useful signals, produces a transparent 0–100 score, reveals only limited information, and qualifies prospects for the $299 assessment.

## Responsibilities

- Maintain the 11-question free-check specification
- Define stable question and answer IDs
- Define English and Spanish labels for the same canonical answers
- Maintain the complete score formula
- Select the top three opportunity categories
- Define result-page text rules
- Define confidence and lead-quality flags
- Define CRM segmentation outputs
- Produce test cases and edge-case handling
- Prevent misleading or random scoring

## Approved score blocks

- Lead Response and Follow-Up: 30
- Manual Work: 25
- Systems and Data: 20
- Strategic Priority: 15
- Opportunity Breadth: 10

## Required output schema

At minimum:

```json
{
  "assessment_version": "1.0",
  "language": "en|es",
  "answers": {},
  "score_total": 0,
  "score_blocks": {},
  "opportunity_level": "",
  "top_opportunity_categories": [],
  "confidence": "high|medium|low",
  "lead_segment": "",
  "primary_observation_key": ""
}
```

## Must not do

- Do not modify the public price
- Do not provide full recommendations or tool names in free results
- Do not infer exact financial losses
- Do not let contact information affect the score
- Do not use random values or industry-based score inflation
- Do not create language-specific scoring differences

## Required deliverables

1. Question schema
2. Answer taxonomy
3. Scoring specification
4. Top-opportunity selection algorithm
5. Result-copy rules
6. Confidence and segmentation rules
7. At least 30 test profiles across industries
8. Edge-case and missing-answer rules
9. Handoff contracts for Website, Backend, CRM, and QA

## Acceptance criteria

- Identical canonical answers produce identical scores in English and Spanish
- The formula can be implemented without interpretation
- Result text never overstates certainty
- Free results are personalized enough to engage but do not replace paid analysis
- Test cases cover low, medium, high, and contradictory profiles
