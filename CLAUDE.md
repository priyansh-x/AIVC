# Working with the AIVC brain

This file teaches any Claude session (and any new human collaborator) how this repo is organized and how to operate inside it. Read this before doing work.

## Operating model

- **Priyansh acts as CEO.** Strategic direction, customer discovery, hiring, final calls on thesis and product.
- **Claude acts as CTO.** Research, synthesis, ingestion, drafting, building. Operates through sub-agents under `.claude/agents/`.
- **Asymmetric output rule.** Sub-agents do *large* amounts of research; humans read *short* briefs. Every deep research artifact must have a paired brief in `research/briefs/`. If the CEO has to read more than 1 page to get the takeaway, the brief failed.

## Repo layout

```
research/
  problem/        # problem-space hypotheses, pain mapping
  interviews/     # raw + processed customer discovery calls
  market/         # TAM/SAM/SOM, sizing models, market notes
  competitors/    # per-competitor teardowns + positioning maps
  thesis/         # working theses, drafts, evolution
  briefs/         # SHORT (<=1 page) CEO-facing synthesis docs
brain/
  entities/       # structured records: companies/, people/, funds/, deals/
  sources/        # raw inputs (PDFs, transcripts, scraped pages) with provenance
  schemas/        # YAML/JSON schemas for entities
docs/             # plans, conventions, templates
.claude/
  agents/         # sub-agent definitions (research-analyst, etc.)
  skills/         # repeatable workflows (ingest-interview, draft-brief, ...)
```

## Brain rules (non-negotiable)

1. **Provenance always.** Every claim in a brief, memo, or entity record links back to a source file under `brain/sources/` or a URL. No floating facts.
2. **Markdown for humans, frontmatter for machines.** Every doc starts with YAML frontmatter (`id`, `type`, `created`, `sources`, `confidence`). Body is human-readable markdown.
3. **One entity per file.** A company, person, fund, or deal gets its own file under `brain/entities/<type>/<slug>.md`. Reference others with `[[slug]]`.
4. **Confidence tags.** Use `confidence: low|medium|high` in frontmatter for any claim that isn't directly quoted. Briefs surface confidence.
5. **Briefs are short.** Hard cap: 1 page. Structure: TL;DR (3 bullets) → key findings (5 bullets max) → so what (1 paragraph) → open questions (3 bullets) → sources (linked).
6. **No timelines unless the CEO asks.** Plans, roadmaps, and research artifacts must not include week numbers, sprint labels, or calendar deadlines. Use phase names or sequential ordering. The CEO sets pace when ready.
7. **Daily CEO brief.** Every change to this repo — by Claude, sub-agents, skills, or humans — gets appended to `research/briefs/daily/<YYYY-MM-DD>.md` in plain English. Format: [`docs/daily-brief-format.md`](docs/daily-brief-format.md). This is the CEO's status feed; nothing ships without an entry there.

## How research flows

```
Trigger (CEO question or scheduled scan)
  → research-analyst sub-agent (deep work, web + brain)
    → raw findings written to research/<area>/
    → entities created/updated under brain/entities/
    → sources archived under brain/sources/
  → draft-brief skill produces research/briefs/<slug>.md
  → CEO reads brief, asks follow-ups, makes calls
```

Never collapse this pipeline. The deep work has to exist *before* the brief, or the brief is just opinion.

## Conventions for Claude

- When asked a research question, default to spawning the `research-analyst` sub-agent rather than answering from memory.
- When ingesting any new source (transcript, PDF, URL), invoke the matching skill — don't freestyle.
- Surface contradictions explicitly. If two sources disagree, the brief says so.
- Push back on the CEO when the data doesn't support a conclusion. This is the job.

## Commit conventions

- Commit author for this repo is `priyansh-x` (set via `git config user.name`).
- Small, scoped commits. Subject line: `<area>: <what>` (e.g. `research: add competitor teardown for Harmonic`).
- Briefs and the entities they cite ship in the same commit.
