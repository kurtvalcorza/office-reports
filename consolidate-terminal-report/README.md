# Consolidate Terminal Report

Rolls a project's **annual reports** into the **Terminal (project-end) Accomplishment Report** — the Activity accomplishment arc, a **grand-total output closeout** against commitments, an **outcomes/impact layer**, and a **terminal evaluation** judged on objective achievement.

```
weekly → monthly → quarterly → annual → TERMINAL (this skill)
```

The accomplishment spine is a **pure roll-up** of the annuals. What's **new here** is the evaluation: closing outputs against grand-total commitments, an outcomes/impact layer, and a verdict on whether each objective achieved its intended result — **outcome, not just output**.

## Inputs / Outputs
- **In:** the project's `YYYY_Compliance-Tags_<Project>.md` (per year) + annual narratives + `project-profile.md` (the commitments closed against). *Missing years are flagged in-text.*
- **Out:** `Terminal-Report_<Project>.md` — narrative → grand-total closeout → outcomes/impact → terminal evaluation → Gaps & Flags.

## Key rules
- Roll up, don't re-analyze; annual tags carried up unchanged.
- **Outcome ≠ output** — judge whether objectives delivered their intended results.
- Evidence-only on impact; flag unverifiable claims `[NEEDS INPUT]`; no fabricated metrics.
- Report unmet commitments honestly.

## Related
- **Core:** `../reporting-pipeline-core.md` · **Profile:** `../project-profile.md`
- **Upstream:** `consolidate-annual-report`
