---
id: operating-model-decomposition
type: research-artifact
category: problem
created: 2026-05-31
author: research-analyst
sources:
  - brain/sources/2026-05-31-vc-funnel-metrics-hbs.md
  - brain/sources/2026-05-31-vc-investment-memo-workflow.md
  - brain/sources/2026-05-31-secrets-sand-hill-road.md
  - brain/sources/2026-05-31-reference-call-diligence.md
  - brain/sources/2026-05-31-lp-reporting-relationships.md
  - brain/sources/2026-05-31-a16z-platform-model.md
  - brain/sources/2026-05-31-vc-power-law-horsley-bridge.md
  - brain/sources/2026-05-31-founder-personality-study.md
  - brain/sources/2026-05-31-llm-limits-2026.md
  - brain/sources/2026-05-31-signalfire-beacon-ai.md
  - brain/sources/2026-05-31-eqt-motherbrain.md
  - brain/sources/2026-05-31-correlation-ventures.md
  - brain/sources/2026-05-31-vela-partners.md
  - brain/sources/2026-05-31-harmonic-ai.md
  - brain/sources/2026-05-31-solo-gp-ai-leverage.md
  - brain/sources/2026-05-31-agent-fund-angellist.md
confidence: medium
---

# The VC operating model, atomic-activity by atomic-activity — where does AI change the economics?

## Question

A venture capital firm is a production system. Capital and decisions are the outputs; sourcing, screening, judgment, relationships, and reporting are the inputs. Which of those input activities does AI in 2026 *actually* change the economics of (cost / speed / quality / possibility) and which only get a cosmetic uplift?

## Method

