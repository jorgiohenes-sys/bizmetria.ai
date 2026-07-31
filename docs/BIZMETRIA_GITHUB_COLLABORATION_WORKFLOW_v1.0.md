# BizMetria GitHub Collaboration Workflow

**Version:** 1.0  
**Status:** Approved operating baseline  
**Owner:** Master Control

## 1. Purpose

BizMetria work is distributed across specialized ChatGPT chats. The user must not act as a manual courier between chats. GitHub is the shared collaboration layer, and every substantive result must be stored there.

## 2. Core operating model

The normal flow is:

1. Master Control records an assignment in `docs/BIZMETRIA_TASK_QUEUE.md`.
2. A specialist chat reads the current `main` branch, its dedicated brief, and the active task.
3. The specialist creates a feature branch from `main`.
4. The specialist writes its versioned deliverable into the repository.
5. The specialist opens a draft pull request targeting `main`.
6. The specialist reports only the PR number, file paths, status, and blockers to the user.
7. The user tells Master Control to review that PR.
8. Master Control reads the PR directly from GitHub, requests changes or approves it, and merges it when ready.
9. Master Control updates the Decision Log, Project Status, and Task Queue when necessary.
10. Downstream chats read approved files from `main`; the user does not copy deliverable contents between chats.

## 3. Required files every chat must read

Before starting work, every chat must read the latest versions from `main`:

1. `README.md`
2. `docs/BIZMETRIA_MASTER_BRIEF_v1.0.md`
3. `docs/BIZMETRIA_COORDINATION_PROTOCOL_v1.0.md`
4. `docs/BIZMETRIA_GITHUB_COLLABORATION_WORKFLOW_v1.0.md`
5. `docs/BIZMETRIA_DECISION_LOG.md`
6. `docs/BIZMETRIA_PROJECT_STATUS.md`
7. `docs/BIZMETRIA_TASK_QUEUE.md`
8. Its dedicated file under `docs/chat-briefs/`
9. Any upstream deliverables named in its active task

A chat must not ask the user to upload or paste files that are already available in the repository.

## 4. Branch naming

Use one branch per work package:

`workstream/<number>-<short-description>`

Examples:

- `workstream/02-product-blueprint-v0-1`
- `workstream/04-free-audit-schema-v0-1`
- `workstream/05-english-voice-prompt-v0-1`
- `master-control/approve-product-blueprint`

If the GitHub integration requires another prefix, `agent/` is acceptable, but the workstream number and purpose must remain visible.

## 5. Deliverable locations

Workstream outputs belong under:

`docs/workstreams/<number>-<workstream-name>/`

Examples:

- `docs/workstreams/02-product-strategy/BIZMETRIA_PRODUCT_BLUEPRINT_v0.1.md`
- `docs/workstreams/04-free-audit/FREE_AUDIT_SCHEMA_v0.1.json`
- `docs/workstreams/05-english-voice/ENGLISH_VOICE_PROMPT_v0.1.md`
- `docs/workstreams/08-report-system/REPORT_STRUCTURE_v0.1.md`

Shared machine-readable contracts belong under `schemas/`. Approved AI prompts belong under `prompts/`.

## 6. Specialist chat procedure

A specialist chat must:

1. Read the required source files from `main`.
2. Find the task assigned to its workstream in the Task Queue.
3. Confirm the task ID, inputs, required output, and acceptance criteria.
4. Create a branch from the current `main`.
5. Create or update only files within its authorized scope.
6. Include the required Handoff Summary inside the primary deliverable.
7. Open a draft PR targeting `main`.
8. In the PR body, include:
   - task ID;
   - deliverables created;
   - decisions referenced;
   - assumptions;
   - affected workstreams;
   - checks performed;
   - open questions;
   - Change Requests, if any.
9. Do not merge its own cross-functional deliverable.
10. Return a compact completion message containing only:
   - PR number and link;
   - branch name;
   - file paths;
   - deliverable status;
   - blockers or decisions needed.

The full deliverable must live in GitHub, not only in chat history.

