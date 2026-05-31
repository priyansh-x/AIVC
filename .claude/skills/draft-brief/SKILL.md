---
name: draft-brief
description: Convert a deep research artifact (under research/<area>/) into a ≤1-page CEO brief. Use when the deep work exists but a brief hasn't been written, or when a brief needs to be regenerated after the artifact changes.
---

# Draft brief

## When to use

- A new file landed under `research/{problem,market,competitors,interviews,thesis}/` without a matching brief in `research/briefs/`.
- The CEO asks "give me the short version of <artifact>".

## Procedure

1. Read the deep artifact in full. Don't skim.
2. Identify the single decision this artifact informs. If you can't, ask the CEO before drafting.
3. Use `docs/brief-template.md` as the structure.
4. Write the brief at `research/briefs/<YYYY-MM-DD>-<slug>.md`:
   - TL;DR: 3 bullets. Bullet 3 names the recommended CEO action.
   - Key findings: ≤5, each with an inline source citation (link to deep artifact section anchor or to a `brain/sources/` file).
   - So what: 1 paragraph. Names the decision implied. Does not hedge.
   - Open questions: 3 max. Each one would actually change the decision if answered.
   - Sources: linked.
5. Verify the rendered page is ≤1 page. If not, cut findings, then prose, never sources.
6. Set `confidence` honestly in frontmatter.
7. Commit: `briefs: <slug>`.

## Hard rules

- No new claims in the brief that aren't in the deep artifact. The brief is a synthesis, not an extension.
- If the deep artifact has contradictions, the brief surfaces them — don't hide them for cleanliness.
- "So what" must name a decision. "We should consider..." is not a decision. "Move forward with X by Friday" is.
