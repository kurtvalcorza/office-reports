---
name: official-travel-report
description: Synthesize source documents from a folder into a completed Official Travel Report. Use when a user points to a folder containing travel-related source materials (invitations, programs, notes, slides, articles, etc.) and needs the four main report sections written. Produces structured, evidence-based content with explicit gap flags for anything that cannot be confirmed from sources.
---

# Official Travel Report Writing Skill

This skill guides an agent in reading and synthesizing multiple source documents from a designated folder into the four required sections of an Official Travel Report. The agent acts as a careful synthesizer — never an inventor. Every claim in the report must be traceable to a source document.

This format follows the standard government/institutional Official Travel Report convention: a four-section structure (Highlights/Major Decisions, Recommended Follow-Through Actions, Impressions/Observations, Linkages Established) used widely across public-sector and research organizations.

---

## Core Principle: Evidence-Only Writing

**This is an official institutional document. The following rules are non-negotiable:**

- Write ONLY what is supported by the source documents.
- Do NOT infer, assume, or fill gaps with plausible-sounding content.
- When information is missing or unclear, insert a `[NEEDS INPUT: <description of what is missing>]` placeholder.
- At the end of the report draft, produce a consolidated **Gaps & Flags** list summarizing every placeholder inserted.
- When in doubt, flag it — do not guess.

---

## Step 1: Ingest All Source Documents

When the user points to a folder, use `file-search` to discover all files, then use `file-read` to read every file before writing anything. Source documents may include any combination of:

- Invitation letters or official event correspondence
- Official program of activities / agenda / schedule
- Event briefers or concept notes
- Presentation or slide decks
- Personal notes or trip reports from the traveler
- News articles or press releases about the event
- Social media posts or official event pages
- Calling cards or contact information collected during the trip
- Photos with captions (if available)

**For each file read, note:**
1. What type of document it is
2. What dates, sessions, speakers, or topics it covers
3. Any contact information or linkages mentioned

After reading all files, do a brief internal inventory:
- What days of the trip are covered?
- Which sessions or activities are documented?
- Are there gaps in the day-by-day coverage?
- Are S&T impact areas clearly evidenced, or only implied?
- Are any contacts/linkages documented with sufficient detail?

Only then proceed to drafting.

---

## Step 2: Draft the Header Information

Before the four sections, confirm or flag the following header fields:

```
Activity Title  :  [From invitation or program — exact official name]
Date            :  [From invitation or program — inclusive travel dates]
Venue           :  [From invitation or program — full venue name and address]
```

If any of these cannot be confirmed from the sources, insert `[NEEDS INPUT: ...]`.

---

## Step 3: Draft Section 1 — Highlights/Major Decisions

This is the longest and most substantive section. It has three layers:

### Layer A: Event Overview (2–4 paragraphs)

Write a narrative introduction covering:
- What the event was (conference, summit, standards meeting, workshop, etc.)
- Who organized it and who the key organizers or co-organizers were
- Where and when it was held
- The primary purpose, theme, or objectives of the event
- The significance or context of the event (why it matters globally or regionally)
- The organization's role or reason for participation (e.g., paper presentation, delegation, standards body membership)
- If applicable: the specific project or mandate that funded/motivated the travel

Base this entirely on the source documents. Use formal, third-person government/institutional report language.

### Layer B: Day-by-Day Chronological Account

After the overview, narrate what happened each day of the event. Use the following heading format for each day:

```
Day [N] – [Full Date] – [Optional: Theme or Title of the Day if available]
```

For each day, write a narrative paragraph (or multiple paragraphs for dense days) covering:
- Opening ceremonies, keynotes, or plenary sessions (speaker names, titles, affiliations, and key messages)
- Parallel sessions, workshops, or breakouts attended (topics and key takeaways)
- Any presentations made by the organization's representatives (title of paper/presentation, key points)
- Notable discussions, debates, or decisions made
- Networking events or bilateral meetings if documented

**Important notes for this layer:**
- Only include sessions that are evidenced in the source documents (program + notes/articles/slides).
- If the traveler attended only some sessions of a multi-track event, write only about those attended.
- If a day is documented in the program but has no notes or other coverage, insert: `[NEEDS INPUT: No session notes found for this day. Please provide details of sessions attended.]`
- Do not pad or invent session content from the program alone — the program tells you what was scheduled, not what actually happened or what was learned.

### Layer C: Science & Technology (S&T) Impact Categories (the "So What")

After the day-by-day account, synthesize the impact of the trip using the applicable categories below. **Do not force all eight categories** — only include those where the source documents provide clear evidence.

For each applicable category, write 1–2 paragraphs synthesizing the relevant insights, technologies, or outcomes from the trip.

**The eight categories (use only applicable ones):**

1. **Knowledge and Technologies Diffused**
   Evidence: knowledge shared with the home scientific or professional community; technologies or best practices encountered that can be adopted locally.

2. **New Knowledge and Technologies Generated**
   Evidence: new findings, innovations, or research outputs produced or presented by the organization during the trip.

3. **S&T Human Resources Developed**
   Evidence: training received, skills built, exposure to new methodologies or technical domains.

4. **Quality S&T Services Provided**
   Evidence: services rendered by the organization's representatives to other participants, organizations, or the delegation.

5. **Conducive S&T Policy Environment Created**
   Evidence: participation in policy discussions, standards development, governance frameworks, or regulatory dialogues.