Decompose the VC operating model into 12 atomic activities. For each: (1) job to be done, (2) where time/cost goes today, (3) the specific mechanism by which AI changes it (or doesn't), (4) the irreducibly human residue, (5) leverage score — cosmetic / meaningful / transformative.

A note on terms:
- **Cosmetic** = AI does the same work the human would, faster. Output is indistinguishable. Cost-down, no new behavior.
- **Meaningful** = AI does work the human couldn't do at the same scale, OR shifts where time goes inside an activity. Behavior changes.
- **Transformative** = AI makes possible an activity the firm could not previously perform at all, OR collapses a cost structure so hard the firm's *shape* changes.

---

## 1. Sourcing

**Job to be done.** Build a comprehensive set of investable companies, ideally before competitors see them. Average partner sees 500–1,000 companies/year, takes 150–200 meetings, invests in 8–12 — a ~1% close rate ([HBS funnel data](../../brain/sources/2026-05-31-vc-funnel-metrics-hbs.md)).

**Where time goes today.** ~22 of 55 weekly hours per partner on networking + sourcing ([same]). 58% of deals come from professional-network referrals; only 10% from unsolicited inbound — the network, not the search, is the bottleneck.

**What AI changes — and how.**
- *Discovery of pre-network companies.* Tools like Harmonic.ai, SignalFire's Beacon, EQT's Motherbrain track hiring velocity, GitHub commits, incorporation filings, social momentum on 10M–80M+ entities ([Beacon](../../brain/sources/2026-05-31-signalfire-beacon-ai.md), [Motherbrain](../../brain/sources/2026-05-31-eqt-motherbrain.md), [Harmonic](../../brain/sources/2026-05-31-harmonic-ai.md)). Mechanism: continuously scanning leading-indicator signals no human partner could read at scale.
- *Triage of inbound.* LLMs rank decks and emails by historic performance patterns and thesis fit. Mechanism: pattern-matching against the firm's prior good/bad decisions.

**Irreducibly human residue.** The 58% network-referral channel. A warm intro from a respected former founder is *non-substitutable* signal. AI cannot become someone's trusted ex-boss.

**Leverage score: Meaningful.** Borderline transformative inside the *non-relationship-gated* sub-funnel (the 10–40% of deals that come from cold / signal-driven sourcing). But the relationship-gated majority is unmoved. The risk of cosmetic adoption is real — most VCs already had decent sourcing.

---

## 2. Screening / triage

**Job.** Cut 500–1,000 candidates down to ~150 meeting-worthy ones per partner per year.

**Time today.** First-pass screening is associate-heavy: read deck, glance at team, classify thesis fit. Cheap per-unit, expensive in aggregate. ~10–15% of sourced deals advance to partner ([funnel data](../../brain/sources/2026-05-31-vc-funnel-metrics-hbs.md)).

**What AI changes.** Deck parsing, market classification, team-graph lookup, prior-pass cross-reference — all instant. Mechanism: LLM + structured prompt against the firm's thesis doc + historical decisions DB.

**Irreducibly human residue.** "This isn't obviously interesting but I want to meet anyway" — taste-based exceptions. These are statistically rare but disproportionately produce outliers.

**Leverage score: Transformative.** The clearest collapse-the-cost activity. The firm's *shape* changes here: one analyst with an AI can screen what 3–5 analysts did. This is where the platform-VC headcount premise weakens.

---

## 3. Founder evaluation

**Job.** Form a view on whether this specific person can ship a unicorn-shaped outcome.

**Time today.** Multiple meetings, reference calls, gut. Considered the irreducibly human core of VC. Yet it's also where ~50% of decision weight sits (most early-stage memos collapse to "team + market").

**What AI changes.**
- *Founder pattern extraction.* UNSW/Oxford study: ML on 21,000+ founders' public text predicts success at 82.5%; personality is 5x more predictive than industry ([founder-personality study](../../brain/sources/2026-05-31-founder-personality-study.md)). Mechanism: Big-Five + founder-archetype scoring from public corpus.
- *Background graph.* AI maps a founder's network density, prior team performance, code/writing output. Mechanism: cross-source aggregation.
- *Vela claim:* founder probability before product ([Vela](../../brain/sources/2026-05-31-vela-partners.md)). Whether this generalizes beyond the firm's own re-publication is unverified.

**Irreducibly human residue.** Trust-formation in real time. A founder's response to an unexpected question, their reaction to a hard challenge, the rapport that determines whether they'll pick up the phone in a crisis 4 years later.

**Leverage score: Meaningful.** The hype outruns substance here. AI extracts *correlates* of success; it cannot bear the conviction that gets a partner to write the check. But it materially shifts what humans spend the meeting on — from biographical sleuthing (now automated) to trust formation (irreducible).

---

## 4. Market evaluation

**Job.** Is this a market that can produce a $10B outcome?

**Time today.** Days to weeks of analyst research per memo. Market maps, competitive landscaping, customer-segment sizing.

**What AI changes.** End-to-end market maps from a one-line prompt. Harmonic's Scout, SignalFire Beacon, every major LLM with web tools. Mechanism: web-scale retrieval + structured synthesis. Comparable analyst output goes from 3 days to ~3 hours.

**Irreducibly human residue.** Contrarian market reads — recognizing a market that doesn't yet show in any data set (because the leading indicators are not yet legible). The best market calls in VC history (mobile in 2007, crypto in 2013) were made *against* the data.

**Leverage score: Transformative for default work, cosmetic for contrarian work.** AI raises the floor of market analysis and lowers its cost. It does not raise the ceiling — and the ceiling is where the power-law outliers live.

---

## 5. Technical diligence

**Job.** Assess product, architecture, defensibility. Hardest at deep tech, AI infra, biotech.

**Time today.** Often outsourced or done by ex-operator partners. Heavy serial reading + targeted expert calls.

**What AI changes.** Code-review at scale. Architecture critique. Patent landscape analysis. Comparison to published research. Mechanism: code-aware LLMs + retrieval over papers + structured rubric.

**Irreducibly human residue.** Judging whether a research lead has "taste" — whether their model choices are first-principles or cargo-culted. AI cannot yet evaluate scientific aesthetics reliably.

**Leverage score: Meaningful.** Technical-diligence cost falls; quality rises if the operator partner stays in the loop. AI-only tech diligence (no operator) overestimates polished-but-derivative work — known LLM failure mode.

---

## 6. Reference calls / backchannels

**Job.** Get high-signal third-party views on founder and traction. Avg 10 calls / 118 hrs per deal ([reference-call source](../../brain/sources/2026-05-31-reference-call-diligence.md)).

**Time today.** Prep, scheduling, call, write-up, synthesis — heavy.

**What AI changes.** Prep questions, call transcription, sentiment, theme extraction, synthesis into memo language. Mechanism: ASR + LLM summary against a structured rubric. ~70% of non-call time compressible.

**Irreducibly human residue.** Two things: (1) the *call itself* — candor depends on social trust, which AI cannot manufacture; (2) the *network access* — getting the unfiltered ex-employee on the phone requires that the partner is someone they're willing to talk to. AI cannot make people trust you.

**Leverage score: Meaningful.** Compresses prep + write-up; does not change the relationship economics of the call itself.

---

## 7. Memo drafting

**Job.** Produce the IC memo. ~3,000 words formal IC memo; analysts spend ~80% of their time on this ([memo workflow](../../brain/sources/2026-05-31-vc-investment-memo-workflow.md)).

**Time today.** Days of writing + revision. Heavy templated content (market, competition, financials, team) wrapped around 1–2 distinctive sections ("why we win," "risks I'm carrying").

**What AI changes.** Templated sections are now first-draftable in minutes. Auto-update of financial / competitive / market sections from data refresh. Mechanism: structured-prompt LLM → markdown.

**Irreducibly human residue.** The political function of the memo — partner conviction signaling, partnership debate fuel, accountability for the call. The IC memo is partly a vote-procurement document; AI cannot procure votes.

**Leverage score: Transformative for the artifact, cosmetic for the underlying decision.** Memo drafting is the single highest-time-savings activity for analysts. Whether that translates into better *decisions* is unproven — and the Correlation Ventures 15-year track record suggests it does not, on its own.

---

## 8. Investment committee

**Job.** Surface conflicts, force conviction-statement, make the decision.

**Time today.** Weekly partner meeting. Live debate. Partnership norm: "I'll back you on this one."

**What AI changes.** Minimal direct impact. AI can prep IC packets and counter-arguments ("what would a skeptical partner say?"); some firms use it as a "devil's advocate" agent.

**Irreducibly human residue.** The vote, the conflict, the partnership consequence of a bad call. IC is the social-capital ledger of the firm. AI can inform it; AI cannot be on it.

**Leverage score: Cosmetic.** A small lift. Anyone selling "AI replaces IC" is selling marketing.

---

## 9. Term sheet negotiation

**Job.** Price the round, structure the deal, define governance.

**Time today.** Hours to days. Pattern-match against recent comps; lawyer back-and-forth.

**What AI changes.** Comps lookup (instant), term-sheet redlining (LLM + legal corpus), market-standard flagging. Mechanism: retrieval over the firm's own past term sheets + market data.

**Irreducibly human residue.** Negotiation itself — managing the founder relationship while contesting valuation. Setting a precedent the firm can live with.

**Leverage score: Meaningful.** Real time-saving; no shape change to the firm.

---

## 10. Portfolio support / platform

**Job.** Help portfolio companies recruit, sell, ship, raise. a16z built a 150+ person platform around this ([a16z platform](../../brain/sources/2026-05-31-a16z-platform-model.md)). NEA has a vendor platform; most mid-size firms have 5–20 platform people.

**Time today.** Highest fixed-cost activity in a modern VC outside investing itself. Reactive (founder calls in distress) + proactive (programming, intros, ops reviews).

**What AI changes.**
- *Talent search:* SignalFire Beacon used directly for portfolio recruiting ([same source](../../brain/sources/2026-05-31-signalfire-beacon-ai.md)). Mechanism: matchmaking against 80M+ orgs.
- *Sales/GTM agents:* AI SDR-style agents inside portfolio companies, increasingly orchestrated by the fund.
- *Operating playbooks on demand:* an LLM with the firm's institutional knowledge becomes a 24/7 on-call ex-operator for every portfolio CEO.
- *Diligence-on-portfolio:* continuous monitoring of portfolio health (hiring, attrition, web traffic, customer reviews) so support gets allocated before founders ask.

**Irreducibly human residue.** Emotional support during near-death moments. Senior intros where the GP's reputation is the asset. Board judgment.

**Leverage score: Transformative.** This is plausibly the biggest economic-shape change AI brings to VC. If 80% of platform headcount cost converts to AI cost, the unit economics of being a platform VC change radically. Replicating 30% of a16z's platform value with software flips the cost model.

---

## 11. Follow-on decisions

**Job.** Decide reserves, ratable participation, pro-rata pass.

**Time today.** Ad hoc per company; often under-rigorous.

**What AI changes.** Continuous portfolio health scoring + counterfactual analysis (what's the marginal $ worth here vs new deal?). Mechanism: KPI ingestion + portfolio-construction modeling.

**Irreducibly human residue.** Political — backing a struggling founder you have a relationship with even when the math says no. Not always wrong.

**Leverage score: Meaningful.** Better-informed decisions; relationship overrides remain.

---

## 12. LP communications & fundraising

**Job.** Keep LPs informed; raise the next fund.

**Time today.** Quarterly reports (ILPA-conformant); annual meeting; ongoing 1:1s; multi-year fundraising cycles. Established LP roster drops cost-to-raise ~67% and time-to-first-close 6–9 months ([LP source](../../brain/sources/2026-05-31-lp-reporting-relationships.md)).

**What AI changes.** Data-room automation, KPI rollups, portfolio-narrative drafting, LP-update generation. Mechanism: ingestion of portfolio data → templated LP narrative per LP archetype.

**Irreducibly human residue.** The relationship. Pension funds and endowments do not commit nine-figure checks to AI agents. The fundraising sales cycle is multi-meeting, multi-year, judgment-laden.

**Leverage score: Meaningful.** Reporting cost falls. Fundraising itself is unchanged.

---

## Cross-cutting analysis

**The two atomic activities AI most transforms (the wedge candidates):**

1. **Screening + memo drafting (the "associate stack")** — this is where 80%+ of headcount cost in a modern fund lives, and it's the most templated work. AI doesn't just speed it up; it removes the need for the role.
2. **Portfolio support / platform** — the most labor-intensive non-investing activity. The firm shape changes when this converts to software.

**The two atomic activities where AI is mostly cosmetic in 2026:**

1. **IC / final commitment** — political, not analytic. (Agent Fund, the most AI-native fund in market, still keeps humans on commit ([Agent Fund](../../brain/sources/2026-05-31-agent-fund-angellist.md)).)
2. **Network-gated sourcing** — the 58% of deals that come from relationships are not unlocked by software.

**A productive tension:** Correlation Ventures has been "AI-investing" for 15+ years and is ~$500M AUM, co-invest-only ([Correlation](../../brain/sources/2026-05-31-correlation-ventures.md)). EQT Motherbrain has been operating inside an incumbent for 10 years and produced 15 attributed deals, one fund-returning ([Motherbrain](../../brain/sources/2026-05-31-eqt-motherbrain.md)). Both validate "meaningful." Neither validates "transformative." The 2026 question is whether agentic capabilities cross a different threshold.

**LLM-limit constraint.** Hallucination rates 8–52% across 2026 benchmarks; reasoning is post-hoc rationalization, not faithful introspection ([LLM limits](../../brain/sources/2026-05-31-llm-limits-2026.md)). This forces a hard rule: the activities AI cannot own in 2026 are the ones where a hallucinated input becomes an irreversible commitment of capital or reputation. That is precisely IC, fundraising, and final founder yes/no.

## Contradictions

- *"AI-native VC outperforms"* (Vela, Air Street narrative) **vs** *Correlation's 15-year track of solid-but-not-category-defining returns.* Resolution: AI-native may be necessary but not sufficient. Without sourcing access (network or brand), the model produces middle-of-distribution picks, not outliers.
- *"AI sees what humans miss"* (Beacon, Motherbrain narrative) **vs** *the power law says 6% of deals = 60% of returns and outliers are by definition pre-signal.* Resolution: AI finds early *late*-stage signals (hiring spikes); humans still find pre-signal opportunities (founder vision, contrarian thesis).
- *Solo-GP-with-AI scales to $200M+* (Air Street) **vs** *AI-only fund (Correlation) plateaus at $500M after 15 years.* Resolution: it's not "AI" that scales the fund; it's *brand + AI*. Tooling without brand is not a fundraising story.

## Open questions

1. Does an AI-native fund actually source *different* deals than a non-AI peer, or just the same deals faster? (No public DPI comparison exists for Vela or Agent Fund yet.)
2. Are the wins SignalFire / EQT report attributable to AI, or to capital and brand that would have won those deals anyway?
3. What's the LP appetite ceiling for "autonomous decisions"? Agent Fund stops at semi-autonomous. Will any LP commit to a fully autonomous IC in this decade?
4. What's the marginal cost of an AI-native fund per portfolio company vs a traditional platform fund? No public number exists; this is a candidate for our own modeling.

## Sources

See frontmatter. Cross-link to entities: [[signalfire]], [[eqt-ventures]], [[correlation-ventures]], [[vela-partners]], [[air-street-capital]], [[agent-fund]], [[harmonic-ai]].
