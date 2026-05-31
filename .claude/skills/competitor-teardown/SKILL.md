---
name: competitor-teardown
description: Deep teardown of a competitor or adjacent player in the AI-for-VC / VC-tech space. Use when the CEO names a company to investigate or when a new competitor surfaces in research. Produces a structured competitor profile, a company entity, and a brief.
---

# Competitor teardown

## Procedure

1. **Confirm the target.** Company name + URL. If ambiguous, ask.
2. **Source sweep** (use `WebSearch` + `WebFetch`):
   - Homepage, pricing page, product/features pages
   - Latest 3–6 months of blog posts / changelog
   - Founder podcast appearances, interviews, conference talks
   - Crunchbase / PitchBook funding history (whatever's free + accessible)
   - LinkedIn job postings (signals on what they're building next)
   - Customer reviews (G2, Capterra, Twitter threads)
   - Compare-page traffic ("X vs Y") for who they position against
3. **Write company entity** at `brain/entities/companies/<slug>.md` per `brain/schemas/company.yaml`.
4. **Write deep teardown** at `research/competitors/<slug>.md`:
   - **Snapshot** — what they do, in one paragraph
   - **Wedge** — the specific job they originally won
   - **Product surface** — features, with screenshots/URLs cited
   - **Business model** — pricing, ACV estimate, GTM motion
   - **Customer evidence** — who uses them, what they say
   - **Moat hypothesis** — data, network, distribution, or none
   - **Trajectory signals** — hiring, fundraising, releases, founder commentary
   - **Where they're weak** — gaps a new entrant could exploit
   - **Implications for AIVC** — does this validate or threaten our wedge?
   - **Sources** — full list
5. **Write brief** at `research/briefs/<YYYY-MM-DD>-competitor-<slug>.md` using `docs/brief-template.md`. The "So what" must answer: *threat, validation, or irrelevant?*
6. **Update positioning map** at `research/competitors/positioning-map.md` (create if missing) with this player.
7. **Commit.** `research: competitor teardown — <name>`.

## Hard rules

- Cite every claim. "They have 200 customers" → source or don't say it.
- Distinguish marketing claims from external evidence. A pricing page is primary. A founder's tweet is primary-ish. A third-party "top 10" listicle is weak.
- If you can't find pricing, say so. Don't guess.
