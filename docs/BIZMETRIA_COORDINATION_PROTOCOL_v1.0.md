# BizMetria Coordination Protocol

**Version:** 1.0  
**Status:** Approved baseline  
**Owner:** Master Control

## 1. Why this protocol exists

Dedicated ChatGPT chats do not automatically share complete working memory. BizMetria therefore uses explicit files, versioning, contracts, and handoffs to keep all workstreams synchronized.

## 2. Source-of-truth hierarchy

When information conflicts, use this order:

1. `BIZMETRIA_MASTER_BRIEF_v1.0.md`
2. `BIZMETRIA_DECISION_LOG.md`
3. Approved shared schemas and contracts
4. Approved workstream deliverables
5. Draft workstream notes
6. Chat conversation history

Conversation history alone is never the authoritative source for a cross-workstream decision.

## 3. Required startup procedure for every chat

At the beginning of a work session, the workstream must:

1. Read the current Master Brief.
2. Read the Decision Log.
3. Read its dedicated chat brief.
4. Read all named upstream dependencies.
5. State the versions being used.
6. Identify any missing inputs before making irreversible design decisions.

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

## 9. Handoff Summary format

Every completed work package must end with:

```markdown
# Handoff Summary

**Deliverable:**
**Version:**
**Status:** DRAFT / REVIEW / APPROVED
**Owner workstream:**
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

## 13. GitHub workflow

Recommended structure:

- `docs/` for source-of-truth specifications
- `docs/chat-briefs/` for dedicated chat instructions
- `schemas/` for JSON schemas
- `prompts/` for approved AI prompts
- `apps/` or implementation directories after architecture approval

Rules:

- Make changes on feature branches.
- Open draft pull requests for cross-functional changes.
- Reference Decision Log entries in PR descriptions.
- Do not merge breaking contract changes without affected-workstream review.
- Update documentation in the same PR as implementation when behavior changes.

## 14. Review gates

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

## 15. Definition of done

A work item is complete only when:

- The output is documented
- Acceptance criteria are met
- Required tests are included
- Dependencies are named
- English and Spanish impact is considered
- Security/privacy impact is considered
- Handoff Summary is included
- Master Control has approved it when global
