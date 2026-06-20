# Project Profile — EXAMPLE (Smart Agriculture Data Initiative)

> A fully worked, **fictional** example profile for a 3-year grant project, to show how `project-profile.template.md` is filled in. Nothing here is real — adapt the structure to your own logframe.

```yaml
project:
  name: "Smart Agriculture Data Initiative"
  short: "SADI"
  funder: "National Agricultural Research Council (Grant 2025-114)"
  start: "2025-03"
  years: 3
```

---

## §A — Objectives & Activities (the structure spine)

| Objective | Activity code | Activity name (verbatim from workplan) | Weight | Phase/Year |
|---|---|---|---|---|
| **O1** Field data platform | A1 | Establishing the agricultural data platform | 18 | Y1 |
| | A2 | Scaling the platform to regional cooperatives | 8 | Y2 |
| **O2** Predictive models | A3 | Developing crop, pest, and weather models | 22 | Y1 |
| | A4 | Piloting model-driven advisories with farmers | 16 | Y2 |
| **O3** Capacity building | A5 | Training farmers and extension workers | 10 | Y1 |
| | A6 | Continued training & farmer learning networks | 6 | Y3 |
| **O4** Partnerships | A7 | Forging institutional & cooperative partnerships | 8 | Y1 |
| **O5** Responsible data | A8 | Establishing data-governance and privacy safeguards | 12 | Y2 |

*Weights sum to 100. Phases: Y1 = 2025–26, Y2 = 2026–27, Y3 = 2027–28.*

---

## §B — Indicators & Means of Verification

| Activity | Indicator ID | Indicator (what proves progress) | Acceptable MOV (evidence) |
|---|---|---|---|
| A1 | A1-IND1 | Platform deployed with ingest + dashboard for ≥1 region | system record — deployment logs |
| A2 | A2-IND1 | ≥N cooperatives onboarded to the platform | registry — onboarding records |
| A3 | A3-IND1 | Models trained and validated (crop/pest/weather) | system record — model repo, validation reports |
| A4 | A4-IND1 | Advisory pilots run with farmer cohorts | documentary — pilot reports |
| A5 | A5-IND1 | Training events delivered with pre/post assessment | registry — attendance + pre/post-tests |
| A6 | A6-IND1 | Farmer learning networks active | registry — network membership |
| A7 | A7-IND1 | Partnership agreements signed | signed agreement |
| A8 | A8-IND1 | Data-governance framework adopted | published output — framework document |

**MOV vocabulary:** documentary · system record · signed agreement · registry · published output · filing record · financial record.

---

## §C — Output commitments

| Output category | Annual target | Grand-total target | Manual? | Notes |
|---|---|---|---|---|
| Publications | ~1/yr | ≥3 | no | peer-reviewed papers |
| Datasets & Models | — | ≥4 | no | open datasets + trained models |
| Farmers/workers trained | per cohort | ≥400 | **yes** | headcount tracked manually outside the report |
| Partnerships | progress | 8 | no | signed cooperative/agency agreements |
| Policy | — | ≥1 | no | adopted data-governance framework |
| Platform | presence | ingest · dashboard · advisory API | no | product presence |

---

## §D — Team → Activity map & routing

| Functional team / work type | Default → Activity |
|---|---|
| Platform Engineering | A1 (A2 when scaling) |
| Data Science | A3 |
| Field & Extension | A4 / A5 |
| Partnerships | A7 |
| Comms & Outreach | stakeholder engagement (reported under A7) |
| Data Governance | A8 |
| **Admin / HR / procurement / logistics / project reporting** | **Project Management** (standalone, outside the spine) |

**Active team list:** Platform Engineering · Data Science · Field & Extension · Partnerships · Comms & Outreach · Data Governance · Project Management.

**Exclusions:** personal speaking-engagement decks unrelated to project deliverables.

**Cross-project handling:** items belonging to a different grant surface under "Misaligned / For Review," excluded from SADI totals.
