# Product Requirements Document
## TE-to-Course Alignment Accelerator

**Team:** Ranjani Indrajith (PM) · Jamila Gibson (Instructional Design)
**Program:** SLA Dual Literacy (*Emerger Juntos*), Grades K–5

*Reconstructed for portfolio purposes from a delivered Innovation Week project.*

---

## Problem Statement

The SLA digital course build requires mapping every lesson's assets, materials, and component sequences from the Spanish-language Teacher Edition (TE) to the Open Learning course structure.

This process was entirely manual: a team member opened the TE for each lesson, read through complex Spanish-language instructional content, identified relevant data, and manually entered it into a spreadsheet.

The system intended to bridge TE and Open Learning — the CAT tracker — was cloned from the ELA program and did not accurately reflect SLA-unique components (biliteracy building, cross-linguistic connections, dictation printables, non-transferable skills). This forced the team to fact-check the CAT and re-extract directly from the TE every time, with no reusable output. The team was operating without infrastructure that reflected the actual content model.

## Goal

Replace manual, per-lesson TE extraction with an AI-assisted workflow that produces a verified, QC-ready spreadsheet output — reducing a 60-hour-per-unit process to under 15 hours, without sacrificing accuracy.

## Success Metrics

| Metric | Baseline | Result |
|---|---|---|
| Time per lesson | ~60 min | ~10–15 min |
| Time per unit (15 lessons) | ~60 hours | Under 15 hours (75–85% reduction) |
| Program-wide savings (conservative estimate) | — | ~630 hours / ~$18,900 |
| Internal validation | — | 12/12, Innovation Week Opportunity Scorecard |

**Cost model:**
15 lessons/unit × ~1 hr ≈ 15 hrs/unit → 10 units/grade ≈ 150 hrs/grade → 6 grades (K–5) ≈ 900 hrs/program at a $30/hr blended labor rate (~$27,000 baseline cost). At a conservative 70% time reduction, the program saves ~630 hours (~$18,900).

## Users & Stakeholders

| Group | Impact |
|---|---|
| Instructional Design | Bore the direct extraction burden |
| Course Build | Couldn't trust the CAT tracker; independently re-verified alignment |
| CAD | Received inconsistently formatted verification requests |
| Teachers (end users) | Risked missing or misaligned materials in the digital course |
| Program Leadership | Couldn't systematically implement new instructional decisions without a reliable alignment system |

## Requirements

**Functional**
- Ingest Spanish-language TE content via a document-ingestion layer feeding an LLM
- Extract structured, lesson-level data: assets, materials, component sequences
- Produce spreadsheet-ready output (CSV/TSV, or direct paste into Excel/Smartsheet)
- Capture SLA-unique components missed by the ELA-cloned CAT tracker (biliteracy building, cross-linguistic connections, dictation printables, non-transferable skills)
- Keep human review in the loop: the workflow shifts the human role from *creating* extractions to *reviewing and correcting* AI-generated drafts
- Validate prompt templates against sample lessons until output accuracy exceeds 85% before scaling

**Non-Functional**
- Deliverable within a 9-day unit-alignment deadline
- Operable at pilot stage using existing LLM access, with no new tooling procurement

## Out of Scope (v1)

- A custom-built application (e.g., a dedicated tool with a purpose-built UI for TE ingestion, template mapping, and diff views) — deferred to an optional future phase, contingent on usage patterns and team feedback
- Fixing the underlying CAT tracker — sequenced after the extraction workflow, using its verified output as the audit source

## Rollout Plan

| Phase | Timeline | Action |
|---|---|---|
| Template Design | Week 1 | Finalize extraction spreadsheet template — columns, dropdowns, field definitions |
| Prompt Engineering | Week 1 | Develop and test prompt templates on 5–10 sample lessons; iterate to >85% accuracy |
| Pilot Unit | Week 1–2 | Run AI-assisted extraction on current unit; full human review; CAD verification; measure time savings |
| Measure & Refine | Week 2 | Document accuracy rate, time per lesson, error types; refine prompts |
| Scale | Week 3+ | Apply to remaining units; train additional team members on review workflow |
| Infrastructure Fix | Week 3–5 | Use verified output to audit and correct the CAT tracker; establish SLA-specific fork and adjustment protocol |
| Long-Term Tool Evaluation | Month 2+ | Assess whether a purpose-built application is warranted based on usage and feedback |

## Results

- 75–85% reduction in per-unit alignment time (60 hrs → under 15 hrs)
- ~$18,900 projected savings across the program lifecycle
- 12/12 Innovation Week Opportunity Scorecard — rated "Ready" across all four dimensions (Problem Clarity, Scalable KPI, Reusable Pattern, Urgency)
