# 📚 Prompt Library — Agency Workflow & Operations

> **Assessment 1 | Generative AI for Business**  
> Student: Sanzeena Shrestha | Business Field: Full-Service Digital Marketing Agency Operations 
> Model tested on: GPT-4.1 Mini
> Last updated: August 2026

---

## What This Library Does

This prompt library is designed to automate core workflows within a full-service digital marketing agency. By targeting key operational bottlenecks—such as manual client onboarding, strategy development, content production, and monthly performance reporting—this library standardizes generative AI usage across account management, strategy, and creative teams.

Each prompt entry follows the same structure:
- The exact prompt text (with placeholders)
- The workflow task it supports
- The problem it solves
- Its automation potential
- Known risks and mitigations
- Version history and test results

---

## 📂 Folder Structure

```
prompt-library/
│
├── README.md                        ← Library index & framework guide
│
├── 01 client-onboarding/
│   ├── README.md                    ← Section overview
│   ├── P01-brand-voice-extractor.md          ← Extracting guidelines from raw text
│   ├── P02-creative-brief-generator.md       ← Transforming call notes into briefs
│   └── P03-kickoff-welcome-kit.md            ← Drafting kickoff emails & action plans
│
├── 02-campaign-strategy/
│   ├── README.md                             ← Section overview
│   ├── P04-competitor-gap-analysis.md        ← Messaging & creative gap audits
│   ├── P05-multi-channel-calendar.md         ← 4-week thematic campaign planner
│   └── P06-ad-variant-generator.md           ← Search & social ad copy variants
│
├── 03-content-production/
│   ├── README.md                             ← Section overview
│   ├── P07-video-script-builder.md           ← TikTok/Reels/Shorts script writing
│   └── P08-seo-blog-outline.md               ← Search-intent aligned article outlines
│
└── 04-reporting-relations/
    ├── README.md                             ← Section overview
    ├── P09-kpi-performance-digest.md         ← Executive campaign reporting digests
    └── P10-churn-risk-turnaround-pitch.md   ← Account recovery & turnaround plans
```

> 💡 **Rename folders and files to match your chosen business field.**  
> The structure above is an example for HR/Retail operations.

---

## 📊 Library Summary Table

| ID | Prompt Name | Workflow | Automation Level | Risk Level | Status |
|----|-------------|----------|------------------|------------|--------|
| P01 | Brand Voice Extractor | Extracting brand guidelines from raw web text/decks | High | Low | ✅ Tested (v1.2) |
| P02 | Creative Brief Generator | Converting discovery call transcripts to structured briefs | High | Medium | ✅ Tested (v1.2) |
| P03 | Kickoff Welcome Kit | Drafting onboarding email suites & client action checklists | Very High | Low | ✅ Tested (v1.1) |
| P04 | Competitor Gap Analysis | Auditing competitor ad copy to spot messaging white space | Medium | Medium | ✅ Tested (v1.2) |
| P05 | Multi-Channel Calendar | Structuring 4-week cross-platform campaign schedules | High | Low | ✅ Tested (v1.1) |
| P06 | Ad Copy Variant Generator | Writing PPC & Paid Social copy under strict character counts | Very High | Medium | ✅ Tested (v1.3) |
| P07 | Video Script Builder | Generating short-form video scripts with visual/audio cues | High | Low | ✅ Tested (v1.1) |
| P08 | SEO Blog Outline | Drafting search-intent outlines with metadata & headers | High | Medium | ✅ Tested (v1.2) |
| P09 | KPI Performance Digest | Synthesizing monthly metric reports into plain-English summaries | Medium | High | ✅ Tested (v1.2) |
| P10 | Turnaround Pitch Drafter | Generating retention strategies and turnaround proposals | Medium | High | ✅ Tested (v1.1) |


**Automation levels:** 
**Very High / High:** Replaces 70%–90% of manual drafting; requires brief human review.  
**Medium:** Assists ideation and analysis; requires significant strategic human oversight.

**Risk levels:** 
**Low:** Low brand/financial risk; suitable for direct client-facing drafts after quick check.  
**Medium:** Creative or tactical risk; requires spot-checking for tone, accuracy, or character counts.  
**High:** High commercial/legal risk; requires mandatory human verification to prevent metric hallucination or over-promising.
---

## 🔗 Prompt Chaining Map

Prompts in this library are modular and designed to pass structured outputs directly into downstream tasks.

```
1. Client Onboarding & Strategy Chain
P01 Brand Voice Extractor → P02 Creative Brief Generator → P03 Kickoff Welcome Kit

2. Campaign Execution & Production Chain
P01 Brand Guide + P02 Brief → P04 Competitor Gap Analysis → P06 Ad Copy Variant Generator
P01 Brand Guide + Strategy → P05 Multi-Channel Calendar → P07 Video Script Builder & P08 SEO Blog Outline

3. Client Reporting & Retention Chain
P09 KPI Performance Digest → P10 Turnaround Pitch Drafter (if targets missed)
```

---

## ⚙️ Prompting Strategies Used

| Strategy | Prompts | Why chosen |
|----------|---------|------------|
| RACE framework (Role–Action–Context–Evaluation) | P02, P06, P10 | Establishes senior agency role persona; yields structured, client-ready proposals and briefs |
| Grounding constraint ("using only...") | P01, P08, P09 | Prevents metric hallucination and fabricated claims in client reports and SEO articles |
| Markdown Table / JSON output format | P05, P06, P07 | Ensures clean visual layout for content calendars and platform-compliant ad/script formatting |
| Word/Character & Negative constraints | P03, P06, P07 | Enforces strict Google PPC character limits (30/90 chars) and eliminates generic buzzwords |
| Self-critique step | P08, P09 | Forces the model to review its own output for unbacked performance claims before generating |

---

## 📝 Iteration Evidence

All prompt versions are saved in this repository. See individual prompt files for version histories.  
**Commit history = version log** — each commit message describes what changed and why.

| Prompt | Versions | Key improvement |
|--------|----------|-----------------|
| P01 | v1.0 → v1.2 | Added strict grounding clause (`using strictly source text`); edit time 15 min → 2 min |
| P04 | v1.0 → v1.2 | Added Chain-of-Thought reasoning steps for competitor ad audits; edit time 20 min → 4 min |
| P06 | v1.0 → v1.3 | Enforced character-count hard limits and negative keyword filters for PPC compliance |
| P09 | v1.0 → v1.2 | Separated metric parsing from narrative synthesis to eliminate metric calculation errors |
---

## 📖 References
- Anthropic (2025). *Prompt Engineering Overview.* docs.claude.ai
- Kartaca (2026). *Standardizing Enterprise Intelligence with a Corporate Prompt Library.*
- MIT Sloan (2025). *Prompt Engineering is So 2024 — Try These Prompt Templates Instead.*
- Microsoft (2025). *Get Started with Prompt Library — Copilot Studio.*
- VE3 Global (2025). *10 Key Elements of a Prompt Library for Enterprise Tasks.*