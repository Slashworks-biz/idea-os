# PRD Structure

A PRD (Product Requirements Document) is a forcing function for clear thinking, not a delivery artifact. It answers: *what are we building, for whom, why, and how will we know it's working?* — in enough detail that a team could start tomorrow.

## Structure by tier

### T1 — 1-page lean PRD

Keep it under a page. Sections:

1. **One-liner** — what this is, in one sentence
2. **The person + pain** — who it's for and what specifically hurts
3. **The thin slice** — what the first version does (must be a complete end-to-end flow, not a checklist of features)
4. **Done-ness** — what "it works" looks like (one or two measurable things)
5. **Out of scope** — explicitly list what you are NOT doing
6. **Open questions** — what you don't yet know

### T2 — Standard PRD

All T1 sections, plus:

7. **Jobs-to-be-done** — top 3
8. **User segments** — primary segment + one adjacent segment to keep an eye on
9. **Success metrics** — leading and lagging
10. **Solution shape** — user flow and the 3–5 core capabilities (not detailed design)
11. **Risks and assumptions** — what could kill this, what we're betting on
12. **Competitive positioning** — one paragraph: how we win against named competitors

### T3 — Full PRD

All T2 sections, plus:

13. **Context and strategic rationale** — why this, why now, how it fits the broader strategy
14. **Market opportunity** — TAM/SAM/SOM summary pulled from research.md
15. **Non-functional requirements** — performance, security, compliance, accessibility, privacy, availability
16. **Decision log** — every significant decision made, with date, context, alternatives considered, decision, rationale
17. **Risks register** — each risk with likelihood, impact, and mitigation
18. **Dependencies** — teams, vendors, platforms, approvals needed
19. **Launch criteria and rollback plan** — what must be true to ship; what happens if it fails

## Section-by-section quality bar

### Problem statement
- One paragraph. Specific. Falsifiable.
- Bad: "Scheduling is hard for small teams."
- Good: "Small design agencies (5–15 people) lose 6–8 hours a week per PM reconciling project timelines across Asana, Slack, and email — because none of the three systems knows the others exist."

### Target user
- Segment *and* persona. Segment is the group, persona is a representative person with a name and context.
- Include what triggers them to look for a solution ("trigger events").

### Jobs-to-be-done
- Top 3, ranked.
- Each written as: *When [situation], I want to [motivation], so I can [outcome].*
- One of them is the MVP job. Call it out.

### Success metrics
- Separate **leading** (what you can influence now) from **lagging** (what you're ultimately trying to move).
- Separate **input** metrics (activity) from **output** metrics (outcomes).
- Define the metric precisely — "active user" is not a metric until you define activity, window, and unit.
- Include at least one **counter-metric** — what should NOT get worse.
- See `references/metrics-framework.md` for the full treatment.

### Solution shape
- NOT a design spec.
- Core user flow in steps.
- 3–5 key capabilities the solution must include.
- Key constraints that shape the solution (platform, integration, latency, cost).

### Scope and non-goals
- **Non-goals is mandatory.** A PRD without non-goals is a wishlist.
- Non-goals should include things that are *tempting* to include. "No AI chatbot in v1." "No mobile app in v1." "No team/collaboration in v1."
- Add a short reason for each non-goal so future-you remembers why.

### Open questions + assumptions
- Open questions: things you don't know yet that could change the build. Attach an owner and a deadline.
- Assumptions: things you're treating as true to move forward. If an assumption is load-bearing, flag it.

### Risks
- Not generic ("users might not like it").
- Name the specific failure mode and the early signal that would tell you it's happening.
- "Risk: dog trainers won't log sessions on mobile because they're holding a leash. Early signal: <30% of sessions logged within 24h in first 2 weeks of beta."

## Anti-patterns

- **Feature list disguised as a PRD.** Features without problem + user + metrics = wishlist.
- **Adjective-heavy writing.** "Seamless, delightful, intuitive." Cut. Use verbs and specifics.
- **Unfalsifiable success metrics.** "Users love it" is not a metric.
- **No non-goals.** Lazy. Reject.
- **Solution before problem.** If the "what" comes before the "why," rewrite.
- **Edge cases in the happy path.** Keep the core flow clean; park edge cases in their own section.
- **Meeting-notes tone.** PRDs should read like technical writing, not Slack threads.

## Length

- T1 PRD: 200–500 words total.
- T2 PRD: 800–1500 words.
- T3 PRD: 1500–3500 words; longer if it's genuinely a multi-quarter effort.

Longer is not better. A tight T3 beats a sprawling one every time.

## Voice

- Third person, present tense. "The product does X." Not "we will build X" or "you will be able to."
- One declarative sentence per idea. Shorter paragraphs. Bullets where appropriate but not for everything.
- No hedging ("kind of," "sort of," "it might be"). If it might be, make it an open question.
