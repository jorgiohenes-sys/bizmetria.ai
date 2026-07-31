# BizMetria Task Queue

**Owner:** Master Control  
**Purpose:** Provide every specialized chat with a GitHub-readable assignment so the user does not need to transfer task details manually.

## Task status values

- `QUEUED`
- `IN PROGRESS`
- `REVIEW`
- `BLOCKED`
- `APPROVED`
- `CANCELLED`

## Active tasks

### TASK-001 — Product Blueprint v0.1

**Owner workstream:** 02 — Product Strategy  
**Status:** IN PROGRESS  
**Priority:** P0  
**Target artifact:** `docs/workstreams/02-product-strategy/BIZMETRIA_PRODUCT_BLUEPRINT_v0.1.md`  
**Delivery method:** Feature branch + draft PR to `main`

**Objective:**

Define the complete product and commercial model for the $299 BizMetria Business Assessment.

**Required inputs:**

- `docs/BIZMETRIA_MASTER_BRIEF_v1.0.md`
- `docs/BIZMETRIA_COORDINATION_PROTOCOL_v1.0.md`
- `docs/BIZMETRIA_GITHUB_COLLABORATION_WORKFLOW_v1.0.md`
- `docs/BIZMETRIA_DECISION_LOG.md`
- `docs/chat-briefs/02_PRODUCT_STRATEGY.md`

**Required sections:**

1. Product definition and customer problem
2. Ideal and excluded customer profiles
3. Exact paid-assessment scope
4. Explicit exclusions
5. Free-versus-paid boundary
6. Recommended delivery timeline
7. Results-consultation scope
8. Three refund-policy models and recommendation
9. Discount ladder from $49 to $199 off
10. Implementation upsell framework
11. Preliminary unit economics with current-source verification
12. Product KPIs
13. Open decisions requiring Master Control
14. Handoff Summary

**Acceptance criteria:**

- Preserves approved $299 one-time price
- Does not change the free-check or bilingual phone architecture
- Clearly explains why the product is worth $299
- Defines measurable deliverables and operational boundaries
- Evaluates the economics of every discount level
- Separates approved facts from recommendations
- Identifies all required Change Requests
- Is stored in GitHub and submitted through a draft PR

**Downstream consumers:**

- 01 Master Control
- 03 Brand, Website and UX
- 08 Report and PDF System
- 10 Payments, CRM and Lifecycle
- 11 Legal, Privacy and Security
- 12 Marketing, Content and Sales

## Queued tasks

### TASK-002 — Formal Free Audit Specification

**Owner workstream:** 04 — Free Audit and Lead Scoring  
**Status:** QUEUED  
**Priority:** P0  
**Blocked by:** Master Control review of TASK-001 where free-versus-paid boundaries may affect presentation  
**Expected artifacts:**

- `FREE_AUDIT_QUESTION_SCHEMA_v0.1.json`
- `AI_OPPORTUNITY_SCORE_SPEC_v0.1.md`
- `FREE_RESULT_SELECTION_RULES_v0.1.md`

### TASK-003 — Product Experience Architecture

**Owner workstream:** 03 — Brand, Website and UX  
**Status:** QUEUED  
**Priority:** P1  
**Blocked by:** Approved Product Blueprint and formal free-audit specification

### TASK-004 — Legal and Data Inventory Baseline

**Owner workstream:** 11 — Legal, Privacy and Security  
**Status:** QUEUED  
**Priority:** P1  
**Blocked by:** Product Blueprint scope confirmation

## Completed tasks

### TASK-000 — Project Governance Baseline

**Owner:** Master Control  
**Status:** APPROVED  
**Outputs:** Master Brief, Coordination Protocol, Decision Log, 13 chat briefs, GitHub-native collaboration workflow, Project Status, and Task Queue.

## Assignment rule

A workstream starts only a task assigned to it. If no task is active, it must not invent a new cross-functional work package; it should ask Master Control to update this queue.
