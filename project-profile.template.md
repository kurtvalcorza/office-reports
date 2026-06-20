# Project Profile — TEMPLATE

> Copy this file to **`project-profile.md`** and fill in §A–§D. This is the **only** file you edit to adapt the reporting pipeline to your project. The shared core (`reporting-pipeline-core.md`) and the five `consolidate-*-report` skills read this profile for everything project-specific; you never edit the mechanics.
>
> A fully worked example is in [`examples/`](examples/).

```yaml
project:
  name: "<Project name>"              # appears in every report title
  short: "<Acronym>"                  # optional short tag
  funder: "<Funding agency / grant>"  # optional
  start: "YYYY-MM"                     # project start (for Year mapping)
  years: 3                            # number of project years (phases)
```

---

## §A — Objectives & Activities (the structure spine)

List your **objectives** and, under each, the **activities** from your logframe/workplan. Use a stable short **code** per activity (e.g. `A1`, `A2`, …) — the pipeline uses codes everywhere. **Weights** (optional) should sum to 100 across all activities; they drive weighted-progress reporting. **Phase/Year** (optional) maps activities to project years.

| Objective | Activity code | Activity name (verbatim from workplan) | Weight | Phase/Year |
|---|---|---|---|---|
| **O1** <short title> | A1 | <full activity name> | 10 | Y1 |
| | A2 | <full activity name> | 15 | Y1 |
| **O2** <short title> | A3 | <full activity name> | 20 | Y2 |
| … | … | … | … | … |

> Rules: codes are unique and stable; activity names are verbatim (reports reproduce them as headings); weights are optional but if present must sum to 100.

---

## §B — Indicators & Means of Verification (the audit checklist)

For each activity, list its **Objectively Verifiable Indicator(s)** with a stable ID (`<activity>-IND<n>`), and the **Means of Verification (MOV)** — the evidence that proves it. This is your audit checklist; the compliance-tag outputs reference these IDs.

| Activity | Indicator ID | Indicator (what proves progress) | Acceptable MOV (evidence) |
|---|---|---|---|
| A1 | A1-IND1 | <observable, verifiable indicator> | documentary / system record / … |
| A2 | A2-IND1 | <indicator> | signed agreement / registry / … |
| … | … | … | … |

**MOV vocabulary** (use these labels in tags): `documentary` · `system record` · `signed agreement` · `registry` · `published output` · `filing record` · `financial record`. Add your own if needed.

---

## §C — Output commitments (the deliverables you promised)

The output categories your project commits to, with **annual** and/or **grand-total** targets. These are tallied cumulatively; time-boxed ones (e.g. "≥N per year") get a mandatory pace check at the quarterly stage. Mark any category whose count is **tracked manually outside the report** (e.g. training headcounts) — the pipeline records the events/indicators but does not compute those figures.

| Output category | Annual target | Grand-total target | Manual? | Notes |
|---|---|---|---|---|
| <e.g. Publications> | ~1/yr | ≥3 | no | journal/conference outputs |
| <e.g. Patents/IP> | ≥2/yr | ≥6 | no | filings, not prior-art review |
| <e.g. People trained> | per cohort | ≥600 | **yes** | headcount tracked manually |
| <e.g. Partnerships> | progress | 10 | no | signed agreements |
| <e.g. Policy outputs> | — | ≥1 | no | created framework, not input |
| <e.g. Products> | presence | <list> | no | datasets / models / platform |

> Adapt these output categories to your funder's deliverable schedule — e.g. publications, intellectual property, products/datasets, people trained, partnerships, policy outputs.

---

## §D — Team → Activity map & routing

Map each **functional team / workstream** (the section names your weekly reports use) to its default Activity. The mapping is a **hint** — the alignment-first rule (core §2) still governs; classify by what the work advances.

| Functional team / work type | Default → Activity |
|---|---|
| <e.g. Engineering team A> | A2 |
| <e.g. Research team> | A3 |
| <e.g. Training/curriculum> | A4 (capacity building) |
| <e.g. Partnerships/external> | A5 |
| <e.g. Comms/outreach/events> | A6 (stakeholder engagement) |
| **Admin / HR / procurement / logistics / project reporting** | **Project Management** (standalone section, outside the spine) |

**Active team list:** <list the functional team names your weekly reports currently use>.

**Exclusions** (work types to drop entirely, not place or flag): <e.g. personal speaking-engagement decks unrelated to project deliverables>. *Do not list cross-project work here* — that is handled separately below so it **surfaces for review** rather than being silently dropped.

**Cross-project handling:** items belonging to a *different* project surface under **"Misaligned / For Review"** (not Exclusions), and are excluded from this project's totals there.

---

## Notes
- Keep this profile in version control alongside your reports.
- When your workplan changes (new activity, revised target), update the profile — not the skills.
- The five skills + `reporting-pipeline-core.md` never need editing for a new project; only this file does.
