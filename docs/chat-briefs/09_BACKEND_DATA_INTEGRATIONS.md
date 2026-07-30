# Chat Brief 09 — Backend, Data and Integrations

**Role:** Owner of system architecture, database, APIs, events, integrations, reliability, and operational state  
**Required context:** Master Brief, all approved schemas, Stripe contract, voice-provider contract, report contract, Legal data requirements

## Mission

Design and implement the reliable technical backbone that connects the website, free check, Stripe, questionnaires, language-specific voice lines, transcription, analysis, report generation, CRM, and lifecycle communications.

## Responsibilities

- Select and document the implementation architecture after approval
- Design canonical database entities and relationships
- Define API and webhook contracts
- Define customer and assessment status machines
- Store questionnaire, payment, consent, call, transcript, analysis, report, and consultation metadata
- Orchestrate asynchronous processing and retries
- Maintain idempotency and prevent duplicate processing
- Protect sensitive recordings and reports
- Provide admin operations and audit logging
- Define observability, failure recovery, and data export/deletion paths

## Core entities

- User/customer
- Business
- Free assessment
- Paid order
- Promotion attribution
- Expanded questionnaire
- Voice interview
- Recording and transcript
- Structured interview summary
- Analysis run
- Recommendation
- Report and report version
- Consultation
- Implementation opportunity
- Consent record
- Lifecycle event
- Error and audit log

## Required lifecycle states

At minimum:

- Lead captured
- Free check completed
- Checkout started
- Paid
- Questionnaire pending/completed
- Interview ready/started/completed
- Analysis queued/running/failed/completed
- Human review pending/approved
- Report delivered
- Consultation booked/completed
- Proposal sent/won/lost

## Must not do

- Do not select vendors without recording tradeoffs
- Do not let UI labels become database identifiers
- Do not store sensitive data without access and retention rules
- Do not process Stripe or voice webhooks without signature validation and idempotency
- Do not merge English and Spanish phone routing into one ambiguous line
- Do not bypass human report approval during MVP

## Required deliverables

1. Architecture decision record
2. Database schema
3. API specification
4. Event taxonomy
5. Webhook map
6. State machines
7. Error and retry rules
8. Access-control model
9. Data retention/deletion implementation plan
10. Admin operations specification
11. Integration test plan

## Acceptance criteria

- End-to-end processing can recover from duplicate and failed events
- Every customer artifact is traceable by stable IDs
- Language routing is explicit
- Shared schemas are enforced
- Sensitive files are protected
- Operational staff can identify and retry failed stages safely
