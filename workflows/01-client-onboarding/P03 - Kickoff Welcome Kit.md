# P03 · Client Kickoff Welcome Kit Generator

**Section:** 01 — Client Onboarding
**Workflow step:** Step 3 of 3
**Current version:** v1.1
**Status:** ✅ Tested
**Last updated:** August 2026

---

## 📌 Prompt Text (v1.1 — current)

> Copy this exactly into your AI tool. Replace all `[PLACEHOLDERS]` before running.

```
[ROLE]
You are a Lead Account Manager at a digital marketing agency.

[ACTION]
Draft a professional, welcoming Client Kickoff Email and Onboarding Action Checklist for a newly onboarded client.

[CONTEXT]
Client Name: [CLIENT_NAME]
Primary Contact Name: [CONTACT_NAME]
Campaign Start Date: [START_DATE]
Target Deliverables: [DELIVERABLE_SUMMARY]
Key Onboarding Links:
- Asset Upload Portal: [ASSET_LINK]
- Kickoff Call Booking: [CALENDAR_LINK]

Brand Tone: Professional, warm, organized, and confident.

[CONSTRAINTS]
1. Maintain an encouraging and reassuring tone.
2. Clearly highlight immediate action items for the client with deadline expectations.
3. Keep the email copy under 250 words.
4. Do NOT include placeholder text in the body copy—use provided input variables.

[OUTPUT FORMAT]
- Email Subject Line Options (3 variations)
- Email Body Text
- Client Immediate Checklist (Bullet points with clear deadlines)
- Agency Next Steps (Brief 2-bullet summary)
```

**Placeholders to fill:**

| Placeholder | Source | Example |
|-------------|--------|---------|
| `[CLIENT_NAME]` | Account Contract | "Roasted Roost Coffee" |
| `[CONTACT_NAME]` | Primary Client Contact | "Sarah Jenkins" |
| `[START_DATE]` | Campaign Schedule| "Monday, September 1st" |
| `[DELIVERABLE_SUMMARY]` | Output from P02 | "Paid Search setup, Meta creative suite, monthly reporting" |
| `[ASSET_LINK]` | Agency Portal URL | "https://drive.google.com/agency-client-portal" |
| `[CALENDAR_LINK]` | Calendly/HubSpot Link | "https://calendly.com/agency-am/kickoff" |
---

## 🏢 Intended Workflow or Task

Automates the creation of client-facing kickoff communications, outlining immediate deliverables, asset requests, and meeting bookings. 

- **Trigger:** Creative brief (P02) approved by Lead Strategist.
- **Actor:** Account Manager reviews and dispatches email.
- **Timing:** Day 2 of client onboarding.
- **Next step:** Sent directly to client; client completes asset upload portal task.

```
P02 Creative Brief Approved → [THIS PROMPT RUNS] → AM Reviews Draft → Email Sent to Client
```

---

## ❗ Problem Being Solved

Account managers spend significant time re-drafting onboarding emails, gathering calendar links, and listing required assets manually. Missing details or unclear timelines cause delays in client asset delivery, pushing campaign launch dates back.

**Pain points addressed:**
- Inconsistent client onboarding experience across different account managers.
- Campaign launch delays caused by unclear asset upload instructions.
- Repetitive administrative drafting work (~1.5 hours per client).

---

## ⚡ Automation Potential

**Level:** Very High

| Dimension | Assessment |
|-----------|------------|
| Repetitiveness | Very High — identical structure used for every onboarded client. |
| Data availability | High — draws directly from CRM and P02 summary output. |
| Human judgment needed | Low — account manager verifies links, dates, and name spellings. |
| Integration possibility | High — fully automatable via Gmail/Outlook API or HubSpot workflows. |
| Estimated time saving | ~85% — reduces email/checklist prep time from 90 mins to 10 mins. |

**Human-in-the-loop role:** Account Manager verifies calendar links and contact names prior to pressing send.

---

## ⚠️ Risks and Limitations


| Risk | Level | Mitigation |
|------|-------|------------|
| Incorrect dates or broken URLs in email | MEDIUM | Explicit placeholder mapping table provided; AM manual verification. |
| Unclear client deadlines leading to launch delays | MEDIUM | Structured checklist format enforcing explicit relative deadlines (e.g., "by Friday"). |
| Overly informal or cold communication tone | Low | Explicit tone constraints set to "Professional, warm, organized, and confident". |

**Overall risk rating:** LOW — Standard operational draft with low financial or legal risk; human review takes <2 minutes.

---

## 🔄 Version History


### v1.0 — Initial draft
**Date:** 3 August 2026
**Prompt:** Prompt: Write a welcome email to [CLIENT_NAME] asking for assets and a kickoff meeting.
**Output:** Generic email without clear call-to-action buttons, subject line choices, or structured checklist.  
**Observed effect:** Required significant manual editing and adding of missing portal links 
**Lesson learned:** Must specify exact link variables and output structure components

---

### v1.1 — Structured Checklist & Variable Mapping ✅ Current
**Date:** 7 August 2026
**Change:** Added subject line options, explicit checklist format, word limits, and variable input mapping table.
**Output:** Highly polished, structured welcome email with clear client action items and professional tone.
**Observed effect:** Account manager prep time dropped to under 5 minutes per client.
**Lesson learned:** Providing explicit variable tags eliminates unparsed placeholders in final outputs.

---

## 📊 A/B Test Results

**Test date:** 7 August 2026 | **Evaluators:** Sanzeena

| Criteria | v1.0 score | v1.1 score |
|----------|------------|------------|
| Clarity | 85/100 | 90/100 |
| Constraints | 60/100| 85/100 |
| Structure | 70/100 | 90/100 |
| Verifiability | 75/100 | 80/100 |
| Hallucination Risk | 90/100 | 95/100 |
| **Overall** | **76.5/100** | **87.5/100** |

---

## 🔗 Related Prompts

- **Previous in chain:** P02-creative-brief-generator.md
- **Next in chain:** 02-campaign-strategy/P04-competitor-gap-analysis.md
- **Parent section:** 01-client-onboarding README
