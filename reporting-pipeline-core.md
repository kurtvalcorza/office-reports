# Reporting Pipeline — Shared Core

The single source of truth for the **accomplishment-reporting pipeline**: a staged roll-up that turns weekly activity logs into period reports (weekly → monthly → quarterly → annual → terminal), all sharing one structure. Every consolidation skill in this collection cites this file so the **structure, tags, and roll-up logic live in one place**, not copied per skill.

This pipeline is built for **monitoring & evaluation (M&E) of funded or grant-based projects** — the kind with a logical framework (logframe): objectives, activities, indicators, and committed outputs. If your project has a workplan with measurable targets, this fits.

> [!important] Generic mechanics vs. your project's instantiation
> This file is **generic and portable**. Everything project-specific — your objectives, activities, weights, indicator vocabulary, output commitments, and team→activity mapping — lives in **`project-profile.md`** (copy it from `project-profile.template.md` and fill it in). The skills read your profile; you never edit the mechanics. See [`project-profile.template.md`](project-profile.template.md).

---

## 1 — The pipeline

Five stages, each aggregating the one below. **Every stage above weekly shares one shape** — an Activity-structured narrative + indicator/output tags — differing only by **time window**, **aggregation depth**, and the **target horizon** the output tally is measured against.

| Stage | Period | Consumes | Organized by | Tally horizon |
|---|---|---|---|---|
| **Weekly** | week | task-tracker export | functional teams *(input layer)* | — |
| **Monthly** | month | 4–5 weeklies | **Activity narrative + tags** | (establishes tags) |
| **Quarterly** | 3 months | 3 monthlies | **Activity narrative + tags** | cumulative-to-date |
| **Annual** | year | 4 quarterlies | **Activity narrative + tags** | yearly targets |
| **Terminal** | whole project | the annuals | **Activity narrative + output grand totals + outcomes** | grand-total commitments |

**The transformation point is the monthly stage** — weekly is organized by team/function; monthly re-maps the work to **workplan Activities** and applies the tag schema. Everything above monthly is roll-up of the same shape.

---

## 2 — Core principle: alignment-first, team/name-agnostic

Non-negotiable across the pipeline:

- **Map the WORK to the ACTIVITY, not the team/tool/component name to the activity.** A bullet's originating team is a *hint*, not a verdict — classify by what the work advances.
- **Every bullet must pass an alignment test** against the workplan Activities before placement. If it advances no Activity, it goes to **"Misaligned / For Review"**, never force-fit.
- **Cross-cut** only when a bullet genuinely advances a second Activity; annotate `— cross-cut: also supports <code>`.
- **Preserve phrasing** (house style; light edits only). Status suffix `(completed)` / `(ongoing)` on every bullet.

---

## 3 — Structure spine (from your project profile)

The spine is your project's **Objectives → Activities**, with optional weights and phases. **Do not hardcode it here** — it comes from `project-profile.md` §A (Objectives & Activities). The skills read that table and build every report's section structure from it, verbatim.

If your profile assigns **weights** to activities (summing to 100), the pipeline uses them for weighted-progress reporting at the annual and terminal stages. Weights are optional; without them, progress is reported qualitatively.

---

## 4 — Per-accomplishment tag schema

Every accomplishment carries this record. The **narrative** uses `text/status/activity/cross_cut`; the **separate compliance/tag output** adds `indicator/MOV/output`.

| Field | Values | Used in |
|---|---|---|
| `text` | the bullet (house style, preserved) | narrative + tags |
| `status` | `completed` · `ongoing` | narrative + tags |
| `activity` | primary Activity code (from profile §A) | narrative + tags |
| `cross_cut` | secondary Activity code(s), optional | narrative + tags |
| `indicator` | which Objectively Verifiable Indicator(s) it evidences (profile §B) | tags only |
| `MOV` | Means of Verification / evidence type (profile §B) | tags only |
| `output` | output-commitment category + qty, if it's an output (profile §C) | tags only |
| `period` | reporting window (e.g., `2026-03`, `2026-Q1`, `Y1`) | all |
| `source` | originating report/file | all |

The tag triple — **activity code + indicator/MOV + output** — is what makes every higher stage a roll-up rather than re-analysis. **Indicator and MOV vocabularies are defined in your profile** (§B); common MOV types: documentary, system record, signed agreement, registry, published output, filing record, financial record.

---

## 5 — Team → Activity mapping (weekly → monthly)

Functional teams/workstreams are a **hint, not a verdict** — apply the §2 work-type test. The default mapping for your project's teams lives in **`project-profile.md` §D** (Team→Activity map). General routing rules (generic):

