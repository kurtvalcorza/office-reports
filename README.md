# office-reports

A small collection of **agent skills for institutional document drafting** — the kind of formal, evidence-based reports that government agencies, research organizations, and offices produce routinely. Each skill turns raw source material (transcripts, notes, invitations, programs) into a structured, copy-ready document, and flags gaps rather than inventing content.

Built to the [Agent Skills](https://agentskills.io) open standard — portable across any compatible AI tool (Claude, Cursor, Codex, Gemini, Kiro, and others).

## Skills

| Skill | What it does |
| :--- | :--- |
| [`official-travel-report`](official-travel-report/) | Synthesizes a folder of travel source materials (invitations, programs, notes, slides, articles) into a complete four-section Official Travel Report — Highlights/Major Decisions, Recommended Follow-Through Actions, Impressions/Observations, Linkages Established — with an optional S&T impact-categories layer and explicit `[NEEDS INPUT]` gap flags. |
| [`minutes-of-meeting`](minutes-of-meeting/) | Turns a transcript or facilitator notes into copy-ready Minutes of the Meeting: a standard metadata header, Roman-numeral sections I–VI (Call to Order → Adjournment), objective discussion clusters, explicit action items, and Prepared-by / Reviewed-by sign-offs. |

## Design principles

Both skills share the same discipline:

- **Evidence-only.** Write only what the source material supports. Never infer, assume, or pad with plausible-sounding filler.
- **Flag, don't guess.** Anything missing or unconfirmable becomes a `[NEEDS INPUT: …]` placeholder, consolidated into a gaps list for the writer to resolve before submission.
- **Formal, third-person, institutional register.** Suitable for official records.
- **Copy-ready output.** Structured to drop straight into an agency or office template.

## Installation

Each skill is a self-contained directory with a `SKILL.md` (agent instructions) and `README.md` (human docs). To use one, copy its directory into your agent's skills location — e.g.:

- **Claude Code / Agent Skills tools:** `.agent/skills/`, `.claude/skills/`, or wherever your tool discovers skills
- **Cursor / Codex / Gemini / Kiro:** the corresponding `skills/` directory for that tool

The agent picks up the skill from its `SKILL.md` frontmatter (`name` + `description`).

## Customizing for your organization

These are deliberately generic. To adapt them to a specific office:

- **Travel report** — the eight S&T impact categories in Section 1 are a common public-sector / research-org framing. Trim to the categories your organization reports against, or swap in your own outcome framework.
- **Minutes** — the I–VI section structure and the "Division-in-Charge" / "Reference No." header fields are conventional but adjustable. Rename the convening-unit field and section labels to match your house format.

## License

MIT — see [LICENSE](LICENSE). Built with AI.