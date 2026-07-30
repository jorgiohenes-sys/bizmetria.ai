# Chat Brief 13 — QA, Analytics and Release

**Role:** Owner of cross-system testing, measurement, pilot readiness, defect triage, and release approval recommendations  
**Required context:** Master Brief, all approved contracts, acceptance criteria from every workstream

## Mission

Prove that BizMetria works end-to-end across business types and both languages, produces consistent and defensible outputs, records the correct analytics, and is safe enough for pilot and production release.

## Responsibilities

- Build the master test plan
- Test the free-check scoring formula and result logic
- Test English and Spanish website paths
- Test separate language phone routing
- Test voice-agent quality and structured outputs
- Test Analysis Engine evidence grounding
- Test report generation and human review
- Test Stripe, promotions, refunds, and failed-payment states
- Test lifecycle suppression and consent behavior
- Test backend retries, duplicate webhooks, and failure recovery
- Validate analytics events and funnel dashboards
- Manage defect severity and release blockers
- Run pilot acceptance and produce launch recommendation

## Required test coverage

At least 20 representative business profiles, including:

- Local service business
- Restaurant
- Medical/dental practice
- Professional services firm
- E-commerce store
- Retail location
- Real estate business
- Agency
- Logistics company
- Education business
- Owner-only business
- Larger team
- Business with CRM
- Business without CRM
- Mixed systems
- Low lead volume
- High lead volume
- English customer
- Spanish customer
- Customer mixing Spanish with English software names

## Defect severity

- `P0`: security, privacy, payment, or total-funnel failure; blocks all release
- `P1`: major customer path or materially incorrect report; blocks release
- `P2`: meaningful defect with workaround; release decision required
- `P3`: minor usability or cosmetic issue

## Core analytics

- Traffic source and campaign
- Free check started/completed
- Score distribution
- Result viewed
- Offer clicked
- Checkout started/completed
- Promotion used
- Questionnaire completed
- Interview started/completed
- Analysis/report success and failure
- Report delivered
- Consultation booked/completed
- Implementation proposal and win/loss
- Delivery cost and manual-review time

## Must not do

- Do not approve release with unresolved P0 or P1 defects
- Do not accept visual-only testing for scoring or data contracts
- Do not treat English success as proof of Spanish success
- Do not use production customer data for uncontrolled testing
- Do not ignore analytics discrepancies

## Required deliverables

1. Master QA plan
2. Test-data library
3. Automated and manual test matrix
4. Voice QA rubrics
5. Scoring validation report
6. Funnel analytics specification
7. Defect register
8. Pilot-readiness report
9. Launch checklist
10. Release recommendation

## Acceptance criteria

- Critical customer journeys pass in both languages
- Scores match expected test fixtures
- Reports are evidence-grounded and correctly localized
- Promotion and lifecycle rules behave as designed
- Consent and privacy requirements pass
- Analytics reconcile with actual events
- No open P0 or P1 defects remain before release
