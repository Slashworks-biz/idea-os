# Metrics Framework

Metrics should answer one question: *is this working?* Pick a small set that forces honest answers. Many metrics = no metrics.

## The one that matters most — North Star Metric

One metric that captures the core value you deliver to users. Properties of a good North Star:

- It moves when you deliver value, not when you do marketing
- It predicts long-term business success
- It's understandable in a sentence

Examples:
- Spotify — hours of music listened
- Airbnb — nights booked
- Figma — multiplayer hours
- A dog-trainer app — sessions logged per active trainer per week

Anti-example:
- Sign-ups — vanity; doesn't capture whether users got value

Define the North Star first. Everything else serves it.

## Input vs. output metrics

- **Output metrics** — what you ultimately want (North Star, revenue, retention)
- **Input metrics** — things you can influence directly this week that roll up to the output

Teams should track inputs daily, outputs weekly. Inputs are what you control; outputs are what you're measured on.

Example:
- Output: weekly active users
- Inputs: landing-page conversion rate, activation rate (new users who complete first session), reactivation emails sent

## Leading vs. lagging

- **Leading** — early signals that predict outcomes (NPS, activation rate, time-to-value)
- **Lagging** — the outcomes themselves (retention, revenue, churn)

Always pair them. Lagging alone tells you too late. Leading alone can be gamed.

## AARRR (Pirate Metrics)

Useful for consumer and self-serve SaaS. Map one metric per stage:

- **Acquisition** — who lands on the product
- **Activation** — who has a good first experience
- **Retention** — who comes back
- **Revenue** — who pays
- **Referral** — who brings others

Define activation precisely — it's the most abused term in product. "Activation = user completed X within Y of signup" with specific X and Y. Example: "logged first session within 48h."

## HEART

Google's framework, strong for UX-driven products:

- **Happiness** — subjective satisfaction (surveys, NPS, CSAT)
- **Engagement** — level of user involvement (session length, frequency)
- **Adoption** — new users starting to use a feature
- **Retention** — users sticking around
- **Task success** — completion rate, time-on-task, error rate

For each: Goal → Signal → Metric. (Don't skip the goal — metrics without goals drift.)

## B2B / SaaS

Core set:
- **MRR / ARR** — recurring revenue
- **Logo churn** — % of customers lost per period
- **Net revenue retention (NRR)** — accounts for expansion + contraction + churn; >100% is healthy
- **Sales cycle length** — days from first contact to signed
- **CAC payback** — months to recover customer acquisition cost
- **Magic number / LTV:CAC** — efficiency ratios

## Marketplace

- **Liquidity** — % of listings that transact in a time window (the marketplace-works-here threshold)
- **Take rate** — cut per transaction
- **Restock rate on supply side** — how often suppliers return
- **Repeat purchase rate on demand side** — how often buyers return
- **Time to first match** — how fast a buyer finds supply

## AI product specifics

Beyond the usual:
- **Accuracy / task success rate** — objectively measured on representative tasks
- **Cost per successful task** — token + infra cost divided by outcomes
- **Latency p50/p95** — user-perceived speed
- **Fallback rate** — how often the AI defers to humans or returns "I don't know"

## Counter-metrics

For every target metric, define a counter-metric. The counter-metric is what should NOT get worse when you move the target.

- Target: activation rate up. Counter: week-4 retention not down.
- Target: sessions per user up. Counter: NPS not down.
- Target: CAC down. Counter: lead quality (activation within 7 days) not down.

Counter-metrics prevent gaming. Always pair them.

## Goals and targets

A target is: *"Move X from A to B by date D."*

Bad: "Increase retention."
Good: "Raise week-4 retention from 18% to 30% by end of Q2."

Set targets that are ambitious but achievable. If you always hit 100%, set them higher. If you always hit 40%, recalibrate.

## Per-phase metrics in plan.md

Each phase in `plan.md` should list:

1. **North Star for this phase** (can shift phase to phase)
2. **Target level at end of phase** (with date)
3. **Leading input metrics** (2–3)
4. **Counter-metrics** (1–2)
5. **Kill criterion threshold** (the floor that triggers pivot or stop)

Keep it to ~5 metrics per phase. More than that is noise.

## Measurement plan

How will you actually measure these? A metric you can't capture is not a metric.

- What system emits the event?
- Who owns the dashboard?
- What's the freshness (real-time, daily, weekly)?
- What's the definition (write it down — definitions drift)?

For MVPs, a Google Sheet + manual tally is fine. Don't let perfect instrumentation block shipping.
