# Research Frameworks

Reach for the framework that fits the question. Do not run all of them. Running too many frameworks produces a deck, not a decision.

## Table of contents

- [JTBD — Jobs to be Done](#jtbd)
- [SWOT — done right](#swot)
- [Porter's Five Forces](#porter)
- [PESTEL](#pestel)
- [Blue Ocean — value curve](#blue-ocean)
- [Wardley mapping (lite)](#wardley)
- [Pain × Frequency × Urgency matrix](#pfu)
- [Why-now analysis](#why-now)

---

<a id="jtbd"></a>
## JTBD — Jobs to be Done

The user doesn't buy a product — they hire it to do a job. The job has three layers:

- **Functional** — the practical outcome ("get from A to B in under 30 minutes")
- **Emotional** — how the user wants to feel ("competent, in control, not anxious")
- **Social** — how the user wants to be seen ("the organized parent")

Write JTBD as: `When [situation], I want to [motivation], so I can [expected outcome].`

Example (for a Notion-for-dog-trainers): *"When I'm planning next week's client sessions, I want to pull each dog's history and training plan in one place, so I can walk into the session prepared without re-reading last week's notes."*

Force rank jobs. The top job is what the MVP delivers. Everything else is scope creep until the top job is nailed.

**Competitor insight from JTBD:** the competitor set expands beyond named companies to include workarounds (spreadsheets, paper, habits). Often the real competitor is "do nothing" or "copy-paste into Google Docs."

<a id="swot"></a>
## SWOT — done right

Most SWOT is useless because it's too generic. A good SWOT entry passes this test:

> Would this entry be different for a different product in the same category? If not, it's useless.

- **Strengths** — internal, specific, asymmetric. Not "we care about users." Yes: "founder spent 8 years as a dog trainer so can build without user research cycle."
- **Weaknesses** — honest. Things that will hurt you if not addressed. "No prior distribution; no email list; no community presence."
- **Opportunities** — external shifts that favor you *now*. Market trends, regulatory changes, platform shifts, tech unlocks. Tie each to a "why now."
- **Threats** — concrete named risks. "Google could ship this as a Gmail side panel in one quarter." Or: "Platform dependency — 80% of target users discover apps via Instagram; algorithm shift kills reach."

Force yourself to write 3–5 entries per quadrant. No filler.

<a id="porter"></a>
## Porter's Five Forces

Use for T3 ideas or any market entry into an established category. Skip for T1.

1. **Competitive rivalry** — how fierce is competition between existing players? (Number of players, differentiation, switching costs, growth rate.)
2. **Supplier power** — can suppliers (APIs, platforms, labor) squeeze you?
3. **Buyer power** — can customers squeeze you on price or terms?
4. **Threat of substitutes** — can a user solve the same job in a fundamentally different way?
5. **Threat of new entrants** — how hard is it for someone else to copy this once you prove it works? (Moats: network effects, data, switching cost, brand, regulation, capital.)

Output: one paragraph per force + a 1-line verdict on whether this market is structurally attractive.

<a id="pestel"></a>
## PESTEL

Use for regulated domains, consumer products with macro exposure, or international plays.

- **Political** — government stability, trade policy relevant to your category
- **Economic** — inflation, rates, consumer spending, B2B budget cycles
- **Social** — demographic shifts, cultural trends, attitudes relevant to your category
- **Technological** — tech unlocks (AI capability, hardware, infra cost)
- **Environmental** — sustainability pressure, climate effects
- **Legal** — regulation in target geographies, liability exposure, IP

Skip forces that don't materially affect the idea. Depth beats coverage.

<a id="blue-ocean"></a>
## Blue Ocean — value curve

Draw a value curve: the key competing factors in the category on the x-axis, level of investment on the y-axis (from low to high). Plot competitors. Then plot your product.

Ask the "four actions":
1. **Eliminate** — which factors the industry takes for granted should be eliminated?
2. **Reduce** — which should be reduced well below the industry standard?
3. **Raise** — which should be raised well above the industry standard?
4. **Create** — which factors should be created that the industry has never offered?

Output: a short paragraph plus a sketch (ASCII table is fine) showing your curve vs competitors.

<a id="wardley"></a>
## Wardley mapping (lite)

For T3 ideas and platform plays. Map the value chain vertically (user need → components), and each component's evolutionary stage horizontally (genesis → custom-built → product → commodity).

Key insight: components that are commodities shouldn't be custom-built. Components that are genesis are where defensible innovation lives. Build custom where it matters, use commodities where it doesn't.

Skip for simpler ideas — it's heavy machinery.

<a id="pfu"></a>
## Pain × Frequency × Urgency matrix

For any idea, rate the pain on three dimensions (1–5 each):

- **Pain** — how much does this hurt? (Mild annoyance = 1; existential = 5)
- **Frequency** — how often does it happen? (Once a year = 1; daily = 5)
- **Urgency** — does it need to be solved now, or can it wait? (Can wait = 1; needs immediate fix = 5)

Score = Pain × Frequency × Urgency. Anything under ~30 (out of 125) is probably not worth a product.

Also note: low-frequency × high-urgency pains (tax season, moving, illness) are good for products too — just the business model differs.

<a id="why-now"></a>
## Why-now analysis

Every durable product has a "why now" — a reason this works in 2025 but didn't in 2020. Force yourself to name it. If you can't, either the idea has been tried (check why it failed) or the timing is wrong.

Categories of "why now" unlocks:
- **Tech unlock** — a new capability became cheap or possible (LLMs, GPUs, WebGPU, edge compute)
- **Platform shift** — distribution moved to a new surface (TikTok, Meta Quest, smart glasses, in-car OS)
- **Regulatory change** — a law opened a market or mandated a behavior (PSD2, GDPR, HIPAA updates)
- **Behavioral shift** — user behavior changed (remote work, AI trust, creator economy)
- **Cost curve** — something got 10x cheaper (storage, bandwidth, compute, LLM tokens)

Write one paragraph: *"This works now because X became possible/cheap/legal/normal in [year], and the incumbents haven't caught up because [reason]."*
