# PRD — AI Study Companion for JEE (working title: "Saarthi")

**Date:** 2026-04-18
**Tier:** T2 / S2
**Status:** Draft v1
**Owner:** founder (solo)
**Related docs:** [research](research.md) · [plan](plan.md) · [questions](questions.md)

---

## One-liner

A mobile-first Hinglish AI tutor for JEE droppers in tier-2/3 cities that unsticks problems in under 10 seconds and tells the student what to study tomorrow — at 1/50th the cost of a Kota coaching class.

---

## Problem statement

Every year ~15 lakh Indian students sit JEE; ~98% don't get the rank they need [India Today](https://www.indiatoday.in/education-today/news/story/jee-main-2025-registration-numbers-surge-to-all-time-high-with-13-lakh-applicants-2639594-2024-11-25). The ~2–3 lakh who take a gap year ("droppers") in tier-2/3 cities face a brutal choice: move to Kota at ₹3–5 lakh [The Diplomat](https://thediplomat.com/2024/02/student-suicides-in-kotas-coaching-factories-point-to-indias-broken-education-system/) with documented mental-health risks, or self-study from home using a mix of YouTube, Telegram groups, and coaching PDFs — getting stuck nightly with no one to ask. Existing online options (PhysicsWallah, Unacademy, Allen Digital) are video-lecture or live-class businesses that don't personalize; newer AI attempts (Embibe, Arivihan) are either unfocused or narrowly distributed. The re-engagement cost of "give up at 10pm because I'm stuck" is measurable in 2-year outcomes — ranks and seats lost to untutored frustration.

---

## Target user

**Segment:** Indian tier-2/3 city JEE droppers (second attempt), ages 17–19, self-studying from home, smartphone-primary (mid-range Android, ₹10–20k), comfortable in Hinglish, discover tools via r/JEE + Telegram JEE groups + YouTube micro-creators. Household spending ₹10k–50k/year on prep materials; can stretch to ₹299/mo if parents see progress.

**Persona — "Rahul the dropper in Patna":** 18, scored 85 percentile in JEE Main 2026, didn't clear Advanced, taking a gap year at home. Father is a schoolteacher; family can't afford Kota. Currently studies from Cengage books + free PhysicsWallah YouTube + a Telegram group with 12k members. Pain trigger: gets stuck on a Rotational Dynamics problem at 10:45pm, scrolls r/JEE for 20 minutes looking for a similar problem, gives up, lies in bed feeling behind. Wakes up the next morning without a plan.

