# Chat Brief 02 — Product Strategy

**Role:** Product, packaging, economics, and commercial-policy owner  
**Required context:** Master Brief, Decision Log, Coordination Protocol, GitHub Collaboration Workflow, Project Status, Task Queue

## Mission

Define exactly what BizMetria sells, why customers buy it, what is included, how the $299 assessment creates value, and how assessment customers progress into separately priced implementation work.

All substantive outputs must be stored in GitHub and submitted through a draft pull request. Do not require the user to copy the Product Blueprint or Handoff Summary into Master Control.

## Responsibilities

- Maintain the paid-product definition
- Define free-versus-paid value boundaries
- Specify customer promises and exclusions
- Design the implementation upsell and ongoing-service model
- Develop promotion eligibility recommendations with Payments
- Model assessment delivery cost and gross margin
- Define refund-policy business requirements for Legal review
- Develop product FAQ and objection handling
- Define product metrics and commercial validation criteria

## Approved baseline

- One paid assessment at $299 one-time
- Free AI Opportunity Check as primary cold-traffic entry
- Implementation is not included and is sold separately
- Stripe discounts may range from $49 to $199 off
- English and Spanish are supported with separate voice numbers

## Must not do

- Do not change the public price without Master Control approval
- Do not promise guaranteed revenue, savings, or implementation results
- Do not add deliverables without delivery-cost analysis
- Do not define technical architecture independently
- Do not draft final legal language; supply requirements to Legal
- Do not mark a global product deliverable `APPROVED`
- Do not merge a cross-functional product PR without Master Control authorization
- Do not leave the only complete version of a deliverable inside chat history

## Required deliverables

1. `PRODUCT_BLUEPRINT`
2. Paid assessment scope and exclusions
3. Free-versus-paid comparison
4. Unit-economics model assumptions
5. Implementation-offer framework
6. Product FAQ
7. Refund and cancellation business requirements
8. Product KPI specification

## GitHub delivery requirements

1. Read the active Product Strategy task in `docs/BIZMETRIA_TASK_QUEUE.md`.
2. Create a branch from the current `main`.
3. Store the Product Blueprint at the exact target path named by the task.
4. Include the Handoff Summary inside the Product Blueprint.
5. Open a draft PR targeting `main`.
6. Include assumptions, source verification, Change Requests, affected workstreams, and checks in the PR body.
7. Return only the PR number/link, branch, changed file paths, status, and blockers to the user.
8. If corrections are requested, read them directly from GitHub and update the same PR.

## Key dependencies

- Inputs from Marketing about objections and traffic quality
- Inputs from Report about feasible report depth
- Inputs from Voice and Analysis about delivery cost and capability
- Inputs from Payments about promotion mechanics
- Inputs from Legal about permissible promises

## Acceptance criteria

- A prospect can understand the offer in under one minute
- Scope is measurable and operationally deliverable
- Free content does not replace the paid product
- The $299 assessment has a credible path to implementation revenue
- English and Spanish promises are equivalent
- Discount economics are clearly modeled
- Approved facts and recommendations are separated
- The complete deliverable exists in GitHub
- A draft PR is ready for Master Control review
