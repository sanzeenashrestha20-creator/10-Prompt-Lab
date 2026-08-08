# P06 · Ad Copy Variant Generator (PPC & Paid Social)

**Section:** 02 — Campaign Strategy
**Workflow step:** Step 3 of 3
**Current version:** v1.3
**Status:** ✅ Tested
**Last updated:** August 2026

---

## 📌 Prompt Text (v1.2 — current)

> Copy this exactly into your AI tool. Replace all `[PLACEHOLDERS]` before running.

```
[ROLE]
You are a Lead PPC Copywriter and Paid Social Specialist.

[ACTION]
Generate production-ready ad copy variants for Google Search PPC and Meta Ads based on the brand guide and competitor white space analysis.

[CONTEXT]
Client Name: [CLIENT_NAME]
Brand Guide (P01):
"""
[P01_BRAND_GUIDE_OUTPUT]
"""

Competitor White Space Hooks (P04):
"""
[P04_WHITE_SPACE_HOOKS]
"""

[CONSTRAINTS & NEGATIVE FILTERS]
1. Google Search Headlines: EXACTLY 30 characters maximum per headline. (Provide 5 variants).
2. Google Search Descriptions: EXACTLY 90 characters maximum per description. (Provide 3 variants).
3. Meta Ad Copy: 3 distinct body variants (Hook, Value Prop, CTA).
4. BANNED WORDS: Do NOT use "game-changer", "revolutionary", "seamless", or "snobbery".

[OUTPUT FORMAT]
- Google Search Headlines (5 bullet points with character counts listed)
- Google Search Descriptions (3 bullet points with character counts listed)
- Meta Paid Social Copy (3 structured variants with Hook, Body, and CTA)
```

**Placeholders to fill:**

| Placeholder | Source | Example |
|-------------|--------|---------|
| `[CLIENT_NAME]` | Account Record | "Roasted Roost Coffee" |
| `[P01_BRAND_GUIDE_OUTPUT]` | Output from P01 | Paste P01 markdown output |
| `[P04_WHITE_SPACE_HOOKS]` | Output from P04 | Paste P04 recommended hooks |

---

## 🏢 Intended Workflow or Task

Generates platform-compliant search ad headlines and paid social copy variants ready for A/B testing. 

- **Trigger:** Strategy and competitor gap analysis (P04) complete.
- **Actor:** PPC Specialist / Paid Social Buyer reviews output.
- **Timing:** Day 3 of campaign launch setup.
- **Next step:** Uploaded directly to Google Ads and Meta Ads Manager.

```
P01 Guide + P04 Gaps → [THIS PROMPT RUNS] → Platform Compliant Copy → Uploaded to Ad Managers
```

---

## ❗ Problem Being Solved

Copywriters frequently write Google Search headlines that exceed character limits (e.g., 32 characters instead of 30), causing rejection in Google Ads Manager. Manual copy variant generation takes 2–3 hours per campaign.

**Pain points addressed:**
- Disqualified PPC ads due to character limit overruns (>30 or >90 chars).
- Generic ad copy filled with overused buzzwords ("game-changing").
- High manual drafting time (~3 hours per ad set).

---

## ⚡ Automation Potential

**Level:** Very High

| Dimension | Assessment |
|-----------|------------|
| Repetitiveness | Very High — required for every ad campaign and refresh cycle. |
| Data availability | High — uses upstream P01 and P04 structured inputs. |
| Human judgment needed | Low — PPC manager spot-checks character count compliance. |
| Integration possibility | High — output directly formatted for bulk Google Ads CSV upload. |
| Estimated time saving | ~85% — reduces ad copywriting from 3 hours to 15 minutes. |

**Human-in-the-loop role:** PPC Manager spot-checks character counters before importing into ad platforms.
---

## ⚠️ Risks and Limitations


| Risk | Level | Mitigation |
|------|-------|------------|
| Character count calculation error by LLM | High | Mandated character count verification display in brackets. |
| Platform compliance / banned claim rules | MEDIUM | Banned buzzword list included in prompt constraints. |

**Overall risk rating:** Medium — Ad platform rejections can delay campaign launches if character limits fail.

---

## 🔄 Version History


### v1.0 — Initial draft
**Date:** 3 August 2026
**Prompt:** Prompt: Write Google ads and Facebook ads for Roasted Roost.
**Output:** Headlines were 38–45 characters long, completely unusable for Google Ads.  
**Observed effect:** 100% of generated Google Search headlines were rejected upon upload due to character limit overruns, requiring manual re-writing of every headline.
**Lesson learned:** Must enforce strict character constraints and character count reporting.

---

### v1.1 — Length Constraints Added
**Date:** 5 August 2026
**Change:** Added rule: "Headlines must be under 30 characters".
**Output:** Most headlines fit, but model included overused ad buzzwords like "game-changer" and "seamless".
**Observed effect:** Ad approval rate improved to 80%, but copy felt generic and contained clichéd marketing speak.
**Lesson learned:** Needs explicit negative constraints (banned words list).

---

### v1.2 — Negative Filters & Character Counters ✅ Current  
**Date:** 7 August 2026  
**Change:** Added hard 30/90 character constraints, a banned buzzword list, and forced bracketed character count reporting e.g. `[28 chars]`.  
**Output:** 100% compliant PPC headlines and Meta copy ready for platform upload without buzzwords.  
**Observed effect:** Ad variants passed platform validation immediately without manual editing, cutting ad creation time from 3 hours to 15 minutes.  
**Lesson learned:** Combining negative filters with forced self-reporting eliminates formatting and quality errors.

---


## 📊 A/B Test Results

**Test date:** 7 August 2026 | **Evaluators:** Sanzeena

| Criteria | v1.0 score | v1.1 score |
|----------|------------|------------|
| Clarity | 85/100 | 90/100 |
| Constraints | 60/100| 95/100 |
| Structure | 65/100 | 90/100 |
| Verifiability | 70/100 | 85/100 |
| Hallucination Risk | 90/100 | 90/100 |
| **Overall** | **74.25/100** | **89.5/100** |

---

## 🔗 Related Prompts

- **Previous in chain:** P04-competitor-gap-analysis.md
- **Next in chain:** Production Deployment (Google Ads & Meta Ads)
- **Parent section:** 02-campaign-strategy README
