# BizMetria Coordination Protocol

**Version:** 1.0  
**Status:** Approved baseline with GitHub-native operating rules  
**Owner:** Master Control

## 1. Why this protocol exists

Dedicated ChatGPT chats do not automatically share complete working memory. BizMetria therefore uses explicit GitHub files, versioning, contracts, pull requests, and handoffs to keep all workstreams synchronized. The user must not serve as a manual document-transfer mechanism between chats.

## 2. Source-of-truth hierarchy

When information conflicts, use this order:

1. `BIZMETRIA_MASTER_BRIEF_v1.0.md`
2. `BIZMETRIA_DECISION_LOG.md`
3. `BIZMETRIA_COORDINATION_PROTOCOL_v1.0.md`
4. `BIZMETRIA_GITHUB_COLLABORATION_WORKFLOW_v1.0.md`
5. Approved shared schemas and contracts
6. Approved workstream deliverables in `main`
7. `BIZMETRIA_PROJECT_STATUS.md` and `BIZMETRIA_TASK_QUEUE.md`
8. Draft pull-request content
9. Chat conversation history

Conversation history alone is never the authoritative source for a cross-workstream decision.

## 3. Required startup procedure for every chat

At the beginning of a work session, the workstream must read directly from the current `main` branch:

1. `README.md`
2. The current Master Brief
3. This Coordination Protocol
4. `BIZMETRIA_GITHUB_COLLABORATION_WORKFLOW_v1.0.md`
5. The Decision Log
6. Project Status
7. Task Queue
8. Its dedicated chat brief
9. All named upstream dependencies

The chat must state the task ID and versions being used. It must not ask the user to upload or paste files that are already in GitHub.

## 4. Workstream boundaries

Each chat owns only its assigned domain. A workstream may identify cross-functional problems but must not silently redefine another workstream’s contract.

Examples:

- Website may propose a shorter questionnaire, but Free Audit owns scoring logic.
- Voice Analyst may propose a new data field, but Backend owns canonical schema changes.
- Marketing may propose a new discount, but Payments and Product Strategy own price and promotion rules.
- Report may propose new analysis sections, but AI Analysis Engine owns the evidence-producing analysis contract.

## 5. Deliverable status

Every deliverable must use one status:

- `DRAFT`: incomplete and not safe for implementation
- `REVIEW`: complete enough for cross-functional review
- `APPROVED`: accepted by Master Control and safe as a dependency
- `DEPRECATED`: no longer valid; replacement must be named

A specialist chat cannot mark a global deliverable `APPROVED` by itself.

## 6. Versioning

Use semantic document versions:

- `0.1`, `0.2`, etc. for drafts
- `0.9` for release candidate
- `1.0` for first approved baseline
- `1.1`, `1.2` for backward-compatible updates
- `2.0` for breaking changes

File naming example:

`FREE_AUDIT_SCHEMA_v1.0.json`

## 7. Decision process

### Local decision

A workstream may make a local decision when it does not change shared pricing, customer promises, canonical schemas, legal obligations, or another workstream’s interface.

### Global decision

A decision is global if it changes any of the following:

- Product price or deliverables
- Customer journey
- Supported languages
- Phone-line architecture
- Data collected or retained
- Scoring formula
- Shared API or JSON schema
- Report commitments
- Promotion strategy
- Legal disclosures
- Release criteria

Global decisions require Master Control approval and a Decision Log entry.

## 8. Change Request format

```markdown
# Change Request CR-XXX

**Requested by:**
**Date:**
**Affected decision or contract:**
**Current behavior:**
**Proposed behavior:**
**Reason:**
**Customer impact:**
**Technical impact:**
**Legal/privacy impact:**
**Affected workstreams:**
**Migration requirement:**
**Recommendation:** Approve / Reject / Investigate
```

A Change Request must be included in the workstream deliverable and PR description. It is not approved until Master Control records the decision.

## 9. Handoff Summary format

Every completed work package must include this block inside its primary GitHub deliverable:

```markdown
# Handoff Summary

**Deliverable:**
**Version:**
**Status:** DRAFT / REVIEW / APPROVED
**Owner workstream:**
**Task ID:**
**Purpose:**
**Inputs used:**
**Outputs created:**
**Decisions referenced:**
**Dependencies:**
**Consumers:**
**Assumptions:**
**Known limitations:**
**Open questions:**
**What must not be changed without approval:**
**Recommended next action:**
```

