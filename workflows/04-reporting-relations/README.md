# 📂 04 — Reporting & Client Relations Workflow

**Business function:** Client Retention & Performance Reporting
**Trigger:** End of monthly reporting cycle OR client churn risk flagged by account team
**Prompts in this section:** P09, P10

---

## Section Purpose

This section automates executive-level campaign reporting and client retention workflows. Synthesizing complex multi-channel analytics into client-facing digests and building structured recovery strategies for underperforming accounts typically takes account directors 8–10 hours per client. This prompt suite standardizes executive performance communication and turnaround planning, reducing preparation time to under 45 minutes.

## Chain Diagram

```
Complaint received
      │
      ▼
P09 · KPI Performance Digest          → Account Director Review
      │
      ▼ 
P10 · Churn Risk Turnaround Pitch	 → Executive Presentation to Client
```

## Human-in-the-Loop Points

| Step | Human action required |
|------|-----------------------|
| P09 output | Account Director verifies metrics against ad platform dashboards before sending digest |
| P10 output | Head of Client Success approves turnaround scope and budget adjustments before client presentation |

## Prompts

| File | Prompt | Status |
|------|--------|--------|
| [P09-kpi-performance-digest.md](P09-kpi-performance-digest.md) | Executive KPI Performance Digest | ✅ Tested — v1.2 |
| [P10-churn-risk-turnaround-pitch.md](P10-churn-risk-turnaround-pitch.md) | Churn Risk Turnaround Pitch | ✅ Tested — v1.2 |