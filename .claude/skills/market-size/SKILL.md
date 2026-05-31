---
name: market-size
description: Build a defensible TAM/SAM/SOM for an AIVC wedge. Use when the CEO asks for market sizing or when a new wedge needs sizing. Produces a bottom-up model, a top-down sanity check, and a brief.
---

# Market sizing

## Procedure

1. **Define the wedge precisely.** One sentence: "<who> pays <how much> for <what job>". If you can't write that, stop and ask.
2. **Bottom-up build:**
   - Universe: count the target customers (e.g. # of VC funds globally, # of associates per fund, # of LPs). Cite each number.
   - Reachable: what fraction can we plausibly reach in 3 years? Justify.
   - ACV: a defended range, not a single number. Anchor to comparable products' pricing (use competitor entities).
   - TAM = universe × max ACV. SAM = reachable × mid ACV. SOM = 1–3 yr realistic capture.
3. **Top-down sanity check:**
   - Pull at least 2 independent third-party estimates of the VC software / fintech-for-funds market.
   - If bottom-up and top-down are >2x apart, explain why and adjust.
4. **Sensitivity:** show how SAM moves if ACV halves or doubles, and if reachable customer % moves ±50%.
5. **Output:**
   - `research/market/sizing-<wedge-slug>.md` — the full model with every number sourced
   - `research/briefs/<YYYY-MM-DD>-market-size-<wedge-slug>.md` — the brief. TL;DR: "TAM $X, SAM $Y, SOM $Z. Key uncertainty: <one thing>."
   - Sources logged under `brain/sources/`
6. **Commit.** `research: market sizing — <wedge>`.

## Hard rules

- No number without a source. "Industry estimates suggest..." is not a source.
- Ranges, not false precision. "$80M–$140M SAM" beats "$112M SAM" when uncertainty is real.
- Surface the load-bearing assumption. Every sizing has one number that, if wrong, breaks the model. Name it in the brief.