- **Overhead** — admin / HR / procurement / logistics / project reporting / coordination → a standalone **Project Management** section, *outside* the Activity spine (most logframes have no project-management Activity; report overhead separately, parallel to the objectives).
- **Coordination that advances a partnership/collaboration Activity** → that Activity.
- **Outreach / comms / events / stakeholder engagement** → the relevant engagement Activity.
- **Publications / disseminated outputs** → the Activity the work belongs to, tagged with the publication output category.
- **Staff attending external training for their own development** → the Activity their role serves (NOT a capacity-building Activity — those are for training the project *delivers*).
- **Excluded items** — define in your profile (§D) any work types to drop entirely (e.g., personal speaking-engagement decks unrelated to project deliverables).
- **Anything that advances no Activity → "Misaligned / For Review".**

---

## 6 — Roll-up rules (stage N+1 from stage N)

1. **Aggregate** all child-period accomplishments by Activity.
2. **De-duplicate across the period** — collapse recurring "ongoing" items into one representative bullet; merge near-identical bullets; preserve proper nouns and meaningful progress detail.
3. **Carry the tags up** — the activity/indicator/MOV/output tags propagate unchanged; only the `period` field widens.
4. **Tally outputs & indicator evidence** cumulatively against the stage's **target horizon** (§8). Show `(achieved / target)`.
5. **Re-run the alignment gate** — every rolled-up bullet still passes the work-type test under its Activity.
6. **Terminal only:** add an **outcomes / impact** layer and **terminal-evaluation** framing (objective achievement, not just activity completion).

---

## 7 — Uniform output template

Same shape at monthly / quarterly / annual / terminal. **The Activity is the section spine; the weekly functional teams are retained as bolded sub-heads *within* each Activity** — so the report is organized by workplan Activity while preserving the originating team provenance. A team that splits across Activities appears under each (with only its relevant bullets).

```markdown
# [Period] Accomplishment Report — [Project]

## [Objective 1 — short title]

### [A1] — [Activity name from profile §A]
**[Team / workstream]**
- <accomplishment>. (completed)
**[Another team]**
- <accomplishment>. (ongoing) — cross-cut: also supports [A2]

### [A2] — [Activity name]
- _(No accomplishments reported this period)_

## [Objective 2 — …]
...

## Project Management
**[team]**
- <admin / HR / procurement / logistics / coordination bullet>. (completed)

## Misaligned / For Review
- <bullet> — could not align to an Activity; candidate: <Ax>. Needs clarification.
```

**Project Management** is a standalone section *parallel to the objectives* (not an Activity) — project overhead that no Activity covers. Activities with no work get `_(No accomplishments reported this period)_` and no sub-heads. Order teams within an Activity by volume of work.

**Separate compliance/tag output** (the bridge to higher stages), one row per tagged accomplishment:

```markdown
| Activity | Accomplishment | Indicator | MOV (evidence) | Output |
|---|---|---|---|---|
| A4 | Delivered an [X] training for [audience] | A4-IND2 | registry — attendance + certificates | People (event) |
```

…followed by the **output tally** block (categories and targets from profile §C). For any output your profile flags as *manually tracked* (e.g. headcounts kept outside the report), list the event/indicator only — do not compute the figure.

---

## 8 — Output commitments & target horizons (from your profile)

Your project's **output commitments** (the "deliverables you promised the funder") and the horizon each stage tallies against come from **`project-profile.md` §C**. The pattern:

- **Quarterly** tallies cumulative-to-date (pace check — flag any time-boxed commitment that is behind, e.g. "≥N filings/year").
- **Annual** tallies against the yearly target.
- **Terminal** tallies against the grand-total commitments + objective achievement.

Each output category carries a target (annual and/or grand-total). The pace check at the quarterly stage is mandatory for any **time-boxed** commitment.

---

## 9 — Stage interface summary

| Stage | Input | Output(s) |
|---|---|---|
| Weekly | task-tracker export | `Weekly Report - YYYY-MM-DD.md` (functional teams) |
| Monthly | 4–5 weeklies + profile | narrative `YYYY-MM` report (Activities) **+** separate tag/compliance output |
| Quarterly | 3 monthly tag outputs | narrative `YYYY-QN` report + cumulative tag tally + pace check |
| Annual | 4 quarterlies | narrative `YYYY` report + Year-in-Review + yearly tally |
| Terminal | the annuals | full project report + grand-total tally + outcomes/impact + evaluation |

---

## Adapting this to your project

1. Copy `project-profile.template.md` → `project-profile.md` and fill in §A–§D.
2. Drop the five `consolidate-*-report` skill directories into your agent's skills location.
3. Run the weekly skill on a task-tracker export; then monthly; then roll up. The skills cite this core and your profile for everything project-specific.

The mechanics (this file) and the skills are fixed; **your profile is the only thing you edit.**
