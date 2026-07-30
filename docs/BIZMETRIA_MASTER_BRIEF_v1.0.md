# BizMetria Master Brief

**Version:** 1.0  
**Status:** Approved baseline  
**Owner:** BizMetria Master Control  
**Last updated:** 2026-07-30

## 1. Purpose

BizMetria is a bilingual AI-powered business assessment platform for businesses across industries. It helps an owner identify where the company may be losing time, leads, operational efficiency, or visibility, and then produces a personalized AI and automation roadmap.

This file is the shared baseline for every BizMetria workstream and every dedicated ChatGPT project chat. No workstream may silently change approved facts in this document. Proposed changes must be submitted to Master Control as a Change Request and recorded in the Decision Log after approval.

## 2. Product identity

- **Brand:** BizMetria
- **Primary domain:** BizMetria.ai
- **Product category:** AI Business Diagnostic and Automation Roadmap
- **Target market:** Businesses across industries, initially focused on small and medium-sized businesses in the United States
- **Supported customer languages at launch:** English and Spanish
- **Voice interview architecture:** Separate phone number for English and separate phone number for Spanish
- **Public paid price:** $299 one-time
- **Implementation services:** Sold separately after the assessment

## 3. Core promise

### English

Discover where your business may be losing time, leads, and efficiency, then receive a personalized AI and automation roadmap.

### Spanish

Descubra dónde su negocio podría estar perdiendo tiempo, clientes potenciales y eficiencia, y reciba una hoja de ruta personalizada de IA y automatización.

## 4. Customer journey

1. A prospect discovers BizMetria through TikTok, YouTube, Instagram, Facebook, LinkedIn, search, referral, or direct outreach.
2. The prospect visits BizMetria.ai and chooses English or Spanish.
3. The prospect completes the free BizMetria AI Opportunity Check.
4. The platform calculates an AI Opportunity Score from 0 to 100.
5. The result page reveals only limited diagnostic information and displays locked sections from the complete assessment.
6. The prospect is offered the full BizMetria Business Assessment for $299.
7. If the prospect does not purchase, an email lifecycle sequence is started in the selected language.
8. The prospect can use a valid Stripe promotion code at checkout.
9. After payment, the customer completes an expanded business questionnaire.
10. The customer receives the correct phone number for the selected language.
11. The customer completes an adaptive AI voice interview of up to approximately 45 minutes.
12. The call recording and transcript are stored.
13. The AI Analysis Engine reviews the questionnaire, transcript, and approved solution library.
14. A personalized English or Spanish report is generated.
15. A human reviews the report before delivery during the MVP stage.
16. The customer receives the professional PDF report and books a results consultation.
17. BizMetria may offer a separately priced implementation project and optional ongoing optimization.

## 5. Free AI Opportunity Check

The free check is a lead-generation and qualification experience, not a replacement for the paid assessment.

### Goals

- Collect useful information in approximately 3–5 minutes
- Detect likely opportunity categories
- Generate a consistent AI Opportunity Score
- Provide a personalized but intentionally limited result
- Encourage purchase of the complete assessment
- Segment prospects for lifecycle marketing

### Approved structure

The free check contains 11 primary questions plus a contact form:

1. Business type
2. Team size
3. Approximate monthly new-customer inquiries
4. Customer contact channels
5. Typical response speed
6. Where leads and customers are tracked
7. Tasks that require too much manual work
8. Current follow-up process
9. Biggest current business challenge
10. Most desired improvement during the next 90 days
11. Desired implementation timing

### Free result may show

- AI Opportunity Score
- Opportunity level label
- One main observation
- Up to three broad opportunity categories
- Locked previews of deeper analysis sections
- Clear offer for the $299 complete assessment

### Free result must not reveal

- Full problem list
- Specific implementation architecture
- Complete tool recommendations
- Detailed financial estimates
- Full roadmap
- Full PDF report
- Voice analyst phone number
- Results consultation

## 6. AI Opportunity Score

The score ranges from 0 to 100 and estimates the breadth and potential significance of areas that may benefit from deeper analysis. It is not a financial, operational, or quality rating of the business.

### Score blocks

- **Lead Response and Follow-Up:** up to 30 points
- **Manual Work:** up to 25 points
- **Systems and Data:** up to 20 points
- **Strategic Priority:** up to 15 points
- **Opportunity Breadth:** up to 10 points

### Opportunity levels

- 0–24: Focused AI Opportunity
- 25–44: Moderate AI Opportunity
- 45–64: Strong AI Opportunity
- 65–79: High AI Opportunity
- 80–100: Very High AI Opportunity

The detailed scoring rules are owned by the Free Audit and Lead Scoring workstream.

## 7. Paid product

### Name

BizMetria Business Assessment

### Price

$299 one-time

### Approved customer deliverables

- Expanded business questionnaire
- Adaptive English or Spanish AI voice interview, generally up to 45 minutes
- Business-process analysis
- Identification of likely bottlenecks and manual work
- Approximately 8–15 personalized recommendations when supported by evidence
- AI and automation opportunity prioritization
- Impact vs. Effort matrix
- 30–90 day roadmap
- Professional PDF report in the customer’s selected language
- Approximately 30-minute results consultation

