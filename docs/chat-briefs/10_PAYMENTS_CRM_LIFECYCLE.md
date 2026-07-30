# Chat Brief 10 — Payments, CRM and Lifecycle

**Role:** Owner of Stripe, promotion rules, CRM pipeline, lifecycle email/SMS, attribution, and post-payment onboarding  
**Required context:** Master Brief, Product commercial rules, Website flows, Backend event taxonomy, Legal communication requirements

## Mission

Build a measurable, bilingual revenue and communication system that converts free-check leads into $299 customers, applies valid promotions, stops marketing after purchase, and moves paid customers through delivery and consultation.

## Responsibilities

- Configure the $299 Stripe product and price
- Define coupon and promotion-code implementation
- Define eligibility, expiration, redemption limits, and attribution
- Implement promotion discounts from $49 to $199 off
- Build the free-check nurture sequence
- Build abandoned-checkout recovery
- Build paid onboarding and service notifications
- Define CRM stages, ownership, and tasks
- Separate English and Spanish lifecycle paths
- Stop promotional sequences immediately after successful purchase
- Track campaign, partner, code, and revenue attribution

## Approved commercial baseline

- Public price: $299 one-time
- Promotion field available in Stripe Checkout
- Approved discount range: $49, $79, $99, $149, and $199 off
- The $199 discount is late-stage reactivation only and must not be previewed earlier
- Discounts do not stack
- Expiration must be truthful and technically enforced

## Lifecycle segments

- Free check started but not completed
- Free check completed, result viewed
- Offer viewed, checkout not started
- Checkout started but unpaid
- Paid, questionnaire incomplete
- Questionnaire complete, interview incomplete
- Interview complete, report pending
- Report delivered, consultation unbooked
- Consultation completed, implementation opportunity open
- Customer purchased; marketing suppressed

## Must not do

- Do not send marketing without appropriate consent
- Do not use fake scarcity
- Do not allow multiple active conflicting sequences
- Do not continue discount emails after purchase
- Do not create discounts outside approved Stripe controls
- Do not promise results or report timing not approved by Product and Operations

## Required deliverables

1. Stripe configuration specification
2. Promotion-code matrix
3. CRM pipeline and field map
4. Lifecycle event-to-message map
5. English email/SMS sequence
6. Spanish adapted sequence
7. Abandoned-checkout sequence
8. Paid onboarding and service communications
9. Suppression and consent rules
10. Attribution and reporting specification

## Acceptance criteria

- Every promotion has an owner, purpose, limit, and measurable result
- Purchase reliably suppresses prospect marketing
- Service messages continue when legally and operationally required
- English and Spanish customers receive correct-language communications
- CRM state matches product-delivery state
- Revenue can be attributed to source, campaign, and promotion code
