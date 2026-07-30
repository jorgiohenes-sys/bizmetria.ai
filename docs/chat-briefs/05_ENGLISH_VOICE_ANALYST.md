# Chat Brief 05 — English Voice Analyst

**Role:** Owner of the English-language AI voice interview  
**Required context:** Master Brief, paid questionnaire schema, canonical interview-output schema, Legal recording requirements

## Mission

Design an English AI business analyst that conducts a natural, adaptive, evidence-gathering interview across industries and returns complete structured data for the Analysis Engine.

## Responsibilities

- Define the English agent persona and tone
- Write and maintain the English system prompt
- Create opening, recording disclosure, consent confirmation, and closing
- Build the universal interview core
- Build industry and process modules
- Define follow-up and clarification logic
- Prevent repetition and unsupported conclusions
- Handle interruptions, silence, off-topic answers, and disconnected calls
- Define completion criteria
- Produce the canonical structured interview output
- Create test conversations across business types

## Interview principles

- One question at a time
- Brief acknowledgements, not long lectures
- Ask for examples and quantities when useful
- Never invent missing details
- Separate facts, estimates, and uncertainty
- Reuse paid-questionnaire data instead of repeating it
- Explore the business process from inquiry through delivery, payment, follow-up, and reporting
- Do not recommend or sell during the evidence-gathering interview

## Required modules

- Company profile
- Customers and offers
- Lead sources and response
- Sales and conversion
- Scheduling and service delivery
- Administrative work
- Customer support
- Marketing and retention
- Systems and data
- Team coordination
- Pain points, priorities, urgency, and constraints

## Must not do

- Do not change the customer promise
- Do not copy Spanish wording into this prompt
- Do not produce a different data schema from the Spanish line
- Do not guarantee outcomes
- Do not expose confidential transcript data unnecessarily

## Required deliverables

1. English system prompt
2. Conversation state machine
3. Universal and modular question library
4. Completion checklist
5. Recovery and reconnection flow
6. Canonical output mapping
7. QA rubric
8. At least 15 representative test dialogues

## Acceptance criteria

- The interview feels conversational rather than scripted
- Required evidence is collected within a reasonable duration
- The agent does not repeat known information
- Output validates against the shared schema
- The English line can be tested independently from Spanish while remaining data-compatible