### Not included

- Building or implementing automations
- Software subscription fees
- Custom application development
- Guaranteed revenue or savings
- Legal, accounting, medical, cybersecurity, or financial advice

## 8. Promotion strategy

The public price remains $299. Discounts are controlled through Stripe coupons and promotion codes.

Approved discount range:

- $49 discount: customer pays $250
- $79 discount: customer pays $220
- $99 discount: customer pays $200
- $149 discount: customer pays $150
- $199 discount: customer pays $100

The largest discount is reserved for late-stage reactivation when the prospect appears unlikely to purchase at a higher price. Exact timing, eligibility, frequency caps, and code names are owned by Payments, CRM, and Lifecycle.

Rules:

- Discounts must be real and enforced by Stripe
- Expiration claims must match actual expiration
- Promotion codes do not stack
- One promotion code per order
- Purchased users immediately leave promotional sequences
- Service communications remain separate from marketing communications

## 9. Language architecture

English and Spanish use separate phone numbers to eliminate confusion and simplify prompt, voice, QA, and analytics management.

The two lines may differ in wording and cultural adaptation, but they must produce the same canonical structured data schema.

The full customer journey must be localized:

- Website
- Free audit
- Result page
- Checkout instructions
- Expanded questionnaire
- Voice interview
- Email and SMS
- Report
- Consultation booking
- Legal disclosures

Spanish content must be adapted naturally rather than translated word-for-word.

## 10. AI system architecture

BizMetria uses multiple coordinated AI components rather than one monolithic prompt.

### Core components

1. Free Audit Scoring Engine
2. English Voice Business Analyst
3. Spanish Voice Business Analyst
4. Business Classification Engine
5. Interview Quality Controller
6. Structured Summary Generator
7. AI Analysis Engine
8. Recommendation and Solution Library
9. Prioritization Engine
10. Report Generator
11. Human Review Workflow

### Universal-plus-modular interview model

BizMetria is marketed to all businesses, but the interview must not be generic. It uses:

- Universal business questions
- Business-type classification
- Business-model classification
- Industry modules
- Process modules such as leads, phone calls, scheduling, sales, documents, customer service, inventory, marketing, reporting, and employee coordination

## 11. Data principles

The platform may store:

- Customer identity and contact details
- Preferred language
- Business profile
- Questionnaire responses
- Payment and promotion metadata
- Call identifiers, recordings, transcripts, and timing
- Structured interview summary
- AI analysis outputs
- Report versions
- Consultation status
- Implementation opportunity status
- Consent records
- Audit logs and errors

Principles:

- Collect only what is necessary
- Separate marketing consent from service delivery
- Do not treat AI inference as fact
- Label estimates and assumptions
- Support deletion and retention rules
- Restrict access to customer recordings and reports
- Preserve the original interview language

## 12. MVP scope

### Required for MVP

- English and Spanish website paths
- Free AI Opportunity Check
- AI Opportunity Score
- Limited result page
- Stripe payment with promotion-code field
- Expanded paid questionnaire
- Separate English and Spanish phone numbers
- Voice interview and transcription
- Structured AI analysis
- Approved solution library
- PDF report generation
- Human report review
- Report delivery
- Consultation booking
- Basic CRM and status tracking
- Lifecycle email automation
- Product and funnel analytics

### Deferred until after validation

- Native mobile application
- Fully autonomous report delivery without human review
- Hundreds of industry modules
- White-label agency platform
- Marketplace of automations
- Deep customer CRM ingestion
- Automated competitor intelligence
- Multiple additional languages
- Complex customer portal features not required for delivery

## 13. Workstreams

The project is divided into 13 coordinated chats/workstreams:

1. Master Control
2. Product Strategy
3. Brand, Website and UX
4. Free Audit and Lead Scoring
5. English Voice Analyst
6. Spanish Voice Analyst
7. AI Analysis Engine
8. Report and PDF System
9. Backend, Data and Integrations
10. Payments, CRM and Lifecycle
11. Legal, Privacy and Security
12. Marketing, Content and Sales
13. QA, Analytics and Release

Each workstream has a dedicated brief in `docs/chat-briefs/`.

## 14. Governance

- This Master Brief is required context for every workstream.
- The Decision Log records approved global decisions.
- Master Control owns the source of truth.
- Workstreams may propose changes but cannot silently redefine approved scope.
- Every deliverable must include a version, status, dependencies, assumptions, open questions, and a Handoff Summary.
- Shared schemas and contracts must be documented, not implied through chat history.

## 15. Success criteria

The MVP is successful when a prospect can:

1. Complete the free check
2. Receive a consistent limited result
3. Purchase for $299 or with a valid promotion code
4. Complete the expanded questionnaire
5. Call the correct language line
6. Complete the adaptive interview
7. Receive a useful, evidence-grounded report
8. Book a consultation
9. Receive a relevant implementation offer

The business is commercially validated when paid assessments reliably convert into implementation revenue at acceptable acquisition and delivery costs.
