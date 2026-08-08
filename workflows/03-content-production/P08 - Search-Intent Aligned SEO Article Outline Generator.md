# P08 · Search-Intent Aligned SEO Article Outline Generator

**Section:** 03 — Content Production
**Workflow step:** Step 2 of 2
**Current version:** v1.2
**Status:** ✅ Tested
**Last updated:** August 2026

---

## 📌 Prompt Text (v1.1 — current)

> Copy this exactly into your AI tool. Replace all `[PLACEHOLDERS]` before running.

```
[ROLE]
You are an Executive SEO Strategist and Content Architect.

[ACTION]
Create a search-intent aligned SEO Article Outline based on a target keyword and content calendar topic.

[CONTEXT]
Client Name: [CLIENT_NAME]
Target Keyword: [PRIMARY_KEYWORD]
Blog Topic (from P05): [P05_BLOG_TOPIC]
Brand Voice (P01):
"""
[P01_BRAND_GUIDE_OUTPUT]
"""

[CONSTRAINTS]
1. Heading Hierarchy: Must use strict Markdown headers (H1, H2, H3).
2. Search Intent Alignment: Include a dedicated "Key Takeaways / Quick Answer" section right under H1 for Google Featured Snippets.
3. On-Page SEO Elements: Provide Meta Title (under 60 chars) and Meta Description (under 155 chars).
4. Tone: Informative, authoritative, approachable, zero fluff.

[OUTPUT FORMAT]
- SEO Metadata (Title Tag, Meta Description, Target URL Slug)
- Quick Answer Box (50-word snippet optimization)
- Article Structure (H1, H2s, H3s with bulleted talking points per section)
- Internal Linking Suggestions (2 strategic link placements)

```

**Placeholders to fill:**

| Placeholder | Source | Example |
|-------------|--------|---------|
| `[CLIENT_NAME]` | Account Record | "Roasted Roost Coffee" |
| `[PRIMARY_KEYWORD]` | SEO Keyword Research Tool | "fresh coffee bean subscription Australia" |
| `[P05_BLOG_TOPIC]` | Output from P05 | "Why Supermarket Coffee is Stale (And How Fresh Roasting Works)" |
| `[P01_BRAND_GUIDE_OUTPUT]` | Output from P01 | Paste P01 markdown output |

---

## 🏢 Intended Workflow or Task

Creates structured, search-intent aligned blog outlines ready for SEO copywriters to draft without keyword stuffing.

- **Trigger:** Content Calendar (P05) blog topic assigned.
- **Actor:** Content Editor / SEO Specialist reviews structure.
- **Timing:** Day 3 of monthly production cycle.
- **Next step:** Handed to SEO Writer for full drafting.

```
P05 Blog Topic + Keyword → [THIS PROMPT RUNS] → Structured SEO Outline → SEO Copywriter
```

---

## ❗ Problem Being Solved

SEO copywriters often write articles without clear heading hierarchies (H2/H3) or fail to answer search intent directly, leading to poor Google rankings and missed Featured Snippets.

**Pain points addressed:**
- Unstructured articles failing to rank for target search intent.
- Meta titles and descriptions exceeding character limits in Google SERPs.
- High manual outline prep time (~2 hours per article outline).

---

## ⚡ Automation Potential

**Level:** High

| Dimension | Assessment |
|-----------|------------|
| Repetitiveness | High — required for every organic SEO article drafted. |
| Data availability | High — uses target keyword and P05 topic inputs. |
| Human judgment needed | Low — editor verifies keyword intent match. |
| Integration possibility | High — maps directly into SEO management software (SurferSEO/Clearscope). |
| Estimated time saving | ~85% — reduces outline creation from 2 hours to 15 minutes. |

**Human-in-the-loop role:** SEO Specialist confirms that target keyword search intent is accurately addressed in the Featured Snippet section.

---

## ⚠️ Risks and Limitations


| Risk | Level | Mitigation |
|------|-------|------------|
| Meta titles cut off in SERPs | MEDIUM | Enforced strict <60 char constraint for titles and <155 for descriptions. |
| Keyword stuffing in headings | Low | Explicitly instructed model to focus on natural search intent hierarchy. |

**Overall risk rating:** LOW — Standard content architecture template.

---

## 🔄 Version History


### v1.0 — Initial unconstrained draft
**Date:** 3 August 2026
**Prompt:** Prompt: Write an outline for a blog post about coffee subscriptions.
**Output:** Generic list of topics without H2/H3 header tags, metadata, or snippet targets.  
**Observed effect:** SEO writers drafted unstructured essays that failed to target Google search intent, requiring extensive structural editing.
**Lesson learned:** Must mandate strict H1/H2/H3 structures and SEO metadata.

---

### v1.1 — Heading Tags & Metadata Added
**Date:** 5 August 2026
**Change:** Enforced H2/H3 markdown headings and character limits for Meta Title/Description.
**Output:** Better SEO structure, but missed the "Featured Snippet" opportunity on Google.
**Observed effect:** Outlines were good, but missed out on quick zero-click ranking positions on Google SERPs.
**Lesson learned:** Needs a dedicated "Quick Answer / Featured Snippet" section under H1.

---

### v1.2 — Snippet Optimization & Internal Links ✅ Current
**Date:** 7 August 2026
**Change:** Added a mandatory 50-word Quick Answer Box for Featured Snippets and internal link suggestions.
**Output:** Production-ready SEO outline optimized for Google ranking factors.
**Observed effect:** Reduced outline creation time from 2 hours to 15 minutes while improving article structure quality.
**Lesson learned:** Featured Snippet blocks significantly improve organic ranking potential.

---

## 📊 A/B Test Results

**Test date:** 7 August 2026 | **Evaluators:** Sanzeena

| Criteria | v1.0 score | v1.2 score |
|----------|------------|------------|
| Clarity | 80/100 | 90/100 |
| Constraints | 40/100| 95/100 |
| Structure | 50/100 | 90/100 |
| Verifiability | 30/100 | 85/100 |
| Hallucination Risk | 40/100 | 90/100 |
| **Overall** | **56/100** | **89.5/100** |

---

## 🔗 Related Prompts

- **Previous in chain:** P05-multi-channel-calendar.md
- **Next in chain:** Article Draft Copywriting Execution
- **Parent section:** 03-content-production README
