# Examples

A **fictional** worked example for the reporting pipeline — the *Smart Agriculture Data Initiative (SADI)*, a 3-year grant project. Nothing here is real; it exists to show the shape of a filled profile and a pipeline input.

| File | What it shows |
| :--- | :--- |
| [`project-profile.md`](project-profile.md) | A fully filled profile (§A objectives/activities + weights, §B indicators/MOV, §C output commitments, §D team→activity map) — copy `../project-profile.template.md` and fill it like this. |
| [`Weekly Report - 2026-03-13.md`](Weekly%20Report%20-%202026-03-13.md) | An example **weekly** report (organized by functional team) — the input `consolidate-monthly-report` re-maps onto the SADI Activities (A1–A8). |

## How the example flows through the pipeline

1. **Weekly** — the sample weekly is organized by team (Platform Engineering, Data Science, …).
2. **Monthly** — `consolidate-monthly-report` re-maps each bullet to a SADI Activity: the ingest connector → **A1**, the pest model → **A3**, the extension-worker training → **A5**, the MOU → **A7**, the privacy framework → **A8**, and procurement/onboarding → the **Project Management** section.
3. **Quarterly → Annual → Terminal** — roll up the monthly tag outputs, tally against the §C commitments (e.g. Partnerships 0/8, Publications x/3), pace-check time-boxed targets, and at terminal evaluate objective achievement (did the advisories actually improve farmer outcomes — outcome, not just "models built").
