# MVP Slicing

An MVP is the smallest thing that delivers an end-to-end user outcome — not a feature checklist, not a "minimum feature set," and definitely not "v0.1 of the full product."

## The one rule

**Slice vertically, not horizontally.**

Horizontal slice (wrong): "We'll build the database, then the API, then the UI, then ship."

Vertical slice (right): "We'll build the one flow — user opens app, captures one session note, retrieves it later — and ship that."

The vertical slice teaches you whether the core value resonates. The horizontal slice teaches you nothing until it's all built.

## Walking skeleton

Before building anything, sketch the **walking skeleton**: the thinnest possible end-to-end path through the product. It's ugly. It skips features. It's barely functional. But a user can complete the core job with it.

If you can't describe the walking skeleton in 3 sentences, the MVP is not defined yet.

## MVP vs. v1 vs. target state

Use three named stages to avoid scope creep.

- **MVP** — walking skeleton; one user, one job, end-to-end. The question it answers: *do users want this at all?*
- **v1** — rough product; small set of users actively using it; monetization hypothesis in play. The question: *is this becoming a habit / generating revenue / spreading by word of mouth?*
- **Target state** — the 2–3 year vision. What this looks like when it's working. Written in present tense ("users open this daily to...").

Define all three. Build MVP first.

## Prioritization frameworks

Use these to rank scope inside each phase. Pick one — don't run all three.

### RICE

Score = (Reach × Impact × Confidence) / Effort.

- **Reach** — users affected per time unit
- **Impact** — how much it moves the metric (use a scale: 0.25 / 0.5 / 1 / 2 / 3)
- **Confidence** — how sure you are (as %)
- **Effort** — person-weeks

Good for teams with multiple product bets.

### ICE

Score = Impact × Confidence × Ease (each 1–10).

Simpler than RICE. Good for solo builders and small teams.

### Kano

Classify each feature into:

- **Must-haves** — table stakes; absence causes dissatisfaction
- **Performance** — more is better linearly
- **Delighters** — unexpected; cause disproportionate delight
- **Indifferent** — nobody cares; cut
- **Reverse** — actively disliked by some users

Useful early to kill indifferent features and to find the 1–2 delighters to invest in.

### MoSCoW

Must / Should / Could / Won't. Quick and directional. Not a quantitative method — but the "Won't" column is gold; it's basically the non-goals list.

## How to define the MVP — step-by-step

1. Restate the top JTBD.
2. Ask: *what is the thinnest slice of functionality that lets one user complete this job end-to-end?*
3. Write the user flow in 5–7 steps. If it's more, the slice is too fat.
4. For each step, note the simplest possible implementation — a Google Form, a manual process, a single hard-coded button are all fair game.
5. Write success criteria: how will you know the slice worked? ("N users completed the flow in one sitting without help; X% of them came back within 7 days.")
6. Write kill criteria: what would tell you to stop or pivot? (See below.)

## Kill criteria

Every phase must have a **kill criterion** — a pre-registered signal that says "stop." Without one, sunk cost will keep the project alive past usefulness.

Format: *"If by [date] we haven't seen [metric threshold], we [pivot to X / kill / narrow the target segment]."*

Examples:
- "If by week 4 of beta <20% of signups complete the core flow, we pivot the onboarding approach."
- "If by month 3 of v1 we haven't reached $500 MRR, we narrow the ICP and rerun go-to-market."
- "If by end of Q1 the top-3 JTBD for our beachhead isn't 'capturing session notes quickly,' the positioning is wrong."

Kill criteria feel painful to write. Write them anyway. The point is to set the bar before hope distorts the judgment.

## Pre-MVP validation: the concierge path

Before building software, consider whether a **concierge MVP** (or "Wizard of Oz") can validate the core demand with zero code. You act as the backend yourself.

Examples:
- Before building an AI study app: run a Telegram bot where you personally answer student questions and a helper transcribes. Are students coming back? Paying?
- Before building an automated outreach tool: send outreach manually for a handful of customers. Does the output they get drive retention?
- Before building a marketplace: match buyers and sellers by email or text. Do they transact?

The test: can you validate **willingness to pay + repeat use** with a manual process that takes <1 week to set up? If yes, do that first. Two weeks of concierge invariably tells you more than 8 weeks of building.

A concierge MVP is valid only if it produces the same *outcome* the real product would — not a teaser. If users pay and come back for the concierge version, demand is real. If they don't, no amount of polish saves the built version.

Skip concierge when: the outcome genuinely requires automation to deliver (latency-critical, privacy-critical, high-volume) — but be honest about whether "requires automation" is true or just a preference to start coding.

## Common MVP traps

- **MVP that requires a launch** — if you need to "launch" the MVP, it's too big. MVPs go to 10 people, not the public.
- **Manual backend masked as automation (concierge MVP)** — this is fine! It's a valid technique. Just don't confuse the concierge MVP with the final product.
- **Scope that exceeds 2–4 weeks of build** — if MVP takes 2 months, it's a v1, not an MVP.
- **No measurement plan** — if you can't tell whether the MVP worked, what was the point?
- **MVP = prototype** — no. MVP goes in front of real users. A prototype is a research tool.
