---
name: minutes-of-meeting
description: Generate standardized Minutes of the Meeting with structured header metadata, Roman numeral sections (I-VI), objective discussion bullets, and closing sign-offs, based on a transcript/notes and meeting metadata. Use when writing meeting minutes, formatting MoM from transcripts, or preparing official meeting records.
---

# Minutes of the Meeting Generator — SKILL.md (v1.0)

## Purpose

Produce **copy-ready Minutes of the Meeting** aligned with a standard institutional minutes format:
- Standard **meeting metadata block** (Meeting Title, Division-in-Charge, Date, Time, Venue, Reference No.).
- Roman numeral sections **I–VI**: Call to Order, Approval of Provisional Agenda, Review of Minutes, Updates on Decision-Action Items, Discussions, Adjournment.
- **Objective, factual** language; structured bulleting in Discussions; explicit Action Items; sign-offs (Prepared by / Reviewed by).

## When to Use

Use this skill when you have:
- Meeting details (title/date/time/venue/division/reference no.)
- Participants list (grouped by organization)
- Notes or transcript (raw or cleaned)
- Action items and responsible parties (even if tentative)

## Trigger Phrases

- "Generate meeting minutes"
- "Create minutes of meeting"
- "Format meeting minutes"
- "Write MOM"

## Inputs Required

### A) Meeting Metadata (required)
- Reference No.: (YYYY)-(MM) or per division tracking
- Meeting Title:
- Division-in-Charge:
- Date:
- Time:
- Venue: (Online Meeting / Room / Hybrid)

### B) Attendance (required)
Provide as:
- Organization 1:
  - Full Name, Position/Role
- Organization 2:
  - Full Name, Position/Role

### C) Content Sources (at least one required)
- Transcript (preferred), OR
- Facilitator notes / agenda notes, OR
- Chat log + decisions summary

### D) Decisions / Action Items (optional but recommended)
- Action item statement
- Owner / responsible unit
- Target timeline (if stated)
- Dependencies / next meeting (if any)

## Output

A single minutes document in **standard institutional style**, ready to paste into your template or word processor.

## House Style & Rules

### Tone and Voice
- **Objective, third-person**, past tense.
- No filler, no personal opinions, no "I/we think".
- Use **clear, informational** wording suitable for internal records.

### Formatting Rules

1. Use Roman numeral section headers: **I. … VI. …**
2. Use short paragraphs for I–IV; use structured bullets for V (Discussions).
3. Keep organization groupings and bullet lists consistent:
   - Organization Name:
     - • Name, Title/Role
4. If a section has no content, write **"N/A"** on the next line.
5. Use an **Action Items:** block (explicit label) when there are tasks; include owners.
6. Close with:
   - **Prepared By:** NAME (ALL CAPS), Position Title
   - **Reviewed by:** NAME (ALL CAPS), Position Title

### Content Quality Rules

- Resolve obvious transcription errors and normalize terms (e.g., acronyms), but **do not invent facts**.
- Prefer **concrete statements**:
  - What was presented/offered
  - What was discussed/clarified
  - What opportunities/risks were raised
  - What follow-ups were agreed
- If details are missing, keep statements general and do not speculate.

## Document Template (copy-ready)

> Replace bracketed placeholders with actual details.

```
**Reference No.** (____)-(____)  
**MINUTES OF THE MEETING**

**Meeting Title** : [Meeting Title]  
**Division-in-Charge** : [Division]  
**Date** : [DD Month YYYY]  
**Time** : [Start – End]  
**Venue** : [Online Meeting / Location]

---

### I. Call to Order

The meeting was called to order and commenced at [time]. The following participants were in attendance:

**[Organization / Group 1]:**  
  • [Full Name], [Position/Role]  
  • [Full Name], [Position/Role]

**[Organization / Group 2]:**  
  • [Full Name], [Position/Role]  
  • [Full Name], [Position/Role]

### II. Approval of Provisional Agenda

[1 short paragraph summarizing the agenda context and the high-level intent of the meeting. If the agenda was presented and accepted without changes, state that clearly.]

### III. Review of Minutes of the Meeting

N/A  
(or: [State whether prior minutes were reviewed/approved, and any corrections agreed.])

### IV. Updates on Decision-Action Items (DAIs)

N/A  
(or: [List DAIs and status updates briefly, if applicable.])

### V. Discussions

- **[Theme/Topic 1 — concise label]**
  - [Key point 1: what was presented/clarified]
  - [Key point 2: important specs/constraints, if stated]
  - [Key point 3: implications or considerations]

- **[Theme/Topic 2 — concise label]**
  - [Key point 1]
  - [Key point 2]

- **[Synergies / Opportunities / Risks — if raised]**
  - [Opportunity/Risk statement]
  - [Rationale or context]
  - [Next step direction]

**Action Items:**
- [Owner/Org]: [Action item statement]  
- [Owner/Org]: [Action item statement]  
- [If needed] Schedule: [Follow-up meeting / technical deep dive], [timeframe], [purpose]

### VI. Adjournment

The meeting was adjourned at [time] and concluded with [brief neutral closing statement, e.g., mutual appreciation for the discussion].

---

**Prepared By:**  
[NAME IN ALL CAPS]  
[Position Title]

**Reviewed by:**  
[NAME IN ALL CAPS]  
[Position Title]
```

## Generation Procedure (how the skill should work)

1. Ingest meeting metadata + attendance list.
2. Parse notes/transcript into:
   - agenda intent (II)
   - prior minutes/DAIs status (III–IV)
   - clustered discussion themes (V)
   - action items with owners (V)
3. Write V (Discussions) as **topic clusters**, each with 2–5 bullets:
   - start with the external party's presentation/offer (if applicable),
   - then the convening unit's context/needs,
   - then synergy/opportunity,
   - end with action items and scheduling.
4. Insert "N/A" for sections without evidence.
5. Final pass: enforce objectivity, tense consistency, and completeness.

## QA Checklist (must pass)

- [ ] Header fields present: title/division/date/time/venue/reference no.
- [ ] Attendance grouped by organization with name + role.
- [ ] Roman numeral sections I–VI present and ordered.
- [ ] "N/A" used where appropriate (no empty sections).
- [ ] Discussions are MECE-ish clusters (no duplicated points).
- [ ] Action items have clear owner labels; no invented timelines.
- [ ] Adjournment includes end time.
- [ ] Prepared By / Reviewed by blocks complete (names in ALL CAPS).

## Tags

#skill #skill/documentation #minutes-of-meeting #status/active
