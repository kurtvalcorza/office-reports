# office-reports

A small collection of **agent skills for institutional document drafting** — the kind of formal, evidence-based reports that government agencies, research organizations, and offices produce routinely. Each skill turns raw source material (transcripts, notes, invitations, programs) into a structured, copy-ready document, and flags gaps rather than inventing content.

Built to the [Agent Skills](https://agentskills.io) open standard — portable across any compatible AI tool (Claude, Cursor, Codex, Gemini, Kiro, and others).

## Skills

Two kinds: **single-document** generators (one source → one report) and a config-driven **multi-stage reporting pipeline** (weekly logs → period reports that roll up through one shared structure).

### Single-document skills

| Skill | What it does |
| :--- | :--- |
| [`official-travel-report`](official-travel-report/) | Synthesizes a folder of travel source materials (invitations, programs, notes, slides, articles) into a complete four-section Official Travel Report — Highlights/Major Decisions, Recommended Follow-Through Actions, Impressions/Observations, Linkages Established — with an optional S&T impact-categories layer and explicit `[NEEDS INPUT]` gap flags. |
| [`minutes-of-meeting`](minutes-of-meeting/) | Turns a transcript or facilitator notes into copy-ready Minutes of the Meeting: a standard metadata header, Roman-numeral sections I–VI (Call to Order → Adjournment), objective discussion clusters, explicit action items, and Prepared-by / Reviewed-by sign-offs. |

### Reporting pipeline (weekly → terminal)

A config-driven, multi-stage pipeline for **monitoring & evaluation (M&E) of funded or grant-based projects** — the kind with a logical framework (objectives, activities, indicators, committed outputs). It turns weekly activity logs into period reports that roll up through one shared structure:

```
weekly → monthly → quarterly → annual → terminal
```

| Component | Role |
| :--- | :--- |
| [`reporting-pipeline-core.md`](reporting-pipeline-core.md) | The shared mechanics every stage cites — pipeline, alignment-first principle, tag schema, roll-up rules, output template. Generic; you don't edit it. |
| [`project-profile.template.md`](project-profile.template.md) | The **only file you edit** — your objectives, activities, weights, indicators (OVI/MOV), output commitments, and team→activity map. |
| [`consolidate-weekly-report`](consolidate-weekly-report/) | Task-tracker export → weekly report organized by functional team (entry stage). |
| [`consolidate-monthly-report`](consolidate-monthly-report/) | 4–5 weeklies → Activity-mapped monthly report + indicator/MOV/output compliance tags (the transformation stage). |
| [`consolidate-quarterly-report`](consolidate-quarterly-report/) | 3 monthlies → cumulative-to-date tally + mandatory pace check. |
| [`consolidate-annual-report`](consolidate-annual-report/) | 4 quarterlies → yearly tally + Year-in-Review + weighted progress. |
| [`consolidate-terminal-report`](consolidate-terminal-report/) | the annuals → grand-total output closeout + outcomes/impact + objective-achievement evaluation. |

Mapping happens once (at the monthly stage); quarterly→terminal are pure roll-ups, and terminal adds the outcomes/evaluation layer. See [`examples/`](examples/) for a filled profile and a sample weekly.

## Design principles

All skills share the same discipline:

- **Evidence-only.** Write only what the source material supports. Never infer, assume, or pad with plausible-sounding filler.
- **Flag, don't guess.** Anything missing or unconfirmable becomes a `[NEEDS INPUT: …]` placeholder, consolidated into a gaps list for the writer to resolve before submission.
- **Formal, third-person, institutional register.** Suitable for official records.
- **Copy-ready output.** Structured to drop straight into an agency or office template.

## Installation

Each skill is a self-contained directory with a `SKILL.md` (agent instructions) and `README.md` (human docs). To use one, copy its directory into your agent's skills location — e.g.:

- **Claude Code / Agent Skills tools:** `.agent/skills/`, `.claude/skills/`, or wherever your tool discovers skills
- **Cursor / Codex / Gemini / Kiro:** the corresponding `skills/` directory for that tool

The agent picks up the skill from its `SKILL.md` frontmatter (`name` + `description`).

For the **reporting pipeline**, also copy `reporting-pipeline-core.md` and `project-profile.template.md` alongside the five `consolidate-*-report` skill directories, then copy the template to `project-profile.md` and fill it in. The skills resolve the core and your profile by name from the same location.

## Customizing for your organization

These are deliberately generic. To adapt them to a specific office:

- **Travel report** — the eight S&T impact categories in Section 1 are a common public-sector / research-org framing. Trim to the categories your organization reports against, or swap in your own outcome framework.
- **Minutes** — the I–VI section structure and the "Division-in-Charge" / "Reference No." header fields are conventional but adjustable. Rename the convening-unit field and section labels to match your house format.
- **Reporting pipeline** — adapt it entirely through `project-profile.md` (objectives, activities, weights, indicators, output commitments, team→activity map). The core mechanics and the five skills are fixed; your profile is the only thing you edit. The OVI/MOV and output-commitment framing follows the logframe/M&E convention — swap in your funder's own indicator and deliverable schema.

## License

MIT — see [LICENSE](LICENSE). Built with AI.