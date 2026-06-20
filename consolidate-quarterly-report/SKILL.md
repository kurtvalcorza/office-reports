---
name: consolidate-quarterly-report
description: Roll up three monthly compliance-tag outputs into a quarterly workplan-aligned Accomplishment Report plus a cumulative-to-date indicator/MOV/output tally with a mandatory pace check on time-boxed commitments. Pure roll-up of the monthly stage — no re-mapping. Reads project-profile.md.
---

# Consolidate Quarterly Report

## Purpose
Aggregate a quarter's **three monthly reports** into a **Quarterly Accomplishment Report** on the workplan-Activity spine, with a **cumulative-to-date** indicator/output tally and a mandatory **pace check** on time-boxed commitments (e.g. "≥N filings/year").

This is the **quarterly stage** of the pipeline (weekly → monthly → **quarterly** → annual → terminal). The work was already mapped to Activities at the monthly stage; quarterly is a **pure roll-up** — aggregate, de-duplicate, widen the period, re-tally. No re-mapping.

## Read first
- **`reporting-pipeline-core.md`** — §6 roll-up rules, §7 template, §8 output horizons.
- **`project-profile.md`** — §A spine, §B indicators, §C output commitments (targets + manual flags).

---

## Inputs
- **3 monthly compliance-tag outputs** `YYYY-MM_Compliance-Tags_<Project>.md` (the roll-up unit).
- The 3 monthly narratives (phrasing/provenance).
- *If a month's tag output is missing:* generate it via `consolidate-monthly-report` Phase 6 first, or flag the partial quarter.

## Outputs
- `YYYY-QN_Quarterly-Report_<Project>.md` — narrative.
- `YYYY-QN_Compliance-Tags_<Project>.md` — cumulative-to-date tally + pace check.

---

## Non-Negotiable Rules
1. **Activity spine** (core §3 / profile §A) — no new categories.
2. **Roll-up, not re-analysis** — carry the monthly `activity / indicator / MOV / output` tags **up unchanged**; only widen `period` to `YYYY-QN` (core §6.3). Do **not** re-map (settled at monthly).
3. **De-duplicate across the quarter** — collapse multi-month "ongoing" persisters into one bullet (core §6.2).
4. **Re-run the alignment gate** (core §6.5); surface misfits to Misaligned.
5. **Retain team sub-heads** and the standalone **Project Management** section (core §5/§7).
6. **Cumulative-to-date tally** — tally outputs/indicators cumulatively across the project to date (core §8), `(achieved / target)`.
7. **Pace check is mandatory** — for every time-boxed commitment (profile §C), state on-track / behind / ahead with the arithmetic.
8. **Two outputs separate;** manually-tracked outputs record events only.

---

## Workflow
1. **Initialize** — confirm the quarter + months; locate 3 narratives + 3 tag outputs; flag gaps.
2. **Aggregate** — gather tagged accomplishments by Activity (core §6.1).
3. **De-duplicate across the quarter** (core §6.2); carry tags up; widen `period`.
4. **Build the narrative** — core §7 template; empty Activities get the no-work line; add Project Management + Misaligned.
5. **Cumulative tally + pace check** — tally vs each commitment's horizon (profile §C); for time-boxed ones state on-track/behind/ahead. Emit the tag output.
6. **QA** — all 3 months represented (or partial noted); tags unchanged; duplicates collapsed; tally arithmetic; pace check present for every time-boxed output.

## Anti-Patterns
**AVOID:** re-mapping/re-tagging (monthly's job); re-deriving tags from narratives instead of rolling up the tag outputs; a quarter-only tally (must be cumulative); skipping the pace check.
**DO:** roll up unchanged; de-dup; tally cumulatively; run the pace check; cite core + profile.

---

## Version History
### v1.0
- Generic quarterly stage — pure roll-up of 3 monthly tag outputs; cumulative tally + mandatory pace check.
