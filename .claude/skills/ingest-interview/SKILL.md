---
name: ingest-interview
description: Ingest a customer-discovery interview transcript into the AIVC brain. Use when a new transcript, recording summary, or call notes file is provided. Produces a structured interview record, updates person/fund entities, and surfaces pain-point tags.
---

# Ingest interview

Take raw interview material (transcript, notes, or audio summary) and turn it into a structured, queryable record in the brain.

## When to use

- User says "ingest this interview" / "process this call" / drops a transcript file
- A new file appears in `research/interviews/_raw/`

## Procedure

1. **Identify the interviewee.** Name, role, fund/company, persona category (VC associate, GP, LP, founder).
2. **Save raw source** at `brain/sources/<YYYY-MM-DD>-interview-<slug>.md` with frontmatter: `url: null`, `retrieved`, `retrieved_by: ingest-interview`, `summary` (2 lines).
3. **Write structured interview record** at `research/interviews/<YYYY-MM-DD>-<persona>-<slug>.md` with:
   - Frontmatter: `id`, `type: interview`, `persona`, `interviewee` (links to person entity), `date`, `interviewer`, `duration_min`, `sources`, `confidence`.
   - Sections:
     - **Context** (2–3 lines: who, why, what fund/co)
     - **Pain points** — bulleted, each tagged `#sourcing #diligence #portfolio-ops` etc., with verbatim quote
     - **Current workflow** — how do they do this today, what tools
     - **Wishlist / unprompted asks** — what they said they wished existed
     - **Objections to AI-native VC tooling** — any skepticism
     - **Quotes worth keeping** — verbatim, attributed by timestamp if available
     - **Follow-ups** — questions for next call
4. **Update entity files**:
   - `brain/entities/people/<slug>.md` for the interviewee
   - `brain/entities/funds/<slug>.md` if they're at a fund we haven't recorded
5. **Tag for synthesis.** Add to `research/problem/pain-synthesis.md` (create if missing) a one-line entry per distinct pain point with link back to interview.
6. **Commit.** `research: ingest interview — <persona> at <fund>`.

## Hard rules

- Mom Test compliance check: if the interviewer pitched the product or asked leading questions, flag it in `confidence` and note in the record.
- Never invent quotes. If something isn't a direct quote, don't put it in quote marks.
- If the interview contradicts an earlier one, link the contradiction explicitly in both records.
