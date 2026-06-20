# Consolidate Weekly Report

Turns a **task-tracker export** (Microsoft Planner, Jira, Asana, Trello, or a spreadsheet) into a polished **weekly accomplishment report** organized by functional team.

## Where it sits

```
WEEKLY (this skill) → monthly → quarterly → annual → terminal
```

This is the **entry stage** of the [reporting pipeline](../reporting-pipeline-core.md) — the only stage organized by team. The monthly stage re-maps these bullets to your workplan Activities.

## Inputs / Outputs
- **In:** a week's task export (task name, status/completion date, team/bucket; optional checklist/labels/notes).
- **Out:** `Weekly Report - YYYY-MM-DD.md`, grouped by the functional teams in `project-profile.md` §D.

## Usage
```
"Consolidate the weekly report from <export file> for the week of <dates>."
```

## Key rules
- Structured export is the source of truth (notes/chat are supplemental).
- Compound bullets, not task dumps; every bullet ends `(completed)`/`(ongoing)`.
- Group by the profile's functional teams; sanitize internal data.

## Related
- **Core:** `../reporting-pipeline-core.md` · **Profile:** `../project-profile.md` (§D teams)
- **Downstream:** `consolidate-monthly-report`