6. **Growth of Innovative and Knowledge-based SMEs**
   Evidence: exposure to industry innovations, startup ecosystems, or commercial applications relevant to local SMEs.

7. **R&D Capacity Enhanced**
   Evidence: research collaborations initiated or deepened, access to datasets, tools, or methodologies, exposure to R&D infrastructure.

8. **Public S&T Awareness Improved**
   Evidence: outreach activities, public-facing presentations, or media engagements that promote S&T awareness.

If a category is not supported by the sources, omit it entirely — do not write a vague placeholder paragraph to fill it.

---

## Step 4: Draft Section 2 — Recommended Follow-Through Actions

Use `file-read` to re-check source documents for actionable items if needed.

Organize under two sub-headings:

**Follow-up actions/activities**
Specific next steps the traveler or organization should take. Examples: follow up with a contact met, submit a report to a standards body, apply for a fellowship, propose a joint project, disseminate standards to local stakeholders, organize a workshop.

**Local application of technologies learned**
How technologies, methodologies, or frameworks encountered during the trip can be adopted or piloted in the local context, particularly within the organization's mandate.

**Writing guidance:**
- Each recommendation should be specific and actionable, not generic.
- Recommendations must be grounded in specific things that happened during the trip — not generic best practices.
- Aim for 4–8 recommendations total across both sub-headings.
- If the source documents do not provide sufficient basis for a recommendation, insert `[NEEDS INPUT: ...]` rather than writing a vague one.

---

## Step 5: Draft Section 3 — Impressions/Observations

This section is more reflective and analytical in tone, but remains formal and third-person. It captures the traveler's informed perspective on the field and the event.

Cover the applicable sub-topics below, using source documents and any personal notes provided:

**Recent developments in the field of specialization**
What are the current frontiers, emerging trends, or paradigm shifts in the relevant technical domain? What did the event reveal about where the field is heading?

**Status of S&T in the host country**
What is the state of science, technology, and innovation in the country visited? How does it compare to the home context? (If no source documents address this, flag it.)

**Controversial issues arising from the discussion**
Were there debates, contested positions, or unresolved tensions at the event? What were the competing perspectives?

**Outstanding reactions/comments from co-participants**
Were there notable statements, reactions, or contributions from other participants that stood out? (Requires personal notes or direct quotes from sources.)

**Other personal observations**
Any other relevant observations about the event, the host organization, the international community, or implications for the organization's work.

**Writing guidance:**
- This section should read as informed professional reflection, not a second summary of the day-by-day account.
- Avoid repeating details already covered in Section 1.
- If personal notes are sparse, flag which sub-topics need the traveler's input.

---

## Step 6: Draft Section 4 — Linkages Established

This section documents the professional contacts and relationships formed during the trip.

Write a brief introductory sentence or two about the networking opportunities the event provided and the types of connections made.

Then list each contact in the following format:

```
[Full Name], [Title/Designation], [Organization/Institution]
Contact: [Email / Phone / LinkedIn / Website — as available]
[Optional: 1 sentence on context of meeting or potential collaboration]
```

**Critical rules for this section:**
- Only list contacts that are documented in the source materials (calling cards, notes, attendee lists with contact info, etc.).
- Do not invent or look up contact information.
- If contact details are incomplete, include what is available and flag the rest: `[NEEDS INPUT: Complete contact details for this person]`
- If no contacts are documented at all, write: `[NEEDS INPUT: Please provide contact details for individuals met during the trip.]`

---

## Step 7: Produce the Gaps & Flags Summary

After the four sections, append a clearly separated **Gaps & Flags** section. This is for the traveler's use before submitting the report — it is not part of the final submitted document.

Format:

```
---
GAPS & FLAGS (For Writer's Review — Remove Before Submission)

The following items require your input or confirmation before this report is finalized:

1. [Section / Field]: [Description of what is missing or needs verification]
2. [Section / Field]: [Description]
...

Total: [N] items flagged
---
```

Be specific and actionable in each flag so the traveler knows exactly what to provide.

---

## Output Format

Use `file-write` to save the completed draft. Present the completed draft in the following order:

1. Header (Activity Title, Date, Venue)
2. Section 1: Highlights/Major Decisions
3. Section 2: Recommended Follow-Through Actions
4. Section 3: Impressions/Observations
5. Section 4: Linkages Established
6. Gaps & Flags Summary (separated, for writer review only)

The tone throughout should be formal, third-person, and consistent with government/institutional report writing conventions.

---

## Required Capabilities

- `file-search` - Discover all files in the source folder
- `file-read` - Read each source document
- `file-write` - Save the completed travel report draft

---

## Quality Reminders

- **Never fabricate.** A wrong name, a misattributed quote, or an invented session topic is worse than a placeholder.
- **Depth over brevity.** These reports are substantive documents. Section 1 in particular should be thorough — several paragraphs per day is appropriate for dense multi-day events.
- **No generic filler.** Sentences like "The event was very informative and provided valuable insights" add nothing. Be specific or flag the gap.
- **Traceability.** Every specific claim should be traceable to a source document. If you are unsure of the source, flag it.
- **Respect the traveler's voice.** Personal notes, if provided, should inform the Impressions/Observations section especially — that section benefits most from first-person perspective translated into formal third-person prose.
