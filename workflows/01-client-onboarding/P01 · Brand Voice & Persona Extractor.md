# P01 · Brand Voice & Target Persona Extractor

**Section:** Client Onboarding  
**Workflow step:** Step 1 of 3
**Current version:** v1.2  
**Status:** ✅ Tested
**Last updated:** August 2026

---

## 📌 Prompt Text (v1.2 — current)

> Copy this exactly into your AI tool. Replace all `[PLACEHOLDERS]` before running.

You are a Lead Brand Strategist at a full-service digital marketing agency.

[TASK]
Analyze the provided raw client background text and extract a standardized Brand Voice & Target Persona Guide.

[CONTEXT]
We have onboarded a new client and need to extract their underlying brand voice, core positioning, and audience traits from their raw website copy or discovery documents. This guide will inform all downstream creative and ad copywriting work.

[CONSTRAINTS]
1. Use ONLY the facts, tone cues, and explicit statements present in the source text below. Do NOT extrapolate or invent brand facts.
2. If specific details (e.g., target demographics) are not mentioned, state "Not specified in intake text".
3. Maximum length: 350 words.
4. Tone: Professional, analytical, and structured.

[OUTPUT FORMAT]
Respond using the following structure:
- Core Brand Voice Traits (3-4 adjectives with 1-sentence explanations)
- Tone Rules (3 "Do's" and 3 "Don'ts" for copywriting)
- Target Audience Persona (Key pain points & primary motivations)
- Key Value Proposition (1-2 sentences summarizing their market position)

[SOURCE TEXT]
"""
[CLIENT_RAW_TEXT]
"""

```

**Placeholders to fill:**

| Placeholder | Source | Example |
|-------------|--------|---------|
| `[CLIENT_RAW_TEXT]` | Client website "About Us" page, intake form answers, or raw discovery transcript | Apex Logistics provides automated freight shipping for SMBs... |

---

## 🏢 Intended Workflow or Task

Automates the extraction of core branding attributes from raw client-provided text to establish a baseline brand strategy guide.  

- **Trigger:** Account Manager uploads client onboarding questionnaire or website copy.
- **Actor:** Account Strategist reviews and verifies the output.
- **Timing:** Day 1 of client onboarding.
- **Next step:** Feeds directly into P02 (Creative Brief Generator) and P06 (Ad Copy Variant Generator)

```
Client Intake Form Uploaded → [THIS PROMPT RUNS] → Verified Brand Guide → Feeds P02 & P06
---

## ❗ Problem Being Solved

Account managers typically spend 3 to 4 hours reviewing raw client websites, brand decks, and questionnaires to manually synthesize brand tone guidelines. This leads to inconsistent formatting and subjective interpretation across account teams, increasing the risk of off-brand ad creative.

**Pain points addressed:**
- High manual effort spent reviewing unorganized client onboarding copy (~3.5 hrs per client).
- Inconsistent tone definitions provided to copywriters and media buyers.
- Subjective hallucination of target audience traits by internal strategists.

---

## ⚡ Automation Potential

**Level:** High

| Dimension | Assessment |
|-----------|------------|
| Repetitiveness | High — required for every newly onboarded client. |
| Data availability | High — raw text is readily available in onboarding intake forms or public websites. |
| Human judgment needed | Low/Medium — strategist verifies tone accuracy in a 5-minute sanity check. |
| Integration possibility | High — can connect via Webhooks from Typeform/HubSpot directly into Notion or Asana. |
| Estimated time saving | ~80% — reduces process from 3.5 hours to 20 minutes per client. |

**Human-in-the-loop role:** Account Strategist verifies that extracted tone traits accurately reflect the client's actual market positioning before final sign-off.

---

## ⚠️ Risks and Limitations


| Risk | Level | Mitigation |
|------|-------|------------|
| Model infers target demographics not present in text | Medium | Enforced strict grounding constraint (Use ONLY facts present...) |
| Source text lacks sufficient detail | Medium | Instructed model to explicitly flag missing fields as "Not specified in intake text". |
| Overly generic voice traits (e.g., "Professional yet friendly") | Low | Enforced strict 3 "Do's" and 3 "Don'ts" structure for operational clarity. |

**Overall risk rating:** LOW — Strict grounding constraints are enforced in the prompt, and output is verified internally before client-facing usage.

---

## 🔄 Version History

### v1.0 — Initial draft
**Date:** 1 August 2026
**Prompt:** Read this client text and summarize their brand voice and audience.  
**Output:** Generative, overly verbose paragraphs. Model invented specific target income ranges and demographic details not in the source document.  
**Observed effect:** Account managers spent 15+ minutes editing out hallucinated demographic data. 
**Lesson learned:** Requires strict grounding constraints and structural rules.

---

### v1.1 — Structural Formatting & Section Limits
**Date:** 4 August 2026
**Change:** Added markdown headers, 350-word limit, and specific output sections (Do's/Don'ts)
**Output:** Formatting improved significantly. However, model still made assumptions about missing information 
**Observed effect:** Output quality was higher, but still required checking for factual drift.
**Lesson learned:** Must explicitly instruct the model how to handle missing data fields.

---

### v1.2 — Strict Grounding Clause ✅ Current
**Date:** 7 August 2026
**Change:** "Use ONLY the facts... present in source text. Do NOT extrapolate". Added fallback statement for missing data.
**Output:** Highly accurate, grounded brand voice guide matching source material precisely.
**Observed effect:** Reduced manual review time to <3 minutes per client.
**Lesson learned:** Grounding clauses eliminate creative hallucinations in analytical extraction tasks.

---

## 📊 A/B Test Results

**Test date:** 7 August 2026 | **Evaluators:** Sanzeena

| Criteria | v1.0 score | v1.2 score |
|----------|------------|------------|
| Clarity | 90/100 | 90/100 |
| Constraints | 70/100| 95/100 |
| Structure | 75/100 | 90/100 |
| Verifiability | 85/100 | 90/100 |
| Hallucination Risk | 90/100 | 95/100 |
| **Overall** | **82.25/100** | **91.5/100** |

---

## 🔗 Related Prompts

- **Previous in chain:** None (First prompt in onboarding workflow)
- **Next in chain:** P02-creative-brief-generator.md
- **Parent section:** 01-client-onboarding README
