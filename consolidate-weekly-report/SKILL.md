---
name: consolidate-weekly-report
description: Consolidate a task-tracker export (Microsoft Planner, Jira, Asana, Trello, or a spreadsheet/task list) into a polished weekly accomplishment report organized by functional team. Use to turn raw weekly task data into a professional narrative — the entry stage of the accomplishment-reporting pipeline. Reads project-profile.md for the team list.
---

# Consolidate Weekly Report

## Purpose
Transform a week's raw task data into a polished, professional **weekly accomplishment report** organized by **functional team / workstream**. This is the **entry stage** of the reporting pipeline (weekly → monthly → quarterly → annual → terminal) — the only stage organized by team rather than by workplan Activity.

## Read first
- **`reporting-pipeline-core.md`** — the shared mechanics (§1 pipeline, §7 template conventions).
- **`project-profile.md`** §D — your functional-team list (the section headings this report uses).

This skill governs only the **weekly workflow**; the pipeline structure lives in the core and your profile.

---

## Inputs
- A **task-tracker export** for the target week — Microsoft Planner (`.xlsx`/`.csv`), Jira (`.csv`), Asana/Trello/ClickUp export, or any task list with: task name, status/completion date, and a team/bucket field. Optional: checklist items, labels, notes.
- Optional supplemental sources (meeting notes, chat updates) — used only to clarify or add, never as the starting point when a structured export exists.

## Output
- `Weekly Report - YYYY-MM-DD.md` (end-of-week date), organized by the profile's functional teams.

---

## Workflow

### Phase 1 — Ingest
1. Identify the **primary structured export**; treat notes/screenshots/chat as supplemental.
2. Isolate the useful columns: task name, completion date/status, team/bucket, and (if present) checklist items, labels, notes. Ignore the rest to avoid bloat.

### Phase 2 — Temporal filter
- **Include:** tasks completed within the target week → `(completed)`.
- **Include:** tasks with no completion date (in progress) → `(ongoing)`.
- **Exclude:** tasks completed in a prior week (historical).

### Phase 3 — Group & synthesize
1. Group tasks by their **functional team** → map to the report headings in `project-profile.md` §D.
2. Within each team, merge related tasks + checklist items into **compound bullets**:
   > "Advanced [main task], including [sub-task A], [sub-task B], and [sub-task C]. (completed)"
3. Use strong lead verbs (Advanced, Continued, Completed, Conducted, Delivered). Every bullet ends with `(completed)` or `(ongoing)`.
4. Reconcile supplemental sources only after the structured-export draft exists.

### Phase 4 — Generate & sanitize
1. Emit Markdown with one `##` heading per team (profile §D order).
2. Professional, third-person voice; no "I/we".
3. **Sanitize:** replace internal server names/IPs with generic descriptors; remove local paths.
4. Save `Weekly Report - YYYY-MM-DD.md`.

---

## Non-Negotiable Rules
1. **Structured export is the source of truth** — never start synthesis from screenshots/chat if an export exists; never let supplements override export status/dates.
2. **Status suffix on every bullet** — `(completed)` or `(ongoing)`.
3. **Group by team** (profile §D); preserve the team taxonomy — don't merge sections.
4. **Compound bullets, not task dumps** — merge related micro-tasks; preserve meaningful progress detail from checklists/notes.
5. **Sanitize** sensitive data before finalizing; confirm before overwriting an existing report.

---

## Quality Checks
- [ ] Every bullet ends with a status.
- [ ] Only tasks within the week (or blank-date "ongoing") are included.
- [ ] Headings match the profile's team list.
- [ ] No internal IPs/paths/credentials remain.
- [ ] Structured export remained the primary basis; supplements reconciled after.

## Handoff
This weekly feeds **`consolidate-monthly-report`**, which re-maps the team-organized bullets to workplan Activities. Generate 4–5 weeklies per month for a clean monthly roll-up.

---

## Version History
### v1.0
- Generic weekly stage of the reporting pipeline. Tool-agnostic ingest; organizes by the profile's functional teams; cites `reporting-pipeline-core.md`.
