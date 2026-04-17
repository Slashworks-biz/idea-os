# PRD — {{idea title}}

**Date:** {{YYYY-MM-DD}}
**Tier:** {{T1/T2/T3}} · {{S1/S2/S3}}
**Status:** Draft
**Owner:** {{name}}
**Currency:** {{target-market currency — use consistently}}
**Related docs:** [research](research.md) · [plan](plan.md) · [questions](questions.md)

---

## One-liner

{{What this is, in one sentence. Readable by a non-expert.}}

---

## Problem statement

{{One paragraph. Specific. Falsifiable. Includes who, what hurts, what it costs them, and how they solve it today.}}

---

## Target user

**Segment:** {{primary segment — firmographic + behavioral}}
**Persona:** {{named representative — role, context, daily routine, triggers that make them look for a solution}}
**Adjacent segment (watch):** {{segment we're not building for but keeping an eye on}}

---

## Jobs-to-be-done (top 3, ranked)

1. **Primary (MVP target).** When {{situation}}, I want to {{motivation}}, so I can {{outcome}}.
2. When {{situation}}, I want to {{motivation}}, so I can {{outcome}}.
3. When {{situation}}, I want to {{motivation}}, so I can {{outcome}}.

---

## Success metrics

### North Star
**{{metric}}** — {{definition and why this captures value delivered}}

### Leading (input, influence now)
- {{metric}} — {{precise definition and capture method}}
- {{metric}} — {{...}}

### Lagging (output, measured over time)
- {{metric}} — {{...}}
- {{metric}} — {{...}}

### Counter-metrics (must not get worse)
- {{metric}} — {{...}}

### Targets
- By end of MVP phase: {{metric = value}}
- By end of v1: {{metric = value}}

---

## Solution shape

**Not a design spec — this is the shape, not the details.**

### Core user flow

1. {{step}}
2. {{step}}
3. {{step}}
4. {{step}}
5. {{step}}

### Key capabilities

- {{capability}} — why it's in the MVP
- {{capability}} — why it's in the MVP
- {{capability}} — why it's in the MVP

### Shaping constraints

- {{constraint — platform, integration, latency, cost}}
- {{constraint}}

---

## Scope and non-goals

### In scope for MVP
- {{item}}
- {{item}}
- {{item}}

### Non-goals (explicit — do NOT do these in v1)
> _This is the most important section of the PRD. Bad PRDs die because they don't have this._

- **{{non-goal}}** — {{reason}}
- **{{non-goal}}** — {{reason}}
- **{{non-goal}}** — {{reason}}

---

## Competitive positioning

{{One paragraph: how we win against the named competitors in research.md. Reference the wedge thesis.}}

---

## Assumptions

> _Things we're treating as true to move forward. Load-bearing assumptions are flagged `[load-bearing]` — if they turn out false, the plan breaks._

- {{assumption}}
- {{assumption}} `[load-bearing]`
- {{assumption}}

---

## Open questions

| Question | Why it matters | Owner | Resolve by |
|---|---|---|---|
| {{}} | {{}} | {{}} | {{}} |
| {{}} | {{}} | {{}} | {{}} |

---

## Risks

| Risk | Likelihood | Impact | Early signal | Mitigation |
|---|---|---|---|---|
| {{}} | L/M/H | L/M/H | {{}} | {{}} |
| {{}} | L/M/H | L/M/H | {{}} | {{}} |

---

<!-- The block below is REQUIRED for T3, OPTIONAL for T2, OMIT for T1. Delete the HTML comments and the T3-only block entirely if you're writing a T1 or T2 PRD. -->
<!-- T3-only (begin) -->

## Non-functional requirements

- **Performance:** {{}}
- **Security:** {{}}
- **Privacy:** {{}}
- **Accessibility:** {{}}
- **Compliance:** {{}}
- **Availability:** {{}}

## Dependencies

- {{team/vendor/platform/approval needed}}
- {{}}

## Decision log

| Date | Decision | Alternatives | Rationale |
|---|---|---|---|
| {{}} | {{}} | {{}} | {{}} |

## Launch criteria

- {{criterion}}
- {{criterion}}

## Rollback plan

{{how we revert if it fails; what "failure" looks like}}

<!-- T3-only (end) -->

---

_Changelog_
- {{YYYY-MM-DD}}: initial draft
