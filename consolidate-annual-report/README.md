# Consolidate Annual Report

Rolls a year's **four quarterly reports** into an **Annual Accomplishment Report** with a tally against the **year's targets** (plus cumulative), a **Year-in-Review**, and weighted progress if the profile defines activity weights.

```
weekly → monthly → quarterly → ANNUAL (this skill) → terminal
```

A **pure roll-up** — aggregate the quarterlies into year-scale milestones, widen the period, tally against the yearly horizon. Phase-aware if the profile maps activities to project years.

## Inputs / Outputs
- **In:** 4 × `YYYY-QN_Compliance-Tags_<Project>.md` + quarterly narratives + `project-profile.md`.
- **Out:** `YYYY_Annual-Report_<Project>.md` (+ Year-in-Review) + `YYYY_Compliance-Tags_<Project>.md`.

## Key rules
- Roll up, don't re-analyze; tags carried up unchanged.
- Tally against the yearly target **and** show cumulative-to-date.
- Bullets are year-scale milestones; Year-in-Review with weighted progress.

## Related
- **Core:** `../reporting-pipeline-core.md` · **Profile:** `../project-profile.md`
- **Upstream:** `consolidate-quarterly-report` · **Downstream:** `consolidate-terminal-report`
