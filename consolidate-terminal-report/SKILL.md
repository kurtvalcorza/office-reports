---
name: consolidate-terminal-report
description: Roll up a project's annual reports into the terminal (project-end) Accomplishment Report — grand-total output closeout against commitments, an outcomes/impact layer, and a terminal evaluation framed on objective achievement (outcome, not just output). Evidence-only; flags unverifiable claims. Reads project-profile.md.
---

# Consolidate Terminal Report

## Purpose
Aggregate the project's **annual reports** into the **Terminal (project-end) Accomplishment Report** on the workplan-Activity spine, and add the two things only this stage carries:
1. a **grand-total output closeout** against the project's commitments (profile §C), and
2. an **outcomes / impact layer + terminal evaluation** judged on **objective achievement** (did the objectives deliver their intended results?), not merely activity completion.

This is the **terminal stage** (weekly → monthly → quarterly → annual → **terminal**). The accomplishment spine is a pure roll-up of the annuals; the **evaluation and outcomes framing is new here**.

## Read first
- **`reporting-pipeline-core.md`** — §3 spine + weights, §6 roll-up (esp. §6.6 outcomes), §7 template, §8 grand-total horizons.
- **`project-profile.md`** — §A spine + weights, §B indicators/MOV, §C output commitments (the commitments to close against).

---

## Inputs
- The project's annual compliance-tag outputs `YYYY_Compliance-Tags_<Project>.md` (one per year).
- The annual narratives (incl. Year-in-Review sections). *Flag any missing/partial year in-text — a terminal report with gaps must say so.*

## Output
- `Terminal-Report_<Project>.md` — single document: accomplishment narrative → grand-total closeout → outcomes/impact → terminal evaluation → Gaps & Flags.

---

## Non-Negotiable Rules
1. **Activity spine** for the accomplishment layer (core §3 / profile §A).
2. **Roll-up, not re-analysis** — carry annual tags up unchanged into grand totals (core §6.3).
3. **De-duplicate to project-scale milestones** — the narrative is the arc across years, one bullet per major milestone per Activity.
4. **Grand-total closeout mandatory** — every output commitment (profile §C) reported `achieved / committed` against the grand-total horizon, with a **met / partially met / not met** verdict and the gap.
4b. **Outcome ≠ output** — the evaluation judges whether objectives achieved their **intended results** (outcomes/impact), separate from whether activities/outputs were completed. Do not conflate "we built it" with "it delivered the intended benefit."
5. **Evidence-only on impact** — outcome/impact claims must trace to MOV evidence; where asserted but unverifiable, flag `[NEEDS INPUT: outcome evidence for …]` rather than claiming it. **No fabricated metrics.**
6. **Weighted objective achievement** — if the profile defines weights (§A), express overall completion using them; state the assumption (weights = share of effort, not task completion).
7. **Surface unmet commitments honestly** — partial/not-met outputs and unachieved objectives are reported plainly with reasons, not buried or omitted.
8. **Retain the standalone Project Management section;** apply profile §D exclusions.
9. **Manually-tracked outputs** (profile §C) — list events/indicators and reference the manual source; do not compute the figure.

---

## Workflow
1. **Initialize** — confirm the project span; locate every annual narrative + tag output; flag missing years; load the spine + commitments (profile §A/§C).
2. **Aggregate to grand totals** by Activity and by output category (core §6.1); verify figures reconcile across years.
3. **De-duplicate to project-scale milestones** (core §6.2).
4. **Build the accomplishment narrative** — core §7 at project scale; Activities never reached get an explicit `_(Not undertaken — see evaluation)_`; add Project Management + Misaligned.
5. **Grand-total closeout** — every output `achieved / committed` with a met/partial/not-met verdict + gap.
6. **Outcomes / impact + terminal evaluation** *(the stage-defining step)*:
   - Per-objective: intended result (profile) vs **evidenced outcome** (cite MOV; flag unverifiable).
   - Weighted achievement (profile §A weights), assumption stated.
   - Terminal verdict per objective: achieved / substantially achieved / partially achieved / not achieved.
   - Lessons & sustainability.
7. **QA** — years represented (gaps flagged); tags unchanged; figures reconcile; closeout complete with verdicts; outcomes layer present and **outcome≠output respected**; every impact claim traces to MOV or is flagged; unmet commitments surfaced; no fabricated metrics.

## Outputs (document order)
1. Accomplishment narrative (Activity spine) + Project Management
2. Grand-total output closeout (met / partial / not met)
3. Outcomes / impact (per objective)
4. Terminal evaluation (weighted achievement + per-objective verdict + lessons/sustainability)
5. Gaps & Flags (consolidated `[NEEDS INPUT]` items)

## Anti-Patterns
**AVOID:** conflating outputs with outcomes; fabricating impact metrics; burying unmet commitments; silently omitting activities never reached; re-mapping/re-tagging.
**DO:** roll up unchanged; close every output against its grand total with a verdict; evidence or flag every impact claim; report misses plainly.

---

## Version History
### v1.0
- Generic terminal stage — grand-total closeout + outcomes/impact + objective-achievement evaluation (outcome≠output, evidence-only). Completes the five-stage pipeline.
