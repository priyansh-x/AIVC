# Research plan

**Owner:** Priyansh (CEO)  •  **Executor:** `research-analyst` sub-agent

Goal of this phase: **conviction or kill.** We exit either with a defensible thesis + an MVP scope, or with a clear reason AIVC isn't the right shape and we pivot.

Every output below lands as (a) a deep artifact under `research/<area>/`, (b) a ≤1-page brief under `research/briefs/`, and (c) an append to the day's [daily CEO brief](../research/briefs/daily/). The CEO reads briefs; deep artifacts exist for audit, drill-down, and future agents.

No timelines in this plan by design — phases run as fast as the evidence allows. The CEO sets pace.

---

## Phase 0 — Foundations (first principles)

**Question:** What does an AI-native VC firm actually look like, from first principles? Which parts of the VC operating model can be automated, augmented, or rebuilt entirely? Where is the leverage real vs. cosmetic?

**Sub-agent tasks:**
- Decompose the VC operating model into atomic activities (sourcing, screening, founder eval, market eval, technical diligence, reference calls, memo writing, IC, term sheet, portfolio support, follow-on, LP comms, fundraising).
- For each, ask: what's the *job to be done*, where does the cost/time go today, what does AI plausibly change, what's the irreducible-human part?
- Map the space of "AI-native VC" interpretations — from "VC firm with AI tools" to "AI is the investor" — and stake out where AIVC could sit.
- Identify the 2–3 atomic activities where AI changes the economics most.

**Outputs:**
- `research/problem/ai-native-vc-first-principles.md`
- `research/problem/operating-model-decomposition.md`
- `research/briefs/<date>-foundations.md`

**CEO action:** Pick where on the AI-native spectrum AIVC sits. Pick 1–2 atomic activities to pursue into Phase 1.

---

## Phase 1 — Problem space mapping

**Question:** Within the wedge zone we picked, which sub-problems are real, painful, and poorly served today?

**Sub-agent tasks:**
- Survey every "AI for VC" / "AI-native fund" write-up worth reading. a16z, Sequoia, SignalFire, EQT Motherbrain, Correlation Ventures, Vela, Harmonic, Specter, Hebbia-for-finance, etc.
- Map the workflow inside the chosen wedge: stages, time costs, current tooling, where AI has been tried, where it has failed.
- Identify 2–3 candidate wedges with the strongest pain × poor-existing-solution signal.

**Outputs:**
- `research/problem/workflow-map.md`
- `research/problem/wedge-candidates.md`
- `research/briefs/<date>-problem-space.md`

**CEO action:** Pick 1–2 wedges to take into discovery.

---

## Phase 2 — Customer discovery

**Question:** Do the wedge hypotheses survive contact with real operators?

**Target conversations (~25–30 total):**
- VC associates / principals (operators of the pain)
- Partners / GPs (the buyers)
- LPs (the meta-buyer — what they wish their GPs did better)
- Founders (supply side — how they want to be sourced/diligenced)

**Sub-agent tasks:**
- Build outreach target lists (LinkedIn, Twitter, BITS network).
- Draft persona-specific outreach (Mom Test compliant — no pitching).
- Per interview: ingest via `ingest-interview` → tagged pain points, persona, quotes, contradictions.
- Running synthesis: what's converging, what's diverging.

**Outputs:**
- `research/interviews/<slug>.md` per call
- `research/problem/pain-synthesis.md`
- `research/briefs/<date>-discovery-readout.md`

**CEO action:** Run the calls. Decide if the wedge still holds.

---

## Phase 3 — Market + competitor

**Question:** Is the wedge a real market, and can we win it?

**Sub-agent tasks:**
- **Sizing.** Bottom-up TAM/SAM/SOM. # of funds globally × addressable ACV × plausible capture. Top-down sanity check from market reports. Both with sources.
- **Competitor teardowns.** Per `competitor-teardown` skill. At minimum: Harmonic, Specter, Tracxn, Affinity, 4Degrees, PitchBook, Vela, SignalFire Beacon, Correlation Ventures, EQT Motherbrain, plus the "AI VC firm" plays. Axes: data moat, workflow vs intelligence, fund-as-customer vs fund-as-operator, pricing, traction.
- **Positioning map.** Where do we sit? Where is the white space?
- **Why now / why us.**

**Outputs:**
- `research/market/sizing.md`
- `research/competitors/<competitor>.md` (one per)
- `research/competitors/positioning-map.md`
- `research/briefs/<date>-market-and-competition.md`

**CEO action:** Stress-test the sizing. Lock positioning.

---

## Phase 4 — Thesis + MVP scoping

**Question:** What's the one thing we build first?

**Sub-agent tasks:**
- Synthesize prior phases into a **thesis v0** (1 page): wedge, user, why-now, moat.
- Strawman product spec (1 page): smallest end-to-end thing that delivers a "holy shit" moment to a target user.
- Build vs buy audit for components.
- Rough scoping for an MVP (effort estimate, not a deadline).

**Outputs:**
- `research/thesis/v0.md`
- `research/thesis/mvp-spec.md`
- `research/briefs/<date>-thesis-and-mvp.md`

**CEO action:** Conviction-or-kill call.

---

## Operating rules

- **Daily brief.** Every change to this repo gets appended to `research/briefs/daily/<YYYY-MM-DD>.md` in plain English — what was done, why, what's next.
- **Briefs ≤ 1 page.** Always.
- **No claim without a source.**
- **No timelines unless the CEO asks.** Phases run as evidence allows.
