# P09 · Executive KPI Performance Digest

**Section:** 04 — Reporting & Client Relations
**Workflow step:** Step 1 of 2
**Current version:** v1.2
**Status:** ✅ Tested
**Last updated:** August 2026
---

## 📌 Prompt Text (v1.2 — current)

> Copy this exactly into your AI tool. Replace all `[PLACEHOLDERS]` before running.

```
[ROLE]
You are a Lead Account Director and Performance Analyst at a digital marketing agency.

[ACTION]
Transform raw monthly campaign metrics into an executive-ready Monthly KPI Performance Digest for client leadership.

[CONTEXT]
Client Name: [CLIENT_NAME]
Reporting Period: [REPORTING_PERIOD]
Raw Performance Data:
"""
[RAW_PERFORMANCE_METRICS]
"""

Brand Strategy Context (P01):
"""
[P01_BRAND_GUIDE_OUTPUT]
"""

[CONSTRAINTS]
1. Use clear Markdown sections and bold executive summary callouts.
2. Structure data using a Markdown Table for MoM (Month-over-Month) comparisons.
3. Keep tone objective, authoritative, and consultative.
4. Maximum length: 350 words.

[OUTPUT FORMAT]
- Executive Summary (3 bullet points highlighting main wins and takeaways)
- Key Metrics Table (Metric | Previous Month | Current Month | MoM Change % | Target Status)
- Strategic Analysis & Key Insights (What worked vs. areas for optimization)
- Next Month Action Plan (3 priority initiatives)

```

**Placeholders to fill:**

| Placeholder | Source | Example |
|-------------|--------|---------|
| `[CLIENT_NAME]` | Account Record | "Roasted Roost Coffee" |
| `[REPORTING_PERIOD]` | Reporting Cycle | "July 2026" |
| `[RAW_PERFORMANCE_METRICS]` | CSV export from Meta/Google Ads dashboard | Ad Spend: $10,000, New Subscribers: 520, CPA: $19.23, ROAS: 3.4x. |
| `[P01_BRAND_GUIDE_OUTPUT]` | Output from P01 | Paste P01 markdown output |
---

## 🏢 Intended Workflow or Task

Synthesizes raw ad platform reporting data into a polished executive digest for monthly client meetings.

- **Trigger:** Monthly billing cycle ends; analytics data exported.
- **Actor:** Account Director reviews digest before sending to client.
- **Timing:** 1st business day of the month.
- **Next step:** Shared with client stakeholders; feeds into P10 if KPIs miss targets.

```
Raw Metrics Export → [THIS PROMPT RUNS] → Executive Digest → Shared with Client

```

---

## ❗ Problem Being Solved

Account managers spend 3 to 5 hours per client manually building reporting slides and spreadsheets. Raw data dumps confuse executive clients who only care about business outcomes (CPA, CAC, ROI).

**Pain points addressed:**
- High manual effort spent reformatting CSV metrics into client reports (~4 hrs per client).
- Confusing technical data dumps that obscure business ROI.
- Inconsistent monthly reporting quality across account managers.

---

## ⚡ Automation Potential

**Level:** High

| Dimension | Assessment |
|-----------|------------|
| Repetitiveness | High — executed monthly for every agency client. |
| Data availability | High — raw metrics exported directly from Google/Meta dashboards. |
| Human judgment needed | Medium — Account Director spot-checks data accuracy. |
| Integration possibility | High — can connect via Zapier/Make to automatically fetch Looker Studio data. |
| Estimated time saving | ~80% — reduces report generation from 4 hours to 25 minutes. |

**Human-in-the-loop role:** Account Director verifies that financial calculations match dashboard source truths before client distribution.

---

## ⚠️ Risks and Limitations


| Risk | Level | Mitigation |
|------|-------|------------|
| Model miscalculates percentage change math | High | Required explicit calculation reporting in structured table format. |
| Model glosses over missed targets | Medium | Enforced "Target Status" column in markdown table to highlight underperformance.|

**Overall risk rating:** Medium — Client-facing financial data requires strict human verification prior to delivery.

---

## 🔄 Version History

### v1.0 — Initial unconstrained draft
**Date:** 2 August 2026
**Prompt:** Summarize these performance numbers for my client: [DATA].
**Output:** Paragraph-dense text without tables, missing Month-over-Month comparison context. 
**Observed effect:** Clients asked follow-up questions because percentage changes were omitted. 
**Lesson learned:** Must mandate Markdown tables and MoM percentage calculations.

---

### v1.1 — Table & MoM Metrics Added
**Date:** 5 August 2026
**Change:** Enforced Markdown table structure with MoM Change columns.  
**Output:** Clean financial table layout, but analysis lacked strategic recommendations.
**Observed effect:** Report looked like an accounting audit rather than strategic marketing guidance.
**Lesson learned:** Needs dedicated strategic insight and next month action plan sections.

---

### v1.2 — Executive Summary & Action Plan Integration ✅ Current
**Date:** 7 August 2026 
**Change:** Added 350-word cap, executive bulleted summary, and 3 priority next steps.
**Output:** Executive-ready monthly report balancing data tables with strategic direction.
**Observed effect:** Reduced monthly reporting creation time from 4 hours to 25 minutes per client.
**Lesson learned:** Combining structured data tables with brief strategic summaries provides maximum executive value.

---

## 📊 A/B Test Results

**Test date:** 7 August 2026 | **Evaluators:** Sanzeena

| Criteria | v1.0 score | v1.2 score |
|----------|------------|------------|
| Clarity | 85/100 | 90/100 |
| Constraints | 70/100| 95/100 |
| Structure | 75/100 | 90/100 |
| Verifiability | 90/100 | 85/100 |
| Hallucination Risk | 95/100 | 90/100 |
| **Overall** | **82.25/100** | **89.5/100** |

---

## 🔗 Related Prompts

- **Previous in chain:** P06-ad-variant-generator.md
- **Next in chain:** P10-churn-risk-turnaround-pitch.md
- **Parent section:** 04-reporting-relations README
