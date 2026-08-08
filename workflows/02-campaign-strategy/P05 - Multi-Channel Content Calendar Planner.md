# P05 · Multi-Channel Content Calendar Planner

**Section:** 02 — Campaign Strategy
**Workflow step:** Step 2 of 3
**Current version:** v1.1
**Status:** ✅ Tested
**Last updated:** August 2026

---

## 📌 Prompt Text (v1.1 — current)

> Copy this exactly into your AI tool. Replace all `[PLACEHOLDERS]` before running.

```
[ROLE]
You are a Lead Content Strategist at a digital marketing agency.

[ACTION]
Generate a 4-week thematic Multi-Channel Content Calendar based on the brand strategy and campaign objectives.

[CONTEXT]
Client Name: [CLIENT_NAME]
Core Campaign Theme: [CAMPAIGN_THEME]
Target Channels: SEO Blog, Instagram/TikTok Video, Email Newsletter

Brand Voice & Positioning (from P01):
"""
[P01_BRAND_GUIDE_OUTPUT]
"""

[CONSTRAINTS]
1. Layout MUST be formatted as a Markdown Table.
2. Ensure weekly content themes connect logically across channels.
3. Keep post descriptions concise and production-ready.

[OUTPUT FORMAT]
A Markdown Table with the following columns:
| Week | Focus Theme | SEO Blog Topic | Short-Form Video Hook (IG/TikTok) | Email Newsletter Subject Line |

```

**Placeholders to fill:**

| Placeholder | Source | Example |
|-------------|--------|---------|
| `[CLIENT_NAME]` | Client Account Record | "Roasted Roost Coffee" |
| `[CAMPAIGN_THEME]` | Output from P02 | "Freshness First: Ditching Stale Supermarket Coffee" |
| `[P01_BRAND_GUIDE_OUTPUT]` | Output from P01 | [Paste P01 markdown output] |

---

## 🏢 Intended Workflow or Task

Structures a 4-week multi-channel organic content schedule to maintain messaging consistency across platforms.  

- **Trigger:** Campaign Strategy approved.
- **Actor:** Content Manager reviews schedule.
- **Timing:** Day 2 of campaign setup.
- **Next step:** Feeds into P07 (Video Script Builder) and P08 (SEO Blog Outline).

```
Campaign Theme Set → [THIS PROMPT RUNS] → 4-Week Markdown Table → Feeds P07 & P08

```

---

## ❗ Problem Being Solved

Planning content across multiple channels leads to siloed messaging where social media, email, and blog teams work in isolation. Manual calendar drafting takes 4+ hours per month.

**Pain points addressed:**
- Disconnected messaging across social, email, and SEO blog channels.
- High manual drafting time (~4 hours per monthly calendar).
- Unclear weekly content themes.
---

## ⚡ Automation Potential

**Level:** High

| Dimension | Assessment |
|-----------|------------|
| Repetitiveness | High — run monthly for all organic retainers. |
| Data availability | High — uses brand guide (P01) and theme input. |
| Human judgment needed | Low/Medium — Content Lead approves topic viability. |
| Integration possibility | High — Markdown table easily converts to CSV for Notion/Asana. |
| Estimated time saving | ~80% — reduces calendar planning from 4 hours to 30 minutes. |

**Human-in-the-loop role:** Content Manager verifies topic feasibility before assigning scripts to creators.

---

## ⚠️ Risks and Limitations


| Risk | Level | Mitigation |
|------|-------|------------|
| Unrealistic production scope | Medium | Constrained calendar to 3 primary core channels. |
| Generic video hooks | Low | Feeds downstream into P07 for full script generation. |

**Overall risk rating:** Low — Internal editorial planning tool with minimal operational risk.

---

## 🔄 Version History

### v1.0 — Initial unconstrained draft
**Date:** 3 August 2026
**Prompt:** Give me a 4-week content calendar for a coffee brand. 
**Output:** Bulleted list organized by day, difficult to import or review.  
**Observed effect:** Content managers had to manually copy-paste individual items into spreadsheets, taking ~45 minutes of manual reformatting per calendar. 
**Lesson learned:** Must mandate Markdown Table structure.

---

### v1.1 — Table Formatting Constraint ✅ Current
**Date:** 5 August 2026
**Change:** Enforced Markdown table structure with exact column headings matching agency channels.  
**Output:** Clean 4-week matrix ready for copy-pasting into project boards.
**Observed effect:** Zero reformatting needed; team directly copied markdown table into Notion, saving ~35 minutes per plan.
**Lesson learned:** Table constraints ensure production-ready outputs.

---

## 📊 A/B Test Results

**Test date:** 7 August 2026 | **Evaluators:** Sanzeena

| Criteria | v1.0 score | v1.1 score |
|----------|------------|------------|
| Clarity | 85/100 | 90/100 |
| Constraints | 70/100| 85/100 |
| Structure | 75/100 | 90/100 |
| Verifiability | 60/100 | 80/100 |
| Hallucination Risk | 80/100 | 85/100 |
| **Overall** | **75.5/100** | **86.25/100** |

---

## 🔗 Related Prompts

- **Previous in chain:** P01-brand-voice-extractor.md
- **Next in chain:** P07-video-script-builder.md & P08-seo-blog-outline.md
- **Parent section:** 02-campaign-strategy README
