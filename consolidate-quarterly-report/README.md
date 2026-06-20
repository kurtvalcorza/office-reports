# Consolidate Quarterly Report

Rolls a quarter's **three monthly reports** into a **Quarterly Accomplishment Report** with a **cumulative-to-date** tally and a **pace check** on time-boxed commitments.

```
weekly → monthly → QUARTERLY (this skill) → annual → terminal
```

A **pure roll-up** — mapping happened at the monthly stage. Aggregate the 3 monthly tag outputs, de-duplicate across the quarter, widen the period, re-tally cumulatively. No re-mapping.

## Inputs / Outputs
- **In:** 3 × `YYYY-MM_Compliance-Tags_<Project>.md` + the monthly narratives + `project-profile.md`.
- **Out:** `YYYY-QN_Quarterly-Report_<Project>.md` + `YYYY-QN_Compliance-Tags_<Project>.md` (cumulative + pace check).

## Key rules
- Roll up, don't re-analyze; carry tags up unchanged.
- Cumulative-to-date tally, not quarter-only.
- Pace check is mandatory for time-boxed commitments.

## Related
- **Core:** `../reporting-pipeline-core.md` · **Profile:** `../project-profile.md`
- **Upstream:** `consolidate-monthly-report` · **Downstream:** `consolidate-annual-report`
