# 📂 02 — Campaign Strategy & Execution Workflow

**Business function:** Paid Media & Content Strategy
**Trigger:** Creative brief (P02) approved and client onboarded
**Prompts in this section:** P04, P05, P06

---

## Section Purpose

These prompts automate the strategic campaign execution phase. Translating high-level briefs into concrete ad variants, multi-channel schedules, and competitive positioning takes strategic teams 10–12 hours per campaign. This prompt chain reduces media planner time to under 1 hour while ensuring compliance with ad platform character limits and brand guidelines.

## Chain Diagram

```
Contract Signed & Discovery Form Submitted
        │
        ▼
   P04 · Competitor Gap Analysis    (Day 1 — Audits messaging & creative gaps)
        │
        ▼
   P05 · Multi-Channel Calendar     (Day 2 — 4-week thematic campaign planner)
        │
        ▼
   P06 · Ad Variant Generator      (Day 3 — Search & social ad copy variants)
```

## Human-in-the-Loop Points

| Step | Human action required |
|------|-----------------------|
| P04 output | Senior Strategist validates identified competitor gaps before ad drafting |
| P05 output | Content Lead checks theme alignment and resource availability for 4-week schedule |
| P06 output | PPC Specialist verifies character counts (30/90 chars) and compliance before upload to Google/Meta Ads |

## Prompts

| File | Prompt | Status |
|------|--------|--------|
| [P04-competitor-gap-analysis.md](P04-competitor-gap-analysis.md) | Competitor gap analysis | ✅ Tested — v1.2 |
| [P05-multi-channel-calendar.md](P05-multi-channel-calendar.md) | Multi-channel content calendar | ✅ Tested — v1.1 |
| [P06-ad-variant-generator.md](P06-ad-variant-generator.md) | Ad copy variant generator | ✅ Tested — v1.3 |