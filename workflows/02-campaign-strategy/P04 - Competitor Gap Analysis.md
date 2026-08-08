# P04 · Competitor Gap Analysis

**Section:** 02 — Campaign Strategy
**Workflow step:** Step 1 of 3
**Current version:** v1.2
**Status:** ✅ Tested
**Last updated:** August 2026

---

## 📌 Prompt Text (v1.2 — current)

> Copy this exactly into your AI tool. Replace all `[PLACEHOLDERS]` before running.

[ROLE]
You are a Lead Performance Strategist at a digital marketing agency.

[ACTION]
Perform a messaging gap analysis comparing our client's value proposition against raw competitor ad copy.

[CONTEXT]
Client Brand Guide (from P01):
"""
[P01_BRAND_GUIDE_OUTPUT]
"""

Competitor Ad Copy / Value Props:
"""
[COMPETITOR_RAW_COPY]
"""

[CHAIN-OF-THOUGHT INSTRUCTIONS]
1. Step 1: Identify the primary hooks and angles used by competitors.
2. Step 2: Spot key benefits or customer pain points that competitors are ignoring ("White Space").
3. Step 3: Map our client's unique positioning features to these ignored angles.

[CONSTRAINTS]
1. Rely ONLY on the provided brand guide and competitor copy.
2. Output must be structured, analytical, and actionable for copywriters.
3. Keep under 350 words.

[OUTPUT FORMAT]
- Competitor Dominant Hooks (Top 2-3 angles used in market)
- Market White Space (2 missed opportunities/angles)
- Recommended Strategic Differentiator Hooks (3 specific ad hook angles for P06)
```

**Placeholders to fill:**

| Placeholder | Source | Example |
|-------------|--------|---------|
| `[P01_BRAND_GUIDE_OUTPUT]` | Output from P01 | Paste P01 markdown output |
| `[COMPETITOR_RAW_COPY]` | Meta Ad Library text / Google Ads copy from competitors | Brand A: Premium organic beans, $25/bag. Brand B: $15 trial box... |

---

## 🏢 Intended Workflow or Task

Analyzes competitor advertising messaging to identify underserved messaging angles before creating ad copy.

- **Trigger:** Creative brief (P02) completed; competitor ad research gathered.
- **Actor:** Senior Performance Strategist reviews gaps.
 **Timing:** Day 2 of campaign launch planning.
- **Next step:** Feeds directly into P06 (Ad Copy Variant Generator).

```
Client Intake Form Uploaded → [THIS PROMPT RUNS] → Verified Brand Guide → Feeds P02 & P06
---

## ❗ Problem Being Solved

Agencies often write ad copy in a vacuum, creating campaigns that sound identical to existing market competitors. Strategists spend 3 to 4 hours manually auditing competitor Meta Ad Libraries.

**Pain points addressed:**
- Copywriters reusing saturated market hooks that result in high Ad Fatigue.
- Manual competitor ad analysis taking ~3.5 hours per campaign.
- Lack of clear differentiation in paid social ad copy.

---

## ⚡ Automation Potential

**Level:** High

| Dimension | Assessment |
|-----------|------------|
| Repetitiveness | High — executed for every paid media client setup. |
| Data availability | High — competitor ads easily pulled from Meta Ad Library / Google. |
| Human judgment needed | Medium — strategist confirms if identified white space is commercially viable. |
| Integration possibility | Medium — can connect to ad scraping workflows. 
| Estimated time saving | ~70% — reduces research and positioning synthesis from 3.5 hrs to 30 mins. |

**Human-in-the-loop role:** Senior Strategist verifies that identified "White Space" aligns with client operational capabilities.

---

## ⚠️ Risks and Limitations


| Risk | Level | Mitigation |
|------|-------|------------|
| Model assumes competitor features not in source text | Medium | Enforced strict Chain-of-Thought grounding steps. |
| Outdated competitor data used | Low | Competitor ad text must be gathered from live Meta Ad Library. |

**Overall risk rating:** LOW — Serves as internal strategy input prior to ad drafting.

---

## 🔄 Version History

### v1.0 — Initial unconstrained draft
**Date:** 2 August 2026
**Prompt:** Compare my client with these competitor ads and tell me what to write. 
**Output:** Generic advice like "focus on quality and speed".
**Observed effect:** Copywriters received high-level summaries that did not translate into distinct ad angles, requiring strategists to redo the competitive audit manually. 
**Lesson learned:** Lacks analytical steps and structured output requirements.  

---

### v1.1 — Basic Category Differentiation
**Date:** 4 August 2026
**Change:** Added structured headers asking for "Market Hooks" and "Differentiators".
**Output:** Better structure, but model made broad assumptions about competitor pricing models not present in input.
**Observed effect:** Output was partially helpful, but strategists spent 10 minutes correcting fabricated competitor claims.
**Lesson learned:** Must restrict analysis strictly to provided text and guide the evaluation step-by-step.  

---

### v1.2 — Chain-of-Thought (CoT) Strategy ✅ Current
Date:** 7 August 2026
**Change:** "Added Step 1/2/3 Chain-of-Thought instructions and structured output format.
**Output:** Highly specific, differentiated hook suggestions directly highlighting market gaps.
**Observed effect:** Reduced competitive gap analysis time to under 15 minutes, with copywriters immediately using the identified "White Space" hooks.
**Lesson learned:** CoT prompting dramatically improves strategic analytical tasks.

---

## 📊 A/B Test Results

**Test date:** 7 August 2026 | **Evaluators:** Sanzeena

| Criteria | v1.0 score | v1.2 score |
|----------|------------|------------|
| Clarity | 85/100 | 90/100 |
| Constraints | 60/100| 95/100 |
| Structure | 70/100 | 90/100 |
| Verifiability | 80/100 | 90/100 |
| Hallucination Risk | 90/100 | 95/100 |
| **Overall** | **77.5/100** | **91.5/100** |

---

## 🔗 Related Prompts

- **Previous in chain:** P02-creative-brief-generator.md
- **Next in chain:** P06-ad-variant-generator.md
- **Parent section:** 02-campaign-strategy README
