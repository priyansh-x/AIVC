# Research plan — Weeks 1–4

**Owner:** Priyansh (CEO)  •  **Executor:** `research-analyst` sub-agent  •  **Cadence:** weekly checkpoint

The goal of this phase is **conviction or kill**: by end of week 4 we either have a defensible thesis + an MVP scope, or we know AIVC isn't the right shape and we pivot.

Every output below lands as (a) deep artifact under `research/<area>/` and (b) a ≤1-page brief under `research/briefs/`. CEO reads briefs; deep artifacts exist for audit, drill-down, and future agents.

---

## Week 1 — Problem space mapping

**Question:** What does "AI-native VC" plausibly mean, and which 2–3 sub-problems are real?

**Sub-agent tasks:**
- Survey: every "AI for VC" / "AI-native fund" write-up from 2023–2026. a16z, Sequoia, SignalFire, EQT Motherbrain, Correlation Ventures, Vela, Harmonic, Specter, Hebbia for finance, etc.
- Map the VC workflow end-to-end: sourcing → screening → diligence → memo → IC → post-investment → LP reporting. Tag each stage with: typical time cost, current tooling, where AI has been tried, where it has failed.
- Identify 2–3 candidate wedges with the strongest pain × poor-existing-solution signal.

**Outputs:**
- `research/problem/workflow-map.md`
- `research/problem/wedge-candidates.md`
- `research/briefs/week1-problem-space.md`

**CEO action:** Pick 1–2 wedges to pursue into Week 2.

---

## Week 2 — Customer discovery

**Question:** Do the wedge hypotheses survive contact with real operators?

**Target conversations (25–30):**
- 12–15 VC associates / principals (operators of the pain)
- 5–8 partners / GPs (the buyers)
- 3–5 LPs (the meta-buyer; what they wish their GPs did better)
- 5 founders (supply side; how do they want to be sourced/diligenced)

**Sub-agent tasks:**
- Build outreach target list (LinkedIn + Twitter + BITS alumni network).
- Draft persona-specific outreach templates (Mom Test compliant — no pitching).
- Per interview: ingest transcript via `ingest-interview` skill → tagged pain points, persona, quotes, contradictions.
- Mid-week synthesis: what's converging, what's diverging.

**Outputs:**
- `research/interviews/<slug>.md` per call
- `research/problem/pain-synthesis.md`
- `research/briefs/week2-discovery-readout.md`

**CEO action:** Run the calls. Decide if the wedge still holds.

---

## Week 3 — Market + competitor

**Question:** Is the wedge a real market, and can we win it?

**Sub-agent tasks:**
- **Sizing.** Bottom-up TAM/SAM/SOM. # of funds globally × addressable ACV × plausible capture. Top-down sanity check from VC software market reports. Both with sources.
- **Competitor matrix.** Per-competitor teardown via `competitor-teardown` skill. At minimum: Harmonic, Specter, Tracxn, Affinity, 4Degrees, PitchBook, Vela, SignalFire Beacon, Correlation Ventures, EQT Motherbrain, plus any "AI VC firm" plays. Axes: data moat, workflow vs intelligence, fund-as-customer vs fund-as-operator, pricing, traction signals.
- **Positioning map.** Where do we sit? Where is the white space?
- **Why now / why us.** What changed in the last 18 months that makes this possible?

**Outputs:**
- `research/market/sizing.md` + model
- `research/competitors/<competitor>.md` (one per)
- `research/competitors/positioning-map.md`
- `research/briefs/week3-market-and-competition.md`

**CEO action:** Stress-test the sizing. Decide on positioning.

---

## Week 4 — Thesis + MVP scoping

**Question:** What's the one thing we build first?

**Sub-agent tasks:**
- Synthesize all prior research into a **thesis v0** (1 page): the wedge, the user, the why-now, the moat.
- Strawman product spec (1 page): the smallest end-to-end thing that delivers a "holy shit" moment to a target user.
- Build vs buy audit for the components.
- 8-week MVP timeline.

**Outputs:**
- `research/thesis/v0.md`
- `research/thesis/mvp-spec.md`
- `research/briefs/week4-thesis-and-mvp.md`

**CEO action:** Conviction-or-kill call. If go: greenlight build.

---

## Operating cadence

- **Daily:** sub-agent runs; new interviews ingested same-day; raw artifacts committed.
- **Weekly:** Friday brief delivered to CEO. CEO reads, lands decisions in `docs/decisions/` (to be created when first decision is made).
- **Always:** no claim without a source, no brief over 1 page, no untracked work.
