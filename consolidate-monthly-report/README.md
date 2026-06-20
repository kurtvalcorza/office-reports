# Consolidate Monthly Report

Rolls a month of weekly reports into a **Monthly Accomplishment Report mapped to your workplan Activities** (Objectives → Activities), with an optional **compliance-tag output** (Indicator / MOV / Output) that feeds the quarterly stage.

## Where it sits

```
weekly → MONTHLY (this skill) → quarterly → annual → terminal
```

This is the **transformation stage** — weekly reports are organized by **team**, and this is where that gets re-mapped to **workplan Activities**. Everything above monthly is a roll-up of the same shape.

## Inputs / Outputs
- **In:** 4–5 weekly reports + `project-profile.md`.
- **Out:** `YYYY-MM_Monthly-Report_<Project>.md` (narrative) and, optionally, `YYYY-MM_Compliance-Tags_<Project>.md` (the quarterly bridge).

## Usage
```
"Consolidate the monthly report for <YYYY-MM> from the weekly reports."
```
Add *"and generate the compliance tags"* for the second output.

## Key rules
- Map work→activity, never team→activity (alignment-first).
- No force-fitting — misaligned items are surfaced.
- Overhead → standalone Project Management section.
- Two outputs stay separate; team sub-heads retained for provenance.

## Related
- **Core:** `../reporting-pipeline-core.md` · **Profile:** `../project-profile.md`
- **Upstream:** `consolidate-weekly-report` · **Downstream:** `consolidate-quarterly-report`