The user must not need to copy this block into another chat. Other chats read it from GitHub.

## 10. Shared contracts

The following artifacts must become explicit shared contracts before implementation:

- Free audit question schema
- Score calculation specification
- Lead-segmentation schema
- Paid questionnaire schema
- Canonical business profile schema
- Voice interview output schema
- Transcript metadata schema
- Analysis output schema
- Recommendation schema
- Report input schema
- Customer lifecycle event taxonomy
- CRM status model
- Consent and communication-preference schema

One workstream owns each contract, but all consumers must review breaking changes.

## 11. Canonical identifiers

Use stable IDs instead of UI labels whenever data crosses systems.

Example:

```json
{
  "question_id": "free_q05_response_speed",
  "answer_id": "next_business_day_or_later",
  "display_en": "The next business day or later",
  "display_es": "El siguiente día hábil o después"
}
```

English and Spanish interfaces must map to the same canonical IDs.

## 12. Language synchronization

- English and Spanish may use different natural wording.
- Canonical question IDs and output schemas must match.
- New fields must be added to both language paths.
- Spanish QA must evaluate naturalness, not only literal equivalence.
- Original-language transcripts are preserved.
- Reports are produced in the customer’s selected language.

## 13. Mandatory GitHub workflow

The complete operating procedure is defined in `BIZMETRIA_GITHUB_COLLABORATION_WORKFLOW_v1.0.md`.

Required repository structure:

- `docs/` for source-of-truth specifications and governance
- `docs/chat-briefs/` for dedicated chat instructions
- `docs/workstreams/` for versioned workstream deliverables
- `schemas/` for JSON schemas
- `prompts/` for approved AI prompts
- `apps/` or implementation directories after architecture approval

Rules:

1. Master Control assigns work through `BIZMETRIA_TASK_QUEUE.md`.
2. Specialists work on feature branches created from current `main`.
3. Every substantive result is stored in GitHub.
4. Specialists open draft pull requests for review.
5. Specialists do not merge cross-functional work without explicit authorization.
6. Master Control reviews files and PR diffs directly from GitHub.
7. Review corrections stay on the same PR branch.
8. Approved downstream work is read from `main`; the user does not copy documents between chats.
9. Documentation changes ship with implementation changes when behavior changes.
10. Secrets and customer-sensitive data are never committed.

## 14. Project status and task ownership

`BIZMETRIA_PROJECT_STATUS.md` is the authoritative workstream and gate-status registry.

`BIZMETRIA_TASK_QUEUE.md` is the authoritative assignment registry.

Only Master Control authoritatively updates these files. A specialist proposes status changes in its PR description and Handoff Summary.

Each active task must include:

- task ID;
- owner workstream;
- objective;
- required inputs;
- target artifacts;
- acceptance criteria;
- dependencies;
- downstream consumers;
- delivery method.

## 15. Review gates

### Gate 1: Product Approved

Product, $299 price, free check, customer journey, and promotion framework are approved.

### Gate 2: Experience Approved

Website flow, free audit UX, paid onboarding, language paths, and consent flow are approved.

### Gate 3: AI Approved

English voice agent, Spanish voice agent, analysis engine, output schemas, and report template pass tests.

### Gate 4: Platform Integrated

Stripe, database, CRM, voice calls, analysis, reports, and lifecycle messages work end-to-end.

### Gate 5: Pilot Ready

Cross-industry and bilingual QA passes; critical defects are closed.

### Gate 6: Production Launch

Pilot feedback is incorporated, legal pages are published, analytics are verified, and Master Control approves release.

## 16. Definition of done

A work item is complete only when:

- The output is stored in the correct GitHub path
- The document or contract is versioned
- Acceptance criteria are met
- Required tests or validations are included
- Dependencies and consumers are named
- English and Spanish impact is considered
- Security/privacy impact is considered
- Handoff Summary is included in the deliverable
- A draft PR exists for review
- Review corrections are resolved
- Master Control has approved it when global

## 17. Minimal user role

The user remains the product owner and final decision-maker but should normally need only to issue short commands:

- tell a workstream to execute its active GitHub task;
- tell Master Control to review a PR;
- answer a genuinely unresolved product decision;
- tell a workstream to address its GitHub review comments.

The user should not manually transfer specifications, handoffs, or completed deliverables between chats.
