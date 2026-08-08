# P10 · Churn Risk Account Turnaround Pitch Plan

**Section:** 04 — Reporting & Client Relations
**Workflow step:** Step 2 of 2
**Current version:** v1.2
**Status:** ✅ Tested
**Last updated:** August 2026

---

## 📌 Prompt Text (v1.1 — current)

> Copy this exactly into your AI tool. Replace all `[PLACEHOLDERS]` before running.

```
[ROLE]
You are a Senior Client Success Director and Campaign Turnaround Strategist.

[ACTION]
Develop an executive Account Turnaround Strategy & Re-engagement Pitch for an underperforming or churn-risk client account.

[CONTEXT]
Client Name: [CLIENT_NAME]
Underperformance Root Cause: [UNDERPERFORMANCE_REASON]
Recent Performance Digest (P09):
"""
[P09_DIGEST_OUTPUT]
"""

Agency Action Budget / Concessions: [PROPOSED_CONCESSIONS]

[CONSTRAINTS]
1. Tone: Empathetic, accountable, highly confident, and solution-focused.
2. Acknowledge performance gaps transparently without making excuses.
3. Present a concrete 30-Day Turnaround Roadmap.
4. Keep proposal under 400 words.

[OUTPUT FORMAT]
1. Performance Accountability Statement
2. Root Cause Analysis & Lessons Learned
3. 30-Day Recovery Roadmap (Week 1 to Week 4 Action Plan)
4. Agency Commitment & Commercial Alignment (No-risk concession or trial offer)

```

**Placeholders to fill:**

| Placeholder | Source | Example |
|-------------|--------|---------|
| `[CLIENT_NAME]` | Account Record | "Roasted Roost Coffee" |
| `[UNDERPERFORMANCE_REASON]` | Internal Post-Mortem | "Meta CPMs spiked 40%; ad fatigue on primary video creative" |
| `[P09_DIGEST_OUTPUT]` | Output from P09 | Paste P09 performance digest markdown |
| `[PROPOSED_CONCESSIONS]` | Account Director approval | Free creative production refresh (2 new video ads) + $0 agency fee on spend overrun |

---

## 🏢 Intended Workflow or Task

Generates a structured recovery pitch and action plan to save churn-risk client accounts facing performance dips.

- **Trigger:** KPI Performance Digest (P09) shows missed targets; client expresses dissatisfaction.
- **Actor:** Head of Client Success presents plan to client leadership.
- **Timing:** Within 48 hours of identifying churn risk.
- **Next step:** Presented in executive realignment call to retain contract.

```
P09 Identifies Churn Risk → [THIS PROMPT RUNS] → Turnaround Strategy → Realignment Pitch Call

```

---

## ❗ Problem Being Solved

When campaign performance drops, panicked account teams spend days writing defensive emails or unstructured turnaround plans, often losing the account due to lack of immediate strategic accountability.

**Pain points addressed:**
- High client churn rates due to slow agency response times during performance dips.
- Defensive or excuse-laden communication from account managers.
- Unstructured recovery plans lacking weekly accountability milestones.

---

## ⚡ Automation Potential

**Level:** High

| Dimension | Assessment |
|-----------|------------|
| Repetitiveness | Medium/High — executed whenever an account enters red status. |
| Data availability | High — uses P09 performance outputs and internal post-mortem notes. |
| Human judgment needed | High — Head of Client Success approves commercial concessions. |
| Integration possibility | Medium — connects to CRM churn alerts (HubSpot/Gainsight). |
| Estimated time saving | ~75% — reduces turnaround plan drafting from 5 hours to 45 minutes. |

**Human-in-the-loop role:** Head of Client Success reviews turnaround commitments and approves financial/resource concessions before speaking to client.

---

## ⚠️ Risks and Limitations


| Risk | Level | Mitigation |
|------|-------|------------|
| Overpromising unachievable KPI targets | High | Focus turnaround plan on operational actions and creative refreshes rather than guaranteed numbers. |
| Unapproved financial concessions proposed | Medium | Require account director approval on [PROPOSED_CONCESSIONS] placeholder input. |

**Overall risk rating:** HIGH — High commercial impact (contract retention); mandatory senior management review required..

---

## 🔄 Version History


### v1.0 — Initial unconstrained draft
**Date:** 3 August 2026
**Prompt:** Prompt: Write an email to save a client who is unhappy with ad results.
**Output:** Apologetic email without concrete tactical solutions or structured timelines.  
**Observed effect:** Client felt agency was unprepared and canceled contract regardless.
**Lesson learned:** Must provide a structured 30-day tactical roadmap rather than simple apologies.

---

### v1.1 — Tactical Roadmap Added
**Date:** 5 August 2026
**Change:** Added structured sections for Accountability, Root Cause, and 30-Day Plan.
**Output:** Solid structural proposal, but tone sounded defensive regarding ad platform costs.
**Observed effect:** Plan was better received, but client pushed back on agency accountability.
**Lesson learned:** Tone must balance complete accountability with confident strategic leadership.

---

### v1.2 — Commercial Concessions & Solution Focus ✅ Current
Date:** 7 August 2026
**Change:** Added Commercial Concession alignment and empathetic, solution-focused tone rules.
**Output:** Executive recovery pitch combining radical transparency, a 4-week roadmap, and clear agency commitment.
**Observed effect:** Account retention on red-flagged accounts improved by ~60% in agency pilot tests.
**Lesson learned:** Concrete 30-day roadmaps combined with no-risk agency concessions restore client confidence.

---

## 📊 A/B Test Results

**Test date:** 7 August 2026 | **Evaluators:** Sanzeena

| Criteria | v1.0 score | v1.2 score |
|----------|------------|------------|
| Clarity | 70/100 | 90/100 |
| Constraints | 40/100| 95/100 |
| Structure | 50/100 | 90/100 |
| Verifiability | 60/100 | 85/100 |
| Hallucination Risk | 80/100 | 90/100 |
| **Overall** | **62/100** | **89.5/100** |

---

## 🔗 Related Prompts

- **Previous in chain:** P09-kpi-performance-digest.md
- **Next in chain:** Contract Renewal & Scale Strategy
- **Parent section:** 04-reporting-relations README
