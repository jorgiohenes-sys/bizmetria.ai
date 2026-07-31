# BizMetria.ai

BizMetria is a bilingual AI-powered business assessment platform for companies across industries.

## Approved product baseline

- Brand and domain: **BizMetria.ai**
- Public paid product: **BizMetria Business Assessment**
- Price: **$299 one-time**
- Launch languages: **English and Spanish**
- Voice architecture: **separate English and Spanish phone numbers**
- Primary funnel: free AI Opportunity Check → paid assessment → report consultation → separately priced implementation

## Project documentation

### Shared source of truth

- [`docs/BIZMETRIA_MASTER_BRIEF_v1.0.md`](docs/BIZMETRIA_MASTER_BRIEF_v1.0.md) — universal product and project brief required by every chat
- [`docs/BIZMETRIA_COORDINATION_PROTOCOL_v1.0.md`](docs/BIZMETRIA_COORDINATION_PROTOCOL_v1.0.md) — synchronization, versioning, handoff, and change-control rules
- [`docs/BIZMETRIA_GITHUB_COLLABORATION_WORKFLOW_v1.0.md`](docs/BIZMETRIA_GITHUB_COLLABORATION_WORKFLOW_v1.0.md) — GitHub-native workflow that removes manual document copying between chats
- [`docs/BIZMETRIA_DECISION_LOG.md`](docs/BIZMETRIA_DECISION_LOG.md) — approved global decisions and pending decisions
- [`docs/BIZMETRIA_PROJECT_STATUS.md`](docs/BIZMETRIA_PROJECT_STATUS.md) — authoritative workstream and release-gate status
- [`docs/BIZMETRIA_TASK_QUEUE.md`](docs/BIZMETRIA_TASK_QUEUE.md) — active and queued assignments for every workstream
- [`docs/CHAT_STARTUP_INSTRUCTIONS.md`](docs/CHAT_STARTUP_INSTRUCTIONS.md) — universal initialization instructions for new specialist chats

### Dedicated ChatGPT workstream briefs

1. [`01_MASTER_CONTROL.md`](docs/chat-briefs/01_MASTER_CONTROL.md)
2. [`02_PRODUCT_STRATEGY.md`](docs/chat-briefs/02_PRODUCT_STRATEGY.md)
3. [`03_BRAND_WEBSITE_UX.md`](docs/chat-briefs/03_BRAND_WEBSITE_UX.md)
4. [`04_FREE_AUDIT_LEAD_SCORING.md`](docs/chat-briefs/04_FREE_AUDIT_LEAD_SCORING.md)
5. [`05_ENGLISH_VOICE_ANALYST.md`](docs/chat-briefs/05_ENGLISH_VOICE_ANALYST.md)
6. [`06_SPANISH_VOICE_ANALYST.md`](docs/chat-briefs/06_SPANISH_VOICE_ANALYST.md)
7. [`07_AI_ANALYSIS_ENGINE.md`](docs/chat-briefs/07_AI_ANALYSIS_ENGINE.md)
8. [`08_REPORT_PDF_SYSTEM.md`](docs/chat-briefs/08_REPORT_PDF_SYSTEM.md)
9. [`09_BACKEND_DATA_INTEGRATIONS.md`](docs/chat-briefs/09_BACKEND_DATA_INTEGRATIONS.md)
10. [`10_PAYMENTS_CRM_LIFECYCLE.md`](docs/chat-briefs/10_PAYMENTS_CRM_LIFECYCLE.md)
11. [`11_LEGAL_PRIVACY_SECURITY.md`](docs/chat-briefs/11_LEGAL_PRIVACY_SECURITY.md)
12. [`12_MARKETING_CONTENT_SALES.md`](docs/chat-briefs/12_MARKETING_CONTENT_SALES.md)
13. [`13_QA_ANALYTICS_RELEASE.md`](docs/chat-briefs/13_QA_ANALYTICS_RELEASE.md)

## GitHub-native operating model

The user should not manually copy deliverables between project chats.

1. Master Control assigns work in `BIZMETRIA_TASK_QUEUE.md`.
2. A specialist reads the current `main` branch and its active task.
3. The specialist creates a feature branch and stores the complete deliverable in GitHub.
4. The specialist opens a draft PR targeting `main`.
5. Master Control reviews the PR directly in GitHub, requests corrections or merges it.
6. Downstream chats read approved files from `main`.

The user normally needs to provide only short commands such as:

- `Open the repository and execute your active workstream task.`
- `Review PR #7 according to the GitHub collaboration workflow.`
- `Read current main and begin the next approved task.`
- `Read your PR review comments and fix them.`

## How to start a new project chat

1. Give the chat its workstream name or number.
2. Tell it to open `jorgiohenes-sys/bizmetria.ai` on `main`.
3. Tell it to read `docs/CHAT_STARTUP_INSTRUCTIONS.md` and follow it.
4. The chat must find its own dedicated brief, active task, and dependencies in GitHub.
5. Every substantive result must be delivered through a draft PR.

## Governance

GitHub specifications are the source of truth. Chat conversation may explore ideas, but global changes are not approved until Master Control records them in the Decision Log and relevant versioned specifications.

Secrets, production credentials, customer personal data, recordings, and private keys must never be committed to the repository.
