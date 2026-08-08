# 📂 03 — Content Production Workflow

**Business function:** Organic Content & SEO Production
**Trigger:** Multi-channel calendar (P05) approved by Content Lead
**Prompts in this section:** P07, P08

---

## Section Purpose

This section automates the transition from calendar topics to fully realized production assets (short-form video scripts and SEO article outlines). Creating engaging short-form scripts and search-intent aligned blog structures manually consumes 6–8 hours per content pack. This workflow standardizes visual directions and SEO hierarchies, cutting drafting time down to under 30 minutes.

## Chain Diagram

```
Complaint received
      │
      ▼
P07 · Short-Form Video Script          → Video Creator / UGC Editor
      │
      ▼ 
P08 · SEO Article Outline     	 → SEO Copywriter
```

## Human-in-the-Loop Points

| Step | Human action required |
|------|-----------------------|
| P07 output | Creative Producer reviews visual cues and pacing before filming/editing |
| P08 output | Content Editor verifies keyword placement and heading hierarchy before full drafting |

## Prompts

| File | Prompt | Status |
|------|--------|--------|
| [P07-video-script-builder.md](P07-video-script-builder.md) | Short-form video script builder | ✅ Tested — v1.2 |
| [P08-seo-blog-outline.md](P08-seo-blog-outline.md) | Search-intent aligned SEO blog outline | ✅ Tested — v1.2 |