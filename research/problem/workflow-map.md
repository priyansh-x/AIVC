---
id: workflow-map-india-associate-stack
type: research-artifact
category: problem
created: 2026-05-31
author: research-analyst
sources:
  - brain/sources/2026-05-31-sajith-pai-reflections-one-year.md
  - brain/sources/2026-05-31-sajith-pai-five-years.md
  - brain/sources/2026-05-31-blume-hiring-analysts.md
  - brain/sources/2026-05-31-indian-vc-tech-stack.md
  - brain/sources/2026-05-31-taghash-india-vc-os.md
  - brain/sources/2026-05-31-taghash-indian-vc-survey.md
  - brain/sources/2026-05-31-bain-india-vc-report-2025.md
  - brain/sources/2026-05-31-tracxn-india.md
  - brain/sources/2026-05-31-sanchi-connect.md
  - brain/sources/2026-05-31-evertrace-vc-dealflow.md
  - brain/sources/2026-05-31-india-vc-analyst-salaries.md
  - brain/sources/2026-05-31-mca-roc-india-diligence.md
  - brain/sources/2026-05-31-india-vc-ai-memo-claude.md
confidence: medium
---

# The Indian VC associate workflow — atomised, with tooling and pain

## Question

Inside the associate-stack wedge (screening + memo drafting + market research + comp pulls), what does a junior investment staffer at an Indian seed/Series-A fund actually do, with which tools, and where is pain concentrated?

## Method

