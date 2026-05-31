# Daily CEO brief — format

Location: `research/briefs/daily/<YYYY-MM-DD>.md`. One file per day, appended throughout the day.

Purpose: a plain-English log the CEO can read in 60 seconds to catch up on the day's activity without reading the diff. **Not** the structured brief template — this is conversational.

## Required sections

```markdown
# Daily brief — YYYY-MM-DD

## Plain summary
A short paragraph in plain English. What got done today, why it mattered, where we stand.

## What changed in the repo
- One bullet per meaningful change. Link to the file(s).

## What we learned
- One bullet per real insight. Link to the artifact/brief that contains it.

## Open threads / next up
- What's in flight, what's blocked, what the CEO should decide next.
```

## Rules

- **Plain English. No jargon. No frontmatter required.** This is a human log.
- **Append, don't rewrite.** If multiple work sessions happen in a day, add new entries under the existing sections with a `### HH:MM` subheading. The file grows through the day.
- **Every meaningful change must show up here.** A new artifact, a new brief, a new entity, a scaffold edit, a doc rename — log it.
- **Link liberally.** Anything mentioned should be one click away.
- **End with "Open threads / next up".** The CEO uses this to decide what to act on.

## Who writes to it

- The `research-analyst` sub-agent, at the end of every task it completes.
- Any skill that lands a change in the repo.
- The main Claude session, at the end of any work session.
- A human collaborator, manually, when they make changes outside Claude.

If today's file doesn't exist when you go to write, create it with the sections above.
