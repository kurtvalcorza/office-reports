---
name: consolidate-monthly-report
description: Consolidate a month of weekly accomplishment reports into a workplan-aligned Monthly Accomplishment Report organized by the project's Objectives and Activities, plus an optional indicator/MOV/output compliance-tag output that feeds quarterly reporting. The transformation stage where team-organized weekly work is re-mapped to workplan Activities. Reads project-profile.md.
---

# Consolidate Monthly Report

## Purpose
Transform 4–5 weekly reports into a **Monthly Accomplishment Report mapped to the project's workplan Activities** (Objectives → Activities, from `project-profile.md` §A) — and, as a **separate optional step**, a **compliance-tag output** (Indicator / MOV / Output) that becomes the quarterly report's evidence base.

This is the **transformation stage** of the pipeline (weekly → **monthly** → quarterly → annual → terminal): weekly *functional-team* output is re-mapped to *workplan Activities*. Everything above monthly is roll-up of the same shape.

## Read first
- **`reporting-pipeline-core.md`** — §2 alignment-first, §3 spine, §4 tag schema, §5 team→activity map, §7 template.
- **`project-profile.md`** — §A Activities, §B indicators/MOV, §C output commitments, §D team→activity map.

This skill governs the **monthly workflow and the two outputs**; it does not redefine structure.

---

## Inputs
- 4–5 `Weekly Report - YYYY-MM-DD.md` for the target month (team-organized).
- `project-profile.md` (the spine, indicators, outputs, mapping).

## Outputs
- `YYYY-MM_Monthly-Report_<Project>.md` — narrative (primary).
- `YYYY-MM_Compliance-Tags_<Project>.md` — tag output (optional separate step; the quarterly bridge).

---

## Non-Negotiable Rules
1. **Activity spine** — the narrative follows the profile's Objectives → Activities exactly (core §3). Do not invent categories.
2. **Alignment-first, team-agnostic** — map the *work* to the Activity, not the team name to an Activity (core §2). Every bullet passes the alignment test.
3. **No force-fitting** — bullets advancing no Activity go to **"Misaligned / For Review"**.
4. **Project Management section for overhead** — admin / HR / procurement / logistics / project reporting / coordination go in a standalone **Project Management** section parallel to the objectives (core §5), not under any Activity. Apply profile §D exclusions (drop excluded work types entirely).
5. **De-duplicate across weeks** — collapse recurring/ongoing items into single monthly bullets.
6. **Cross-cut sparingly** — duplicate only when a bullet genuinely advances a second Activity; annotate `— cross-cut: also supports <code>`.
7. **Preserve phrasing** — house style; light edits; `(completed)`/`(ongoing)` on every bullet.
8. **Two outputs are separate** — the narrative never embeds tags inline; tagging is its own output.
9. **Trainings delivered, not received** — capacity-building Activities are for training the project *conducts*; staff attending external training routes to the Activity their role serves.
10. **Retain team sub-heads** — within each Activity, group bullets under their originating weekly **team** as a bolded sub-head (core §7). The Activity is the spine; the team is the sub-section. Placement is still alignment-first — the team is for provenance, never the basis for which Activity a bullet lands in.

---

## Workflow

### Phase 1 — Initialize
Confirm the month; locate the weeklies; load the core + profile.

### Phase 2 — Ingest weeklies
Read each weekly; extract accomplishment bullets **with their team** and status. Build `{text, status, source_week(s), origin_team}`.

### Phase 3 — De-duplicate & merge
Collapse repeats across weeks (core §6.2): "continued/ongoing" persisters → one bullet; merge sub-tasks. Preserve proper nouns and progress detail.

### Phase 4 — Map to Activities (alignment-first)
For each bullet, apply core §2 + profile §D:
1. Which Activity does the *work* advance? → assign it.
2. Second Activity advanced? → cross-cut.
3. Overhead? → **Project Management** section.
4. Advances nothing? → **Misaligned / For Review**. Record `activity` (+ optional `cross_cut`) and keep the origin team.

### Phase 5 — Build the narrative
Use core §7: `## [Objective]` → `### [code] — [Activity]` → **team sub-head** → bullets. Empty Activities get `_(No accomplishments reported this period)_`. Add the standalone **Project Management** section, then **Misaligned / For Review** if any.

### Phase 6 — Compliance tagging (separate output, optional)
For each narrative bullet add the tag triple (core §4): the **Indicator** it evidences (profile §B), its **MOV**, and any **Output** category + qty (profile §C). Emit `YYYY-MM_Compliance-Tags_<Project>.md`: the tag table + an **output tally** block. For manually-tracked outputs (profile §C), record the event/indicator only — do not compute the figure.

### Phase 7 — Quality checks
- [ ] Every weekly bullet mapped OR in Misaligned.
- [ ] Alignment gate re-run (work-type, not team name).
- [ ] Duplicates collapsed; cross-cuts annotated.
- [ ] Overhead in Project Management; exclusions dropped.
- [ ] Headings match the profile spine verbatim.
- [ ] (If Phase 6) every output bullet has an Indicator/MOV; tally arithmetic checks.

---

## Outputs
1. **Narrative** `YYYY-MM_Monthly-Report_<Project>.md` — core §7 template, Activity spine.
2. **Compliance tags** `YYYY-MM_Compliance-Tags_<Project>.md` — Indicator/MOV/Output table + tally. The unit the **quarterly** stage consumes.

## Anti-Patterns
**AVOID:** mapping by team name; force-fitting; embedding tags inline; inventing activities not in the profile; redefining structure here instead of citing the core.
**DO:** map work→activity; route overhead to Project Management; surface misaligned items; keep the two outputs separate; cite the core + profile.

---

## Version History
### v1.0
- Generic monthly/transformation stage. Re-keyed to the profile's Objectives→Activities; structure/tags/mapping cited from the core; narrative + optional compliance-tag output.