(1) Map the workflow stage by stage; (2) for each stage, capture activities, time-cost, current tooling penetration in India, and pain. (3) Cross-check Indian sources (Sajith Pai's Blume writeups, Taghash survey, IndianVCs.com stack catalogue, Blume hiring commentary, 100X.VC public funnel numbers) against the US baseline from Phase 0. Treat Indian-specific deltas as the load-bearing findings.

A note on Indian VC structure: at seed/Series-A in India, fund teams are *small* (5–25 people total at firms like Blume, Stellaris, 3one4, Kalaari; 1–3 at boutiques like 100X.VC, Pi, Together's earlier funds). Most have 1–3 analysts/associates per investment team. Compensation is ₹10–70L base ([salaries source](../../brain/sources/2026-05-31-india-vc-analyst-salaries.md)); fully-loaded cost ~₹15L–1.1Cr ($18K–$130K). This is materially *cheaper* than US analysts ($150K–$250K loaded), so the cost-displacement argument is weaker per-seat in India — but offset by fund sizes being smaller, so the *share of opex* is comparable.

---

## Stage 1 — Sourcing (inbound + outbound + network)

**Activity.** At Blume scale: ~3,500 pitches/year, of which 1/6–1/5 are warm referrals ([Sajith one-year](../../brain/sources/2026-05-31-sajith-pai-reflections-one-year.md)). Total Indian VC market: 1,270 deals closed in 2024 ([Bain](../../brain/sources/2026-05-31-bain-india-vc-report-2025.md)), implying ~60K–250K pitches processed across the market depending on funnel constant. Sources of inbound: founder cold emails, LinkedIn DMs, WhatsApp, warm intros from operators/angels/portfolio CEOs. Twitter/X plays a smaller role in India than US.

**Time-cost.** Cold pitches: 1–5 min triage. Referrals: 15–20 min + reply mail. Pipeline review cadence (per Evertrace benchmark) should be weekly; unclear how strictly Indian funds follow this.

**Tooling penetration in India.**
- **CRM:** Affinity, Attio, Notion, Taghash are the four named anchors ([IndianVCs stack](../../brain/sources/2026-05-31-indian-vc-tech-stack.md)). Taghash is the only India-built. Blume, Kalaari, A91 are public Taghash customers ([Taghash](../../brain/sources/2026-05-31-taghash-india-vc-os.md)). Many smaller Indian funds run on Notion or Airtable.
- **Sourcing data:** Tracxn dominates; Crunchbase + LinkedIn Sales Nav supplement; Harmonic and Evertrace appear in stack catalogues but India penetration unverified. Tracxn pricing is a documented friction for smaller funds ([Tracxn source](../../brain/sources/2026-05-31-tracxn-india.md)).
- **Signal layer:** Effectively absent in India. Evertrace, Harmonic operate globally but no India-specialised pre-announcement founder-detection product is documented.

**Pain.** WhatsApp/email inbound is unmanageable for senior staff ("at least 60–70 mails piled up" after meeting days, [Sajith one-year](../../brain/sources/2026-05-31-sajith-pai-reflections-one-year.md)). The CRM-nobody-uses problem (per [Evertrace](../../brain/sources/2026-05-31-evertrace-vc-dealflow.md)) compounds in tools-light Indian funds. Cold-pitch triage at 1–5 minutes per pitch is the most compressible single activity in the entire associate workflow.

**Where pain concentrates:** at the associate / analyst level, not the partner level. Analysts run the inbound triage gates; partners only see the survivors.

---

## Stage 2 — Screening / first pass

**Activity.** Read deck (5–10 min), classify thesis fit, founder graph lookup, decide: pass / meet / shortlist. 100X.VC published funnel: 4,785 pitches → 458 shortlisted → 10 funded ([100X.VC entity](../../brain/entities/funds/100x-vc.md)), a 9.6% shortlist rate. Blume's cold-pass rate is implicitly higher than 80% (1–5 min triage = mostly pass).

**Time-cost.** Aggregate associate time: dominant share of week for a sub-MBA analyst at a high-throughput fund. No published Indian per-week breakdown exists — this is a research gap.

**Tooling penetration in India.**
- Deck parsing: ad hoc Claude / ChatGPT usage ([IndianVCs stack](../../brain/sources/2026-05-31-indian-vc-tech-stack.md) names Claude as the leading memo tool). No India-specific deck-parser product is documented.
- Founder graph: LinkedIn + LinkedIn Sales Navigator. Harmonic, Evertrace globally but India coverage weak.
- Thesis-fit scoring: not productised in India.

**Pain.** Repetitive, low-judgment work that consumes the role's most-junior staff. Direct line of sight to "this is what AI does instantly." Bessemer's US benchmark: 234 hours/analyst/year reclaimed via AI ([memo source](../../brain/sources/2026-05-31-india-vc-ai-memo-claude.md)). No equivalent Indian benchmark published — likely smaller absolute number but similar relative share.

**Where pain concentrates:** analyst-level repetition; partner-level frustration with "why didn't you screen this better."

---

## Stage 3 — Market research / market mapping

**Activity.** For each shortlisted deal: industry overview, TAM/SAM/SOM sketch, competitor landscape, customer-segment sizing, regulatory notes (FEMA, sector-specific). 1–3 days of work per deal at a tier-1 Indian fund; sometimes outsourced to consultancies (RedSeer, 1Lattice) — both named in IndianVCs.com stack ([source](../../brain/sources/2026-05-31-indian-vc-tech-stack.md)).

**Tooling penetration in India.**
- **Research vendors:** RedSeer, 1Lattice, Kavi Research, Praxis, GLG, AlphaSense, Statista — heavy use at tier-1 funds; less so at boutiques.
- **AI:** Perplexity (cited research), Claude (long-context synthesis), ChatGPT (general). DeepSeek and Gemini also in stack catalogue. No India-grounded market-research AI product documented.
- **News/feeds:** Inc42, YourStory, Entrackr, The Ken, The Morning Context, VCCircle — heavy daily use.

**Pain.** India-specific data is fragmented. RedSeer reports cost ₹5L–25L per study. Free LLMs hallucinate Indian market data (sector sizes, customer counts) more than US data because training-data Indian coverage is thinner. The 3000+ Indian startup dataset becomes meaningful here as a hallucination corrective and a comp source. MCA/ROC public filings exist but no clean AI-grounded India-specific research product wraps them.

**Where pain concentrates:** associate / pre-MBA, with QA pain landing on partners who catch hallucinations late.

---

## Stage 4 — Comp pull / valuation comps

**Activity.** Find similar Indian companies at similar stages with disclosed valuations. Pull funding history, post-money, revenue multiples if known. Used to anchor the term-sheet conversation and pre-commit the IC mentally on price.

**Tooling penetration in India.**
- Tracxn, VCCEdge, Venture Intelligence, Crunchbase. All require paid subscriptions; Indian fund spend on this layer is non-trivial.
- MCA/ROC filings provide cap-table and funding-round legal records but require manual parsing ([MCA source](../../brain/sources/2026-05-31-mca-roc-india-diligence.md)).
- No AI-native India comp-pull product is documented. Tracxn's interface is search-driven; comp synthesis is manual.

**Pain.** Valuation comps in India are *noisier* than US because (a) fewer public benchmarks, (b) ARR/revenue is often not disclosed, (c) iSAFE rounds blur post-money math, (d) cross-border parent/subsidiary structures (Singapore/Delaware hold-cos) hide the real cap table. Pulling clean Indian comps is materially harder than US comps and is one of the activities where the 3000+ Indian-startup dataset has the highest moat-value — if it includes funding-round history.

**Where pain concentrates:** associate-level grunt, partner-level mistrust ("are these comps right?").

---

## Stage 5 — Founder evaluation prep + meetings

**Activity.** Founder background research (LinkedIn, Twitter/X, prior companies, press), reference-call list assembly, prep questions, meeting transcription + summary, write-up.

**Tooling penetration in India.**
- LinkedIn / Twitter / Inc42 / Entrackr for backgrounding — manual.
- Transcription: Granola, Fellow, Otter — emerging adoption; not benchmarked in India.
- Reference calls: India's smaller, denser network means warm reference paths are usually *easier* than US (BITS / IIT / IIM clusters), but call rigor is often lower.

**Pain.** Disproportionately *partner* time at smaller Indian funds because the partner does the meeting directly. AI compresses prep and write-up; the call itself is irreducibly human (Phase 0 finding holds).

**Where pain concentrates:** the partner's time — but partners delegate prep to associates, so it's an associate-pain too.

---

## Stage 6 — Memo drafting

**Activity.** IC memo. Format: ~3,000 words global standard ([Phase 0 memo workflow](../../brain/sources/2026-05-31-vc-investment-memo-workflow.md)). At Indian seed funds, often shorter (1,500–2,500 words) and sometimes replaced by a decision template for iSAFE / convertible rounds at firms like 100X.VC. At Series A, full IC memo is standard. Sections: thesis, team, market, product, traction, comp/valuation, risks, asks.

**Tooling penetration in India.**
- **Claude is named as the leading memo-drafting tool** in the IndianVCs.com stack catalogue ([source](../../brain/sources/2026-05-31-indian-vc-tech-stack.md)). ChatGPT for templated playbook GPTs. No India-built memo-drafting product. Taghash + MCP can theoretically expose fund-specific data to Claude for memo grounding ([Taghash MCP](../../brain/sources/2026-05-31-taghash-india-vc-os.md)).
- **Indian penetration rate:** unmeasured. US benchmark is 85% of dealmakers using AI for daily tasks (Affinity 2025, [memo source](../../brain/sources/2026-05-31-india-vc-ai-memo-claude.md)); Indian rate is anecdotally lower at smaller funds but unverified.

**Pain.** Templated sections (market overview, competitive landscape, financials, team) consume associate days. Distinctive sections (why-we-win, risks-I'm-carrying) are partner-time. AI compresses the former, not the latter — and the partnership-political function of the memo (vote procurement, conviction signaling) is irreducible.

**Where pain concentrates:** associate writing time, partner editing time, partner frustration when AI-drafted sections sound generic.

---

## Stage 7 — IC presentation + decision

**Activity.** Live partner debate; conviction-statement; vote. Per Phase 0, mostly unmoved by AI — political and social, not analytic. Indian funds run smaller partnerships (often 2–4 partners at seed/A), making IC less ritualised than US tier-1 firms.

**Tooling penetration:** none specific to IC.

**Pain:** not a wedge candidate.

---

## Stage 8 — Post-IC: term sheet, diligence, close

**Activity.** Term-sheet negotiation, deeper diligence (legal, financial, customer references), close. Largely lawyer + partner work. Associates do data-room organisation and reference-call write-ups.

**Tooling penetration in India.** Legal diligence is heavily outsourced (Cyril Amarchand, Trilegal, INDUS Law, AZB). Probe42 / Credhive for MCA/ROC layer ([MCA source](../../brain/sources/2026-05-31-mca-roc-india-diligence.md)). No India-specific AI-native diligence tool documented.

**Pain.** Not the highest-leverage AI opportunity; legal cost is the dominant line.

---

## Stage 9 — Portfolio support (post-close)

**Activity.** Per Blume hiring commentary ([source](../../brain/sources/2026-05-31-blume-hiring-analysts.md)): portfolio GTM playbooks, founder-advisor networks, enterprise relationship management (CVCs, System Integrators, GCCs). At Indian funds, this is a meaningful share of associate time — the Indian operator-led model (Stellaris, Blume) makes platform-support an analyst-grade activity, not just a senior-partner one.

**Tooling penetration:** ad hoc, Notion-based.

**Note:** this is the *other* transformative wedge from Phase 0 (portfolio-support transformation). Out of scope for this artifact except to note Indian associates touch it, so the wedge boundary is not clean.

---

## Cross-cutting findings

### A. The Indian tech stack is real but workflow-shallow

Roughly 90+ tools are catalogued for Indian VC use ([IndianVCs stack](../../brain/sources/2026-05-31-indian-vc-tech-stack.md)). India-built tools: **Taghash** (CRM + portfolio + LP, 60+ fund customers), **Tracxn** (data, public co.), **Venture Intelligence** (data), **Sanchi Connect** (deeptech sourcing). Everything else is imported — Affinity, Attio, Notion, Crunchbase, Harmonic, Evertrace, Claude, ChatGPT, Perplexity. The workflow layer between "raw data" and "decision" is *not* productised for the Indian associate role specifically.

### B. AI is being adopted as a layer, not a product

Per the IndianVCs.com stack editorial: "AI now sits as a layer across the stack, not a separate beat." Claude leads for memo drafting; ChatGPT for playbook GPTs; Perplexity for cited research. Indian funds are *using* AI; they are not *buying India-built AI-for-VC products* (because none exist yet at productised scale). Taghash MCP is the closest — and it is plumbing for someone else's AI, not an AI product itself.

### C. The 3000+ Indian-startup dataset has highest moat-value at Stages 3 (market research grounding), 4 (comp pull), and 2 (screening priors)

- **Stage 4 (comp pull):** Public Indian comps are sparse and noisy. A private dataset of 3000+ companies with funding history *materially improves* comp-pull quality. This is the strongest single moat-leverage point in the workflow.
- **Stage 3 (market research):** Indian market-research grounding for LLMs is a known weakness. A private corpus that conditions LLM output reduces hallucination in Indian-specific queries.
- **Stage 2 (screening):** Priors from the dataset (sector base rates, founder archetypes, funding-stage progression) become screening features.

The dataset is low-moat-value at Stages 5 (founder calls), 7 (IC), 8 (legal close), 9 (portfolio support).

### D. India-specific structural pain that US tools don't address

1. **Cross-border cap tables.** Singapore / Delaware flip structures hide real cap-table state from US tools. An India-grounded workflow product can model this natively.
2. **MCA / ROC filings.** Richer public-records layer than US for private companies. Underexploited.
3. **Vernacular founder content.** Hindi-language pitches, regional press coverage. No tool indexes this for sourcing/diligence.
4. **iSAFE-driven seed structure.** Round mechanics differ from US SAFE; comp-pull and term-sheet drafting have India-specific quirks.
5. **WhatsApp as primary inbound channel.** Sajith Pai's writeups make this explicit. No CRM cleanly captures WhatsApp inbound.

### E. Where the workflow is least systematised (and therefore most attackable)

In descending order of compressibility:
1. **Cold-pitch triage (Stage 1 → 2).** 1–5 min per pitch × 3,500 pitches/yr per mid-size fund = ~80–280 hours/yr per fund of pure triage. Highest ROI of AI substitution.
2. **Comp pull (Stage 4).** India-comp pain is structural; the 3000+ dataset directly compounds.
3. **Memo drafting templated sections (Stage 6).** Claude already does this anecdotally; no India-grounded productised version.
4. **Market-research synthesis (Stage 3).** RedSeer at ₹5–25L/study is the displaceable cost.
5. **Inbound channel unification (Stage 1).** WhatsApp + email + LinkedIn DM into a single triaged pipeline.

## Contradictions

- **74% of Indian VCs prioritise AI-first startups** ([Taghash survey](../../brain/sources/2026-05-31-taghash-indian-vc-survey.md)) — *but* the same survey is silent on internal AI tooling adoption. Indian VCs are bullish on AI-as-investment-thesis and quieter on AI-as-internal-workflow. Reconciling: "we invest in AI" is brand-positive; "we run on AI" is undermarketed because most still don't.
- **Blume is a Taghash customer** ([Taghash source](../../brain/sources/2026-05-31-taghash-india-vc-os.md)) — *but* Sajith Pai's published personal stack doesn't mention Taghash or any CRM ([Sajith five-year](../../brain/sources/2026-05-31-sajith-pai-five-years.md)). Reconciling: firm-level tooling and individual-partner workflow are different layers; partners run on email + calendar + Apple Notes even when the firm runs on Taghash. This is the CRM-nobody-uses pattern from [Evertrace](../../brain/sources/2026-05-31-evertrace-vc-dealflow.md).

## Open questions

1. What is the *actual* AI-tool penetration rate at Indian funds for memo drafting, comp pull, market research? Anecdotal only — no published Indian benchmark equivalent to Bessemer's 234-hours-saved.
2. How often do Indian seed funds skip the heavy IC memo for iSAFE rounds? If "often," memo-drafting wedge value-prop shrinks at seed end.
3. What's the schema of AIVC's 3000+ dataset? Comp-pull moat-value depends on whether funding-round history is included.
4. How many of the ~150–250 active Indian VC firms have an associate/analyst seat at all? If <100, the addressable seat-replacement TAM is meaningfully smaller than US.

## Sources

See frontmatter. Linked entities: [[blume-ventures]], [[100x-vc]], [[kalaari-capital]], [[a91-partners]], [[stellaris-venture-partners]], [[taghash]], [[tracxn]], [[sanchi-connect]].
