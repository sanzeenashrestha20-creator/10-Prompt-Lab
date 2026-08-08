# P07 · Short-Form Video Script Builder (TikTok / Reels / Shorts)

**Section:** 03 — Content Production
**Workflow step:** Step 1 of 2
**Current version:** v1.2
**Status:** ✅ Tested
**Last updated:** August 2026
---

## 📌 Prompt Text (v1.2 — current)

> Copy this exactly into your AI tool. Replace all `[PLACEHOLDERS]` before running.

```
[ROLE]
You are a Lead Short-Form Video Producer and UGC Scriptwriter.

[ACTION]
Transform a content calendar video hook into a production-ready, 30-second short-form video script (TikTok/Reels/Shorts).

[CONTEXT]
Client Name: [CLIENT_NAME]
Video Topic/Hook: [VIDEO_HOOK]
Brand Voice Guide (P01):
"""
[P01_BRAND_GUIDE_OUTPUT]
"""

[CONSTRAINTS]
1. Video length: Exactly 30 seconds (approx. 60–75 spoken words).
2. Format MUST be a 3-column table: [Timestamp | Visual / B-Roll Cues | Spoken Audio / On-Screen Text].
3. Include a strong visual hook in the first 3 seconds.
4. Tone: Energetic, authentic, and natural (avoid stiff corporate language).

[OUTPUT FORMAT]
- Video Concept Summary & Target Emotion
- Script Table (Columns: Timestamp, Visual/B-Roll Cues, Spoken Audio/Text)
- Call-to-Action (CTA) & Caption Draft with Hashtags

```

**Placeholders to fill:**

| Placeholder | Source | Example |
|-------------|--------|---------|
| `[CLIENT_NAME]` | Account Record | "Roasted Roost Coffee" |
| `[VIDEO_HOOK]` | Output from P05 / Intake Form | "Stop drinking coffee roasted last year!" |
| `[P01_BRAND_GUIDE_OUTPUT]` | Output from P01 | Paste P01 markdown output |

---

## 🏢 Intended Workflow or Task

Converts simple social media hooks from the content calendar into full production scripts with camera directions and spoken audio for UGC creators.

- **Trigger:** Content Calendar (P05) approved.
- **Actor:** Creative Producer / Video Editor reviews visual cues.
- **Timing:** Day 3 of monthly production cycle.
- **Next step:** Sent to UGC content creator for filming.

```
P05 Calendar Video Hook → [THIS PROMPT RUNS] → 3-Column Production Script → Sent to Creator

```

---

## ❗ Problem Being Solved

Creators often film vague, unscripted videos that miss key brand value propositions or fail to hook viewers in the first 3 seconds, leading to low retention and poor ad organic conversion.

**Pain points addressed:**
-Inconsistent video pacing and weak 3-second opening hooks.
- High manual drafting time spent writing camera directions (~2 hours per script pack).
- Content creators missing mandatory CTA elements.

---

## ⚡ Automation Potential

**Level:** High

| Dimension | Assessment |
|-----------|------------|
| Repetitiveness | High — run weekly for social media video assets. |
| Data availability | High — uses P05 video hooks and P01 brand guidelines. |
| Human judgment needed | Low/Medium — producer spot-checks visual cues for brand fit. |
| Integration possibility | High — markdown table converts directly into Notion script boards. |
| Estimated time saving | ~80% — reduces script preparation from 2 hours to 20 minutes. |

**Human-in-the-loop role:** Creative Producer verifies that B-roll suggestions are feasible within current production budgets.

---

## ⚠️ Risks and Limitations


| Risk | Level | Mitigation |
|------|-------|------------|
| Script exceeds 30-second timeframe | Medium | Word count constraint set to 60–75 words max. |
| Visual cues too complex for low-budget UGC | High | Explicitly constrained to authentic, accessible camera shots.|

**Overall risk rating:** LOW — Low risk operational asset for creative production.

---

## 🔄 Version History

### v1.0 — Initial unconstrained draft
**Date:** 2 August 2026
**Prompt:** Write a TikTok script about fresh coffee for Roasted Roost.
**Output:** Paragraph-style voiceover script with no camera directions or timestamps. 
**Observed effect:** Video editors had to manually structure the script into scenes before filming, adding 30 minutes of prep work per video. 
**Lesson learned:** Must mandate a 3-column table structure separating visual cues from audio.

---

### v1.1 — Table Format Constraint
**Date:** 5 August 2026
**Change:** Required a 3-column table for Timestamps, Visuals, and Audio.  
**Output:** Well-structured script layout, but spoken audio was too long for 30 seconds.
**Observed effect:** Creators spoke too fast trying to fit 150 words into 30 seconds, ruining video quality.
**Lesson learned:** Must limit word count strictly (60–75 words) to match pacing.

---

### v1.2 — Word Count & Pacing Rules ✅ Current
**Date:** 7 August 2026 
**Change:** Enforced 60–75 word limit and explicit 3-second hook constraint.
**Output:** Perfectly paced 30-second script with distinct visual cues and high retention hooks.
**Observed effect:** Production efficiency improved by 80% with zero script re-writes required by creators.
**Lesson learned:** Explicit word counts prevent voiceover timing overruns.

---

## 📊 A/B Test Results

**Test date:** 7 August 2026 | **Evaluators:** Sanzeena

| Criteria | v1.0 score | v1.2 score |
|----------|------------|------------|
| Clarity | 85/100 | 90/100 |
| Constraints | 65/100| 95/100 |
| Structure | 70/100 | 90/100 |
| Verifiability | 80/100 | 85/100 |
| Hallucination Risk | 90/100 | 90/100 |
| **Overall** | **77.25/100** | **89.5/100** |

---

## 🔗 Related Prompts

- **Previous in chain:** P05-multi-channel-calendar.md
- **Next in chain:** Video Recording / Editing Execution
- **Parent section:** 03-content-production README
