# 📂 01 — Client Onboarding Workflow

**Business function:** Client Strategy & Account Management
**Trigger:** New client contract signed / Onboarding intake form submitted
**Prompts in this section:** P01, P02, P03  

---

## Section Purpose

These prompts automate the client onboarding and strategic kickoff phase for a full-service digital marketing agency. In high-velocity agencies, onboarding a new account typically involves hours of manual document analysis, creative briefing, and client communications. This prompt chain reduces account manager lead time from ~8 hours per new client to under 45 minutes, standardizing strategic outputs and accelerating campaign launch timelines.

## Chain Diagram

```
Contract Signed & Discovery Form Submitted
        │
        ▼
   P01 · Brand Voice Extractor          (Day 1 — Analyzes raw client assets)
        │
        ▼
   P02 · Creative Brief Generator     (Day 1 — Synthesizes discovery notes & P01)
        │
        ▼
   P03 · Kickoff Welcome Kit      (Day 2 — Generates onboarding email & action plan)
```

## Human-in-the-Loop Points

| Step | Human action required |
|------|-----------------------|
| P01 output | Account Strategist reviews extracted voice traits against raw client assets for accuracy |
| P02 output | Lead Strategist approves creative brief before sharing with design/media teams |
| P03 output | Account Manager checks kickoff timeline, dates, and milestone links before sending |

## Prompts

| File | Prompt | Status |
|------|--------|--------|
| [P01-brand-voice-extractor.md](P01-brand-voice-extractor.md) | Brand voice & persona extractor | ✅ Tested — v1.2 |
| [P02-creative-brief-generator.md](P02-creative-brief-generator.md) | Creative brief generator | ✅ Tested — v1.2 |
| [P03-kickoff-welcome-kit.md](P03-kickoff-welcome-kit.md) | Client kickoff welcome kit | ✅ Tested — v1.1 |