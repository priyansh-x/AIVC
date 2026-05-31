# The brain

Structured, queryable company knowledge. Every agent reads from and writes to here.

## Layout

- `entities/` — one file per real-world thing
  - `companies/` — competitors, portfolio targets, comparables
  - `people/` — VCs, founders, LPs, advisors
  - `funds/` — investment funds (potential customers, comparables)
  - `deals/` — opportunities we're tracking (future)
- `sources/` — raw inputs we've ingested, with provenance metadata
  - PDFs, transcripts, scraped pages, screenshots
  - Each source file gets a sidecar `.md` with frontmatter
- `schemas/` — YAML/JSON schemas for entity types. Source of truth for shape.

## Entity rules

1. **One file per entity**, slug = stable identifier (e.g. `harmonic-ai.md`).
2. **Frontmatter is required.** Conforms to schema in `brain/schemas/<type>.yaml`.
3. **Provenance fields are required.** `sources: [...]` lists every source backing the entity's claims.
4. **Cross-link liberally** with `[[slug]]`. A person at a fund links to the fund; a deal links to people.
5. **Updates are commits**, never overwrites without a commit. Entity history = git history.

## Sources rules

- File name: `<YYYY-MM-DD>-<short-slug>.<ext>` (e.g. `2026-05-31-harmonic-pricing-page.html`).
- Sidecar metadata file: same name, `.md` extension, with frontmatter: `url`, `retrieved`, `retrieved_by`, `summary`.
- Never delete a source. If it's wrong or stale, mark `superseded_by:` in the sidecar.

## Why this rigor

Two reasons:
1. **Auditability.** A VC's conviction has to be defensible. Every claim → source.
2. **Compounding.** The brain gets more valuable over time only if it's structured. Markdown soup decays.
