---
name: founder-research
description: Build a research dossier on a founder or a founding team. Use when the CEO is preparing for a meeting with a founder, evaluating a potential portfolio company, or sourcing. Produces person + company entities and a short pre-meeting brief.
---

# Founder research

## Procedure

1. **Identify** the founder(s) and company. Confirm URL / LinkedIn before proceeding.
2. **Source sweep:**
   - Company: site, latest product, pricing, hiring
   - Founder: LinkedIn, Twitter/X, podcasts, prior companies, GitHub if technical, any writing
   - Funding: Crunchbase / press releases / public filings
   - Customers: any public references
3. **Entities:**
   - `brain/entities/people/<founder-slug>.md`
   - `brain/entities/companies/<company-slug>.md`
   - Cross-link via `[[slug]]`
4. **Pre-meeting brief** at `research/briefs/<YYYY-MM-DD>-founder-<slug>.md`:
   - TL;DR: who they are in 3 bullets, with one notable signal (positive or red flag)
   - Background: prior experience, prior outcomes
   - What they're building: in their own words (quote from site/pitch), plus your read
   - Traction signals: hiring, revenue indicators, customer mentions
   - Questions to ask in the meeting: 5 sharp questions tailored to gaps in public info
   - Open flags: anything that needs verification in-meeting
5. **Commit.** `research: founder dossier — <name>`.

## Hard rules

- Verify identities. Linkedin profiles with mismatched job histories → flag.
- Distinguish what they claim from what's externally verifiable.
- Five great questions > twenty mediocre ones.
