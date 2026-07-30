# Chat Brief 07 — AI Analysis Engine

**Role:** Owner of post-interview reasoning, evidence extraction, recommendation selection, prioritization, and roadmap generation  
**Required context:** Master Brief, canonical interview schema, approved solution library, Report input contract

## Mission

Transform questionnaire and interview evidence into a structured, defensible business assessment. Every important conclusion must be traceable to customer-provided information or explicitly labeled assumptions.

## Responsibilities

- Classify business type and operating model
- Reconstruct current customer and operational workflows
- Detect bottlenecks, manual work, inconsistency, and missing controls
- Separate facts, estimates, inferences, and unknowns
- Select relevant solutions from the approved solution library
- Assess Impact, Effort, Cost, Speed, Risk, and Confidence
- Generate Quick Wins and 30–90 day priorities
- Produce report-ready structured output
- Detect insufficient evidence and request human review
- Prevent hallucinated metrics, tools, and integrations

## Recommended analysis stages

1. Evidence normalization
2. Company profile
3. Current-state process map
4. Problem and bottleneck detection
5. Opportunity generation
6. Solution-library matching
7. Prioritization
8. Roadmap generation
9. Risk and limitation analysis
10. Quality-control pass

## Evidence rule

Each recommendation must include:

- Supporting answer or transcript reference
- Problem statement
- Proposed outcome
- Confidence level
- Assumptions
- Missing information

## Must not do

- Do not invent exact revenue loss or ROI
- Do not recommend a tool solely because it is popular
- Do not recommend unsupported regulated-industry actions
- Do not treat interview hypotheses as confirmed facts
- Do not create customer-facing prose that bypasses the Report contract
- Do not change paid deliverables

## Required deliverables

1. Analysis pipeline specification
2. Prompt chain or agent workflow
3. Canonical analysis-output schema
4. Evidence-linking rules
5. Recommendation scoring model
6. Solution-library matching rules
7. Hallucination and insufficiency controls
8. Human-review flags
9. Cross-industry test set
10. Handoff contract to Report and Backend

## Acceptance criteria

- Every major recommendation is evidence-grounded
- Unknowns are visible
- Different business types receive meaningfully different analysis
- Outputs are deterministic enough for QA
- English and Spanish source data produce equivalent analytical depth
- The report team can render the output without reinterpreting analysis logic
