# BizMetria Decision Log

This log records approved global decisions. Master Control is the only workstream authorized to mark global decisions as approved.

## DEC-001 — Brand name

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** The product and company brand is `BizMetria`.
- **Primary domain:** `BizMetria.ai`
- **Affected workstreams:** All

## DEC-002 — Market scope

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** BizMetria is marketed broadly to businesses across industries rather than being limited to one vertical.
- **Implementation note:** The product remains modular internally through business classification, industry modules, and process modules.
- **Affected workstreams:** Product, Voice, Analysis, Website, Marketing, QA

## DEC-003 — Launch languages

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** English and Spanish are supported at launch.
- **Affected workstreams:** All customer-facing and data-producing workstreams

## DEC-004 — Separate language phone numbers

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** English and Spanish AI voice interviews use separate phone numbers.
- **Reason:** Reduce language confusion and simplify prompts, voices, QA, routing, and analytics.
- **Affected workstreams:** Voice, Backend, Website, CRM, Legal, QA

## DEC-005 — Paid product price

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** The BizMetria Business Assessment has one public price of `$299` as a one-time payment.
- **Affected workstreams:** Product, Website, Payments, Marketing, Legal

## DEC-006 — Free-check funnel

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** The primary cold-traffic funnel begins with a free AI Opportunity Check before offering the $299 paid assessment.
- **Constraint:** The free result provides limited diagnostic information and primarily sells the complete assessment.
- **Affected workstreams:** Free Audit, Website, Product, CRM, Marketing, Analytics

## DEC-007 — Free-check structure

- **Status:** Approved baseline
- **Date:** 2026-07-30
- **Decision:** The free check contains 11 primary questions plus a contact form.
- **Affected workstreams:** Free Audit, Website, Backend, CRM, Legal, QA

## DEC-008 — AI Opportunity Score

- **Status:** Approved baseline; subject to validation testing
- **Date:** 2026-07-30
- **Decision:** The free check calculates a 0–100 AI Opportunity Score with five blocks:
  - Lead Response and Follow-Up: 30
  - Manual Work: 25
  - Systems and Data: 20
  - Strategic Priority: 15
  - Opportunity Breadth: 10
- **Constraint:** The score is not a financial or business-quality rating.
- **Affected workstreams:** Free Audit, Website, Backend, Marketing, QA

## DEC-009 — Paid assessment deliverables

- **Status:** Approved baseline
- **Date:** 2026-07-30
- **Decision:** The $299 assessment includes an expanded questionnaire, adaptive voice interview up to approximately 45 minutes, personalized analysis, approximately 8–15 supported recommendations, Impact vs. Effort matrix, 30–90 day roadmap, professional PDF report, and results consultation.
- **Affected workstreams:** Product, Voice, Analysis, Report, Website, Legal, QA

## DEC-010 — Implementation sold separately

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** Building and implementing recommended systems is not included in the $299 assessment and is priced separately.
- **Affected workstreams:** Product, Sales, Website, Legal

## DEC-011 — Stripe promotion codes

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** Discounts are implemented through Stripe coupons and promotion codes rather than a custom pricing engine.
- **Affected workstreams:** Payments, Backend, Website, CRM, Analytics

## DEC-012 — Discount range

- **Status:** Approved framework
- **Date:** 2026-07-30
- **Decision:** Lifecycle promotions may use discounts from `$49` through `$199` off the $299 price.
- **Constraint:** The $199 discount is reserved for late-stage reactivation and is not advertised in advance.
- **Affected workstreams:** Product, Payments, CRM, Marketing, Analytics

## DEC-013 — Human review during MVP

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** Every paid report is reviewed by a human before customer delivery during the MVP and pilot stages.
- **Affected workstreams:** Analysis, Report, Backend, Operations, QA

## DEC-014 — Multi-chat operating model

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** The project is divided into 13 dedicated workstream chats coordinated by Master Control and shared GitHub specifications.
- **Affected workstreams:** All

## DEC-015 — GitHub-native collaboration and handoffs

- **Status:** Approved
- **Date:** 2026-07-30
- **Decision:** GitHub is the shared collaboration layer between all BizMetria chats. Specialist chats must store substantive deliverables in versioned repository files, submit them through draft pull requests, and keep review corrections on the same PR. Master Control reviews and merges work directly from GitHub, updates governance files, and assigns downstream tasks. The user should not manually copy full deliverables, Handoff Summaries, or review comments between chats.
- **Implementation note:** `BIZMETRIA_PROJECT_STATUS.md` and `BIZMETRIA_TASK_QUEUE.md` are authoritative governance files maintained by Master Control.
- **Affected workstreams:** All

## Pending decisions

The following are not yet approved and must not be assumed:

- Final technology stack
- Voice AI vendor
- Telephony vendor and exact phone numbers
- CRM and email automation vendor
- Database and hosting stack
- Final refund policy
- Report turnaround commitment
- Exact consultation delivery process
- Final promotion timing and code names
- Final implementation-service pricing