**Adjacent segment (watch, don't build for):** Tier-2/3 Class 12 students in the final 6 months of prep; Kota-enrolled students looking for a 24×7 supplement. Both matter for year-2 expansion; not MVP.

---

## Jobs-to-be-done (top 3, ranked)

1. **Primary (MVP target).** When I'm stuck on a problem at 10pm and nobody's online to help, I want a step-by-step Hinglish explanation that teaches me why, not just shows the answer — plus a clear "here's what to do tomorrow" — so I can keep progressing and not lose the hour (and not lose tomorrow).
2. When I finish my daily self-study, I want to see which chapters I'm actually weak in (across 2 weeks of data), so I know what to prioritize in my next mock.
3. When my parents ask "is this working?" at the end of the week, I want to show them a simple summary that proves effort + progress, so they keep paying for it.

---

## Success metrics

### North Star
**Weekly problems solved with full explanation per active paid student.** (A "problem solved" = student asked a doubt, got a response, and marked "got it" or moved on to a next problem within 10 minutes.) This captures both engagement and value delivered; vanity metrics like DAU don't distinguish a student who used the app for 20 seconds from one who studied for 2 hours.

### Leading (input, influence now)
- **D1 activation rate** = % of signups who ask and complete 1 doubt within 24h of signup. Target: 60%+.
- **Free-to-paid conversion at day 14** = % of free users who upgrade within 14 days of signup. Target: 8%+.
- **Hinglish explanation rating** = blind student rating of AI explanations (thumbs up/down or 1–5). Target: 4.2/5 average.

### Lagging (output, measured over time)
- **Week-4 retention** = % of paid users active in week 4 of their subscription. Target: 45%+ (MVP), 55%+ (v1).
- **MRR** — tracked monthly. Target: ₹1L (month 6), ₹5L (month 12).
- **Referral rate** = % of new signups coming from existing-user referral codes. Target: 20% by v1.

### Counter-metrics (must not get worse)
- **LLM cost per paid user** ≤ ₹80/month (at ₹299 ARPU keeps gross margin >70%).
- **Hallucination rate on past-paper benchmark** ≤ 3% (measured weekly on a 100-problem test set).
- **Parent NPS** must stay ≥ 30.

### Targets
- **End of MVP phase (week 10):** 50 beta signups, 20 paid, 15 active in week 4, D1 activation ≥50%.
- **End of v1 (month 6):** 500 paid, ₹1L MRR, week-4 retention ≥45%, 20% referral signups.

---

## Solution shape

**Not a design spec — this is the shape, not the details.**

### Core user flow

1. Student opens the app at 10pm, stuck on a problem from a Cengage book.
2. Taps "ask a doubt" → snaps a photo of the problem OR types/pastes it.
3. AI returns a step-by-step Hinglish explanation in <10 seconds with intermediate checkpoints ("samjha? yahan tak theek hai?").
4. Student marks "got it" or asks a follow-up. Follow-ups are free-form ("is step 3 mein tangent ka formula kyun use kiya?").
5. AI logs this doubt against the chapter/subtopic, updates student's weak-area profile.
6. Next morning: app shows "today's plan" — 3 problems + 1 concept revision, tuned to last 7 days of weak areas.

### Key capabilities (MVP)

- **Photo/text doubt input** — mobile camera primary; OCR handles printed textbook problems.
- **Hinglish step-by-step explanation** — LLM with a carefully engineered Hinglish system prompt and JEE-specific scaffolding (symbolic math via SymPy fallback for numeric reliability).
- **Weak-area tracking** — every doubt tagged to JEE syllabus subtopic; accumulates student profile.
- **Daily adaptive plan** — 3 problems + 1 concept, generated daily from weak-area profile + days-to-exam.
- **WhatsApp weekly parent summary** — auto-generated "Rahul practiced 42 problems this week, weak in Rotational Dynamics" message, sent Sunday evening.

### Shaping constraints

- **Latency:** doubt response start within 3s, full response within 10s. Beyond this, students abandon.
- **Mobile data efficiency:** assume 4G on ₹20/day plans. Compress images aggressively; text responses preferred over video.
- **Mid-range Android:** works on 2GB RAM phones. No fancy animations. React Native / Flutter over heavy web.
- **LLM cost cap:** ≤ ₹80/paid-user-month (achievable at ₹299 ARPU with 70%+ gross margin).
- **Hinglish-first, English fallback:** never full Hindi (math notation breaks); never full English (alienates tier-2/3).

---

## Scope and non-goals

### In scope for MVP

- Photo + text doubt solver (Hinglish output)
- Weak-area tracker (tagged to JEE syllabus)
- Daily adaptive 3-problem plan
- Parent WhatsApp weekly summary
- Freemium (10 doubts/day free; unlimited + plan at ₹299/mo)
- UPI payment (via Razorpay/Cashfree) — no card forms

### Non-goals (explicit — do NOT do these in v1)

> _This is the most important section of the PRD. Bad PRDs die because they don't have this._

- **No video lectures.** Reason: PW/Unacademy own this; it's a content-library arms race we can't win and it doesn't solve the "stuck at 10pm" job.
- **No live classes.** Reason: scheduling destroys the "24×7" value prop; we're not a coaching class.
- **No human tutor marketplace.** Reason: different business (two-sided, ops-heavy); destroys AI cost economics.
- **No NEET / UPSC / CUET in year 1.** Reason: dilutes focus; JEE beachhead hasn't been proven.
- **No Class 11 early-stage learners in year 1.** Reason: 2-year feedback loop is too slow for validation; beachhead is droppers where outcome is measurable in 9 months.
- **No desktop/web app in MVP.** Reason: target user studies on phone; desktop is a nice-to-have, not the pain point.
- **No Tamil/Telugu/Bengali/Marathi languages in MVP.** Reason: Hinglish covers 60%+ of JEE reachable audience; other Indian languages are v2 expansion.
- **No offline mode in MVP.** Reason: doubt-solving is inherently online (LLM calls); tier-2/3 data is cheap enough.
- **No "replace coaching classes" marketing positioning.** Reason: alienates parents who still want coaching; position as "supplement" not "replacement."

---

## Competitive positioning

We win against **PhysicsWallah / Unacademy** by being the first AI-personalized product in a category they've optimized for cheap video — PW can't copy AI-tutor quality in under 2 quarters without cannibalizing their course sales. We win against **Allen / coaching classes** by being 1/50th the price and available 24×7 for the dropper segment they structurally can't serve online. We win against **Embibe / Arivihan** by owning a sharper wedge (Hinglish + dropper + ₹299 + WhatsApp parent loop) and moving faster than either — Embibe is unfocused, Arivihan is geo-narrow. We beat **YouTube + Telegram** by turning "stuck for 20 minutes → give up" into "stuck for 20 seconds → unstuck." The wedge thesis (see `research.md` §4) is Hinglish-first + dropper-first + WhatsApp-parent-loop.

---

## Assumptions

> _Things we're treating as true to move forward. Load-bearing assumptions are flagged `[load-bearing]`._

- Tier-2/3 dropper families are willing to pay ₹299/mo. `[load-bearing]` — must validate with 10 paid beta families before scaling.
- LLMs (Claude 4 / GPT-4o class + SymPy hybrid) solve JEE Main problems at >95% accuracy and JEE Advanced at >80%. `[load-bearing]` — must benchmark on 100 past-paper problems before MVP commit.
- Hinglish system-prompt engineering produces explanations students rate 4.2/5 or higher. `[load-bearing]`
- We can seed ~500 early users via r/JEE + Telegram + 3 YouTube micro-creator partnerships with zero paid acquisition.
- WhatsApp Business API approval is obtainable within 4 weeks.
- Parents will convert to paid when shown a weekly WhatsApp progress summary.

---

## Open questions

| Question | Why it matters | Owner | Resolve by |
|---|---|---|---|
| Which 5 YouTube micro-creators (50k–200k subs) will partner at MVP launch? | Distribution = 80% of the game | founder | week 2 |
| What's LLM accuracy on JEE Advanced physics (mechanics + modern)? | If <80% on Advanced, need symbolic fallback or narrow positioning to Main | founder | week 2 (benchmark) |
| Is WhatsApp Business API approval feasible in 4 weeks for a solo founder? | Parent loop depends on it | founder | week 3 |
| Can we cache common doubts to drive LLM cost <₹50/user-month? | Margin protection | founder | week 6 (alpha data) |
| What's the real-world Hinglish rating with 10 beta students? | Load-bearing on primary JTBD | founder | week 5 |

---

## Risks

| Risk | Lkd | Impact | Early signal | Mitigation |
|---|---|---|---|---|
| LLM accuracy on JEE Advanced <80% | M | H | Benchmark fails in week 2 | Narrow positioning to JEE Main-first; add SymPy symbolic fallback for math; hold Advanced for v1 |
| Free-to-paid conversion <5% | M | H | <5% of first 100 signups pay by day 14 | Test alternate pricing (₹199 / ₹499 / ₹99 weekly); test paywall position (hard 10-doubt gate vs soft "upgrade for plan") |
| Parents don't see value in WhatsApp summary | M | M | <20% summary open rate | A/B summary format; add progress chart; include specific rank delta estimate |
| PhysicsWallah launches AI tutor | M | H | Public product launch | Double down on Hinglish+dropper focus; PW will ship a generic version; we win by specificity |
| LLM provider rate-limits or de-prioritizes India | L | H | Latency spikes, error rates | Multi-provider fallback (Claude → GPT → open-weight Llama); pre-cache by chapter |
| Founder burnout | M | H | Commit frequency drops, founder sleep <6hr | Pre-commit to hiring contract help by month 3 if MRR hits ₹50k |

---

_Changelog_
- 2026-04-18: initial draft