## 7. Master Control review procedure

When the user says, for example, `Review PR #7`, Master Control must:

1. Fetch PR metadata and all changed files.
2. Read the full primary deliverables, not only the PR summary.
3. Compare the work against:
   - Master Brief;
   - Decision Log;
   - active task acceptance criteria;
   - upstream contracts;
   - affected downstream workstreams.
4. Check whether the work introduces an undocumented global decision.
5. Check bilingual, privacy, security, cost, and implementation impacts when relevant.
6. Either:
   - request specific corrections;
   - approve with explicit limitations;
   - reject with reasons;
   - merge if it is ready.
7. After approval, update governance artifacts when needed:
   - `BIZMETRIA_DECISION_LOG.md`;
   - `BIZMETRIA_PROJECT_STATUS.md`;
   - `BIZMETRIA_TASK_QUEUE.md`;
   - related Master Brief or shared contracts.
8. Assign the next dependent task.

## 8. Authority rules

### Specialist chats may

- create local draft decisions within their own scope;
- create feature branches;
- write versioned deliverables;
- open draft PRs;
- propose Change Requests;
- respond to review comments.

### Specialist chats may not

- silently change approved global decisions;
- edit an approved shared contract without naming affected consumers;
- mark their own global deliverable `APPROVED`;
- merge a cross-functional PR unless Master Control explicitly authorizes it;
- edit the Decision Log as though a proposal were approved;
- overwrite another workstream's artifact without coordination.

### Master Control may

- approve or reject global proposals;
- merge approved workstream PRs;
- update governance files;
- assign work and dependencies;
- resolve ownership conflicts;
- approve release gates.

## 9. Status synchronization

`docs/BIZMETRIA_PROJECT_STATUS.md` contains the current state of each workstream.

`docs/BIZMETRIA_TASK_QUEUE.md` contains active, queued, blocked, and completed tasks.

Only Master Control should authoritatively change these files. A specialist may propose a status update in its PR description or Handoff Summary.

## 10. PR status mapping

- Work in progress: Draft PR
- Complete for review: Draft PR with deliverable status `REVIEW`
- Corrections requested: PR remains open
- Accepted: Master Control merges PR
- Approved dependency: file is in `main` and marked `APPROVED`, or Master Control explicitly records approval

A merged draft document does not automatically become approved unless its document status or Decision Log entry says so.

## 11. Handling changes after review

If Master Control requests corrections, the specialist chat must:

1. Read the PR comments directly from GitHub.
2. Update the same branch and PR.
3. Reply to or resolve each actionable comment.
4. Update the document version when appropriate.
5. Report that the PR is ready for another review.

The user should not copy review comments between chats.

## 12. Downstream handoff

After a PR is merged, the user may tell the downstream chat only:

`Read the current main branch, your active task in BIZMETRIA_TASK_QUEUE.md, and all dependencies named there. Start the task and publish the result through a draft PR.`

The downstream chat must find and read the approved upstream files itself.

## 13. Minimal user interactions

The desired user workflow is limited to commands such as:

- `Open the repository and execute your active workstream task.`
- `Review PR #7 and process it according to the GitHub workflow.`
- `Read current main and begin the next approved task.`
- `Read the review comments on your PR and fix them.`

The user should not need to paste specifications, Handoff Summaries, patches, or complete deliverables between chats.

## 14. Exceptions

Manual copying is acceptable only when:

- GitHub access is unavailable in a specific chat;
- a file is not yet in the repository;
- the user is making an explicit product decision not already documented;
- sensitive information must not be committed to the repository.

Secrets, credentials, customer personal data, recordings, and production keys must never be committed to GitHub.

## 15. Definition of success

This workflow is functioning correctly when:

- every substantive deliverable exists in GitHub;
- each task has one owner and one task ID;
- each review occurs through a PR;
- Master Control can understand progress without copied chat messages;
- downstream chats can start from `main` without asking the user for context;
- the user acts as decision-maker, not as a document-transfer mechanism.
