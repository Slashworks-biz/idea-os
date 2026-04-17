# Market Analysis

Goal: answer "is there a market here, how big, and how do we find it?" — not to impress anyone with big numbers.

## TAM / SAM / SOM

Three nested circles. Be honest at each level and show your method.

- **TAM** (Total Addressable Market) — every human or org that *could* use this if there were no friction. Units: count × price × frequency.
- **SAM** (Serviceable Available Market) — the slice reachable given your geography, language, channel, and product form factor.
- **SOM** (Serviceable Obtainable Market) — the slice you can realistically win in the next 1–3 years. Usually 1–10% of SAM for an early-stage product.

### Two methods — always do both

Running both methods and reconciling them is the sanity check. If the two numbers are >5x apart, one of them is wrong.

**Top-down** (fast, used to sanity-check the category exists):
- Find an analyst report, industry stat, or published number for the overall category.
- Segment down by geography, user type, willingness-to-pay.
- Cite the source and the year.

**Bottom-up** (the one that matters — shows you know your user):
- Number of target users × conversion × ARPU/year = market.
- Example: 50k professional dog trainers in US × 30% plausible adoption × $240/year = $3.6M SAM.
- If you can't fill in these numbers from your own knowledge or research, the market analysis is speculation.

### Reality-check patterns

- If TAM is "$10T global AI market," you're being lazy. Narrow the segment.
- If bottom-up × 10 is bigger than your claimed SAM, your SAM is too small.
- Early-stage SOM rarely exceeds $1–10M in year 1 — even for great ideas. The SOM is used to check that the business math works for the *first* 12 months, not that the idea is "big."

## Segmentation

Describe the market in three dimensions — not just one:

1. **Firmographic / demographic** — for B2B: company size, industry, revenue; for consumer: age, income, geography, life stage
2. **Behavioral** — what they do today, what tools they use, how they discover products, how they buy
3. **Psychographic** — what they value, how they identify themselves, what pain keeps them up

Then pick a **beachhead segment** — narrow enough to dominate in 6 months, specific enough that you can list 10 real names by Friday.

## Growth and trends

Pull three signals, not twenty:

- **Category growth rate** — is this category growing, flat, or declining? Source a number.
- **Adjacent tailwinds** — what adjacent category/tech/behavior is pulling this one forward?
- **Leading indicators** — forum activity, GitHub stars, Reddit subscriber growth, job postings, patent filings, funding announcements

## Timing

Ask: *if this is a good idea, why hasn't it been done, or why didn't it work the last time it was tried?*

Every good idea has a graveyard. Google it. Look at Crunchbase for dead companies in your space. Read a post-mortem. Then state why this time is different.

If you can't find prior attempts, either (a) the idea is novel (rare, be suspicious), or (b) the market is too small, or (c) you haven't searched hard enough.

## Willingness to pay (WTP)

Three ways to probe WTP without a survey:

1. **What do they pay for the current workaround?** (Labor hours × hourly rate, subscription costs for partial solutions, outcomes lost)
2. **What do comparable products charge?** (Use comps with caution — don't anchor too strongly)
3. **Van Westendorp** (formal method, skip for T1) — ask 4 price-sensitivity questions and plot

For B2B, the rule of thumb: price = 10% of value delivered. Quantify the value first.

## Distribution

See [`distribution.md`](distribution.md) — full channel-fit patterns, CAC economics, and first-100-users playbook. The principle: if distribution isn't obvious, the idea is incomplete.

## Output format for `research.md` market section

Short and potent. Three subsections:

1. **Size** — TAM / SAM / SOM with method and source per number
2. **Segments** — 3 segments max; beachhead called out
3. **Trends & timing** — 3–5 bullets with "why now" tied to each
