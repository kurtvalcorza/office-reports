---
name: consolidate-annual-report
description: Roll up four quarterly reports into an annual workplan-aligned Accomplishment Report plus a tally against the year's targets, with a Year-in-Review synthesis and (if weights are defined) weighted progress. Pure roll-up of the quarterly stage — no re-mapping. Reads project-profile.md.
---

# Consolidate Annual Report

## Purpose
Aggregate a year's **four quarterly reports** into an **Annual Accomplishment Report** on the workplan-Activity spine, with a tally **against the year's targets** (plus cumulative-to-date) and a short **Year-in-Review** synthesis. If the profile defines activity weights, report **weighted progress**.

This is the **annual stage** (weekly → monthly → quarterly → **annual** → terminal). A **pure roll-up** — aggregate the quarterlies, de-duplicate into year-scale milestones, widen the period, tally against the yearly horizon.

## Read first
- **`reporting-pipeline-core.md`** — §6 roll-up, §7 template, §8 horizons.
- **`project-profile.md`** — §A spine + weights + phases, §B indicators, §C output commitments.

---

## Inputs
- **4 quarterly compliance-tag outputs** `YYYY-QN_Compliance-Tags_<Project>.md`.
- The 4 quarterly narratives. *Flag any missing/partial quarter.*

## Outputs
- `YYYY_Annual-Report_<Project>.md` — narrative + Year-in-Review.
- `YYYY_Compliance-Tags_<Project>.md` — yearly + cumulative tally.

---

## Non-Negotiable Rules
1. **Activity spine** (core §3 / profile §A).
2. **Roll-up, not re-analysis** — carry quarterly tags up unchanged; widen `period` to `YYYY` (core §6.3).
3. **De-duplicate across the year** — collapse multi-quarter persisters into **year-scale milestones** (core §6.2).
4. **Re-run the alignment gate** (core §6.5).
5. **Retain team sub-heads** + standalone **Project Management** section.
6. **Tally against the YEARLY target** (profile §C) and show the **cumulative project-to-date** figure: `(this year / yearly target)` and `(cumulative / grand total)`.
7. **Phase-aware** — if the profile maps activities to years/phases (§A), foreground the activities in scope for that year; out-of-phase activities with no work get the no-work line.
8. **Year-in-Review required** — objectives advanced, weighted progress (if weights defined), outputs closed vs behind pace, carry-over.
9. **Two outputs separate;** manually-tracked outputs record events only.

---

## Workflow
1. **Initialize** — confirm the year + phase; locate 4 narratives + tag outputs; flag gaps.
2. **Aggregate** by Activity (core §6.1); keep the Q4 cumulative figures.
3. **De-duplicate to year-scale milestones** (core §6.2); carry tags up; widen `period`.
4. **Build the narrative** — core §7 at year scale; out-of-phase/no-work Activities get the no-work line; add Project Management + Misaligned.
5. **Yearly + cumulative tally** (profile §C) — both columns; emit the tag output.
6. **Year-in-Review** — objectives advanced; **weighted progress** (sum the §A weights of activities with substantive movement, state the assumption); outputs closed/behind; carry-over.
7. **QA** — 4 quarters represented (or partial noted); tags unchanged; milestones (not tasks); both tallies present; weighted progress computed if weights exist.

## Anti-Patterns
**AVOID:** re-mapping/re-tagging; month-scale bullets in a year report; a year-only tally with no cumulative; omitting the Year-in-Review.
**DO:** roll up unchanged; collapse to milestones; show yearly + cumulative; compute weighted progress; cite core + profile.

---

## Version History
### v1.0
- Generic annual stage — pure roll-up of 4 quarterlies; Year-in-Review + yearly/cumulative tally; phase- and weight-aware.
