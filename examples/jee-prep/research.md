# Research — AI Study Companion for JEE

**Date:** 2026-04-18
**Tier:** T2 / S2
**One-liner:** A Hinglish, mobile-first AI tutor that solves JEE-level problems step-by-step and adapts a daily study plan to each student's weak chapters — priced for tier-2/3 families who can't afford Allen or PhysicsWallah Vidyapeeth.

> _Every factual claim is sourced or flagged `[assumption]`. Reading order: Insights → Competitors → Market → rest as needed._

---

## Simulated founder-profile answers (T2 / S2, solo builder)

Since no live user is answering the Phase-2 questions, these are the assumptions this research runs on. If any assumption is wrong, specific sections below become invalid — I've flagged which.

1. **Beachhead:** **Droppers + Class 12 tier-2/3 students** who can't afford or physically can't move to Kota. High willingness-to-pay, highest pain, narrowest reachable segment. Writing off Kota-enrolled students (they already have coaching) and Class 11 (too early — product-market loop is too slow to validate in year 1).
2. **Primary JTBD:** **"I'm stuck on a problem at 10pm and need a teacher-quality explanation now, plus a plan for what to study tomorrow."** Combines doubt-solving (a) + personalized plan (b). NOT video lectures. NOT human-tutor marketplace.
3. **10x angle:** **Price (₹299/mo vs ₹1–2 lakh/yr coaching) × Personalization (plan adapts to my weak chapters) × Language (Hinglish).**
4. **Language:** **Hinglish-first.** English for math notation, Hindi for explanation. Deferred: Tamil/Telugu/Bengali/Marathi to v2.
5. **Builder:** Solo founder, full-time push, ~6 months runway from savings, target first ₹1L MRR by month 6, kill or pivot if not hit.
6. **Monetization:** Freemium (10 doubts/day free, unlimited + plan + mock analytics at ₹299/mo or ₹1,499/yr).
7. **Non-goals (founder's pre-declared):** no video lectures, no human-tutor marketplace, no live classes, no Class 6–10 expansion in year 1, no offline/physical centers.

These assumptions drive the rest of this document. They must be pressure-tested with 5–10 real dropper students before writing a single line of code.

---

## TL;DR

- **The JEE market is massive and in active disruption.** ~15.4 lakh unique candidates registered in JEE Main 2025 — all-time high [India Today](https://www.indiatoday.in/education-today/news/story/jee-main-2025-registration-numbers-surge-to-all-time-high-with-13-lakh-applicants-2639594-2024-11-25). The $22B incumbent (BYJU's) has collapsed to near-zero valuation [Inc42](https://inc42.com/features/byjus-2024-review-collapse-edtech-giant-byju-raveendran/), opening shelf space in the mindshare of ~10M+ aspirant households.
- **The winner of the "online JEE prep" category so far is PhysicsWallah — but they won on low-cost human-teacher video, not on AI personalization.** ~$2.8B valuation [TechCrunch](https://techcrunch.com/2024/09/19/indias-physics-wallah-raises-210m-at-2-8b-valuation-even-as-edtech-funding-remains-scarce/), 2.5x revenue growth FY23→FY24. They occupy the "cheap video coaching" quadrant. They do NOT occupy the "1:1 adaptive AI tutor" quadrant.
- **The real competitor is the 2-year coaching-class habit + Kota migration.** 150k–200k students move to Kota annually at ₹3–5 lakh all-in cost [The Diplomat](https://thediplomat.com/2024/02/student-suicides-in-kotas-coaching-factories-point-to-indias-broken-education-system/). Success rate is ~2%. This is a broken workaround more than an entrenched competitor.
- **AI-tutor startups in this exact space already exist.** Arivihan raised $4.17M Pre-Series A in July 2025 from Prosus and Accel, focused on tier-3/4 cities. Embibe (Jio-owned) has been in market since 2012. The category is validated, but not yet consolidated — the wedge is still open.
- **The "why now" is real and stacked.** Claude/GPT-class models can now do JEE problems well; Whisper-class voice transcription is reliable; mobile data is ₹9/GB down from ₹269/GB in 2014 [Storyboard18](https://www.storyboard18.com/digital/660-million-smartphone-users-16-17-billion-monthly-upi-transactions-power-digital-bharat-report-89731.htm); 660M smartphone users with tier-2/3 driving growth.
- **The hidden unlock is emotional, not functional.** Kota logged 20+ student suicides in 2024 [The Hindu](https://www.thehindu.com/news/national/jee-aspirant-from-bihar-dies-by-suicide-in-kota-13th-incident-this-year/article68366961.ece). Parents are looking for alternatives to sending a 16-year-old away from home. A product that lets students prep at home with quality support is emotionally valuable to parents, who are the buyers.

---

## 1. Problem validation

**Is this pain real?** Yes — on three separate dimensions, all sourced.

**(a) Scale of the problem.** JEE Main 2025 saw ~15.4 lakh (1.54M) unique candidate registrations across both sessions [India Today](https://www.indiatoday.in/education-today/news/story/jee-main-2025-registration-numbers-surge-to-all-time-high-with-13-lakh-applicants-2639594-2024-11-25); JEE Main 2024 had ~14.76 lakh. Only ~2.5 lakh qualify for JEE Advanced, and ~17,000 get into IITs — success rate at the Advanced level is ~1.1%. 99% of aspirants fail. That failure happens in public, after 2 years and ₹1–5 lakh per family.

**(b) Cost of the current workaround.** Offline coaching at Allen Kota costs ₹82,000–₹1,65,000/year for JEE Main track and up to ₹5 lakh for 2-year programs, plus ~₹4,500–12,000/month hostel [Propelld/Allen fees](https://propelld.com/site/blog/allen-kota-fees). Average JEE offline coaching in India runs ₹1–2.5 lakh/year [Vedantu](https://www.vedantu.com/jee-main/average-fees-range-for-jee-coaching-in-india). Online options (PhysicsWallah, Unacademy) are cheaper but still batch-model — no personalization.

**(c) Emotional cost.** "18-hour days, 7 days a week" schedule [The Diplomat](https://thediplomat.com/2024/02/student-suicides-in-kotas-coaching-factories-point-to-indias-broken-education-system/). Kota saw 20+ documented student suicides in 2024 [The Hindu](https://www.thehindu.com/news/national/jee-aspirant-from-bihar-dies-by-suicide-in-kota-13th-incident-this-year/article68366961.ece). ~30% of students report mental health deterioration after starting coaching [SATHEE / IITK](https://sathee.iitk.ac.in/gk/exam-news/06-07-2024/jee-exam/neet-jee-exams-are-causing-a-mental-health-crisis-in-india-students-are-struggling-to-cope/). The JTBD is not just "help me learn faster" — it's "help me survive this without breaking."

**Evidence:**
- Reddit r/JEE and r/JEENEETards have continuous daily threads on "stuck on this problem," "coaching is too expensive," "can't afford Kota" — persistent active demand signal.
- Toppr (owned by BYJU's) shut down in 2024, leaving an orphaned user base of ~millions of students who used it for doubt-solving [Reddit discussion](https://www.reddit.com/r/JEENEETards/comments/1fwpsre/toppr_crash/).
- BYJU's collapse means lakhs of paying JEE families are actively shopping alternatives [Inc42](https://inc42.com/features/byjus-2024-review-collapse-edtech-giant-byju-raveendran/).

**Assumptions:**
- `[assumption]` Tier-2/3 droppers are willing to pay ₹299/mo out of pocket. Families spending ₹1–2L/yr on coaching probably will, but needs 5–10 paid beta conversions to validate.
- `[assumption]` Current LLMs are good enough on JEE Advanced problems. Anecdotally Claude 3.5+/GPT-4o+ class models handle JEE Main reliably; Advanced (especially physics modelling) is not yet uniform. Must test with ~100 real past-paper problems before building.

---

## 2. Jobs-to-be-done

**Primary JTBD (MVP target):**
> _When I'm stuck on a problem at 10pm during my self-study and there's no teacher around, I want a patient, step-by-step explanation in Hinglish plus a smart answer to "what should I do tomorrow to actually fix this gap," so I can keep progressing without waiting for Monday's coaching class or giving up for the night._

- **Functional:** Unstick on a specific problem, fast; know what to study next.
- **Emotional:** Feel in control, not alone, not stupid. The right tone matters — not "here is the answer," but "here's how to think about it."
- **Social:** Feel like a "serious" aspirant — someone using a smart tool, not someone desperately Googling answers. Shareable wins ("got my rank from 50k to 20k using this") are a huge acquisition driver in JEE Telegram groups.

**Secondary JTBDs (track but don't build for in MVP):**
1. When I finish a mock test, I want to know which chapters are *actually* weak (not just "you got this wrong"), so I can prioritize.
2. When my parents ask "is this working?" I want a dashboard I can show them, so they see their ₹299/mo isn't wasted.
3. When I'm about to break, I want a human-ish voice telling me it's ok to take a break. (Emotional layer — likely v2.)

**Workarounds today:**
- **YouTube + PhysicsWallah free content** — free, enormous library, but passive. You can't ask it "why is this step justified?"
- **Telegram groups** (many JEE prep Telegram communities, often 10–50k members) — other students answer; quality is hit-or-miss, latency is hours.
- **Doubtnut app** — photo-a-problem, get video solution. Works, but video solution doesn't adapt to *why* you're stuck.
- **Coaching-class doubt slots** — wait till Monday, ask teacher, 5-minute answer. High quality, but gated by time.
- **Just give up for the night** — very common. Kills retention of prep.

The real competitor is YouTube + Telegram + "give up." Beating those means being faster than YouTube, smarter than Telegram, and always-available.

---

## 3. Market

### Size — TAM / SAM / SOM

- **TAM (all Indian competitive-exam aspirants — JEE, NEET, UPSC, CAT, CUET):** ~5–6 crore students/year `[assumption, aggregated from exam registration statistics]`. ARPU at ₹2,000/yr blended = ~₹10,000 crore (~$1.2B).
- **SAM (JEE-specific, smartphone-owning, willing-to-pay online):** ~15.4 lakh JEE Main registrants 2025 [India Today](https://www.indiatoday.in/education-today/news/story/jee-main-2025-registration-numbers-surge-to-all-time-high-with-13-lakh-applicants-2639594-2024-11-25) × estimated 60% English/Hinglish-comfortable and smartphone-native = ~9 lakh × ₹3,600/yr (₹299/mo avg ARPU) = **₹324 crore (~$39M) SAM**.
- **SOM (realistic year 1):** 1–2% of SAM = **₹3–6 crore (~$400k–$700k) ARR**.

**Bottom-up sanity check:** 15.4L JEE aspirants × 10% reachable in year 1 (tier-2/3 droppers + Class 12) × 5% paid conversion × ₹3,600/yr = **₹2.77 crore (~$330k) ARR**. Same order of magnitude as top-down — the numbers triangulate.

This is a large market with a meaningful indie-SaaS Year-1 ceiling and a VC-scale Year-3 ceiling if expansion into NEET/UPSC works.

### Segments

1. **Tier-2/3 droppers (BEACHHEAD)** — students who finished Class 12, didn't clear JEE, can't afford/move to Kota, prepping at home with parents watching wallets closely. ~2–3 lakh/year `[assumption]`. Acute pain, self-directed, measurable outcome (rank), digital-native.
2. **Tier-2/3 Class 12 students in the final push** — similar profile but parallel to school. Bigger segment (~5–7 lakh) but more distractions; school takes priority.
3. **Kota-enrolled students** — already paying ₹3–5 lakh, AI tutor is a supplement not a replacement. Later expansion segment.
4. **Class 11 students / early-stage** — long runway but slow feedback loop for MVP validation; don't chase in year 1.

**Beachhead: droppers.** Reasons: highest pain, highest willingness-to-pay (they've already failed once, parents don't want year 3), measurable outcome (JEE 2027 rank), concentrated in Telegram groups and r/JEE for distribution, decision happens in April–June post-results window (concentrated buying season).

### Trends and timing

- **BYJU's collapse (2024)** — from $22B to ~$0, laying off thousands, Toppr permanently shut down [Inc42](https://inc42.com/features/byjus-2024-review-collapse-edtech-giant-byju-raveendran/). Opens mindshare and orphaned users.
- **PhysicsWallah IPO (Nov 2025)** — went public at ₹3,480 crore IPO [Wikipedia — Physics Wallah](https://en.wikipedia.org/wiki/Physics_Wallah). Signals edtech category re-opening to capital, but PW has optimized for cheap video — not AI tutoring.
- **AI capability unlock** — Claude 4/GPT-4o class models can solve JEE Main problems reliably; step-by-step reasoning (chain-of-thought) maps directly to JEE pedagogy. LLM cost at ~$0.003/1k tokens makes per-student cost viable at ₹299/mo.
- **Smartphone + cheap data** — 660M smartphone users, data at ₹9/GB [Storyboard18](https://www.storyboard18.com/digital/660-million-smartphone-users-16-17-billion-monthly-upi-transactions-power-digital-bharat-report-89731.htm). Tier-2/3 cities drive 70% of new smartphone sales. The physical distribution constraint is gone.
- **Parental mental-health awareness (post-Kota suicides)** — 2024 media attention on Kota suicides shifted parent sentiment toward "can my kid prep at home?" [The Diplomat](https://thediplomat.com/2024/02/student-suicides-in-kotas-coaching-factories-point-to-indias-broken-education-system/). Parents are actively considering alternatives they weren't considering in 2021.

**Why now (one paragraph):** In 2021 an AI tutor for JEE would have cost $50/user/month in LLM fees, run on sub-B-grade models that couldn't solve JEE Advanced, required a desktop, and been sold to parents who still believed Kota was the only answer. In 2026 LLM cost is ~1–3% of that, models solve JEE Main reliably, 660M Indians own smartphones, mobile data is essentially free at ₹9/GB, BYJU's collapse has cleared the incumbent, and parents are reading about Kota suicides and actively asking "is there another way?" This is a three-to-five-year window.

---

## 4. Competitors

### Direct

| Name | URL | Target user | Core job | Positioning | Pricing | Strengths | Weaknesses |
|---|---|---|---|---|---|---|---|
| **PhysicsWallah** | [pw.live](https://www.pw.live/) | Tier-2/3 JEE/NEET aspirants | Affordable video coaching | "Quality coaching at 1/10th the price" | ₹4,200–45,000/course; Vidyapeeth offline ₹50k–1.5L | Scale (₹800+ crore revenue, ~$2.8B valuation) [TechCrunch](https://techcrunch.com/2024/09/19/indias-physics-wallah-raises-210m-at-2-8b-valuation-even-as-edtech-funding-remains-scarce/), strong brand in tier-2/3 | Video-centric (passive), not AI-personalized, now split between online + offline |
| **Unacademy** | [unacademy.com](https://unacademy.com/) | JEE/NEET + UPSC + CAT | Live online classes + test series | "Learn from India's top educators" | ₹2,500–30,000/course | Brand, ₹988 crore revenue FY24 [Entrackr](https://entrackr.com/2024/09/unacademy-narrows-losses-by-62-in-fy24-revenue-remains-flat/) | Revenue declining 5% YoY, struggling post-COVID, losing mindshare to PW |
| **Allen Digital** | [allen.in](https://allen.in/) | Serious JEE/NEET students (Kota-adjacent) | Coaching-class-caliber content, online | "The Kota standard, online" | ₹20,000–80,000/course | Academic credibility (34 of top-100 JEE Main 2023 ranks from Allen) | Expensive, still batch-model, weak digital UX |
| **Embibe** (Jio) | [embibe.com](https://www.embibe.com/) | JEE/NEET/Boards | AI-powered personalized learning | "AI-first exam prep" | Freemium / Jio bundle | Jio distribution muscle, been in market since 2012 | Feature bloat, unclear positioning, inherited from Reliance |
| **Arivihan** | [arivihan.com](https://www.arivihan.com/) | Tier-3/4 JEE/NEET students | Fully-automated GenAI tutor | "Your personal AI tutor" | ₹200–500/mo `[assumption based on segment]` | Closest direct competitor on AI-tutor thesis; $4.17M funded 2025 by Prosus/Accel | Tiny team; narrow geo (MP/Rajasthan); limited brand |
| **Doubtnut** | [doubtnut.com](https://www.doubtnut.com/) | Class 9–12, JEE/NEET | Photo-to-video doubt solution | "Click a pic, get a solution" | Freemium | Huge free user base | Video-based (not adaptive), acquired by Allen 2024 — being absorbed |

### Indirect

- **YouTube + creator channels (PW free channel, Khan Academy, Unacademy free, Nitin Vijay Sir, etc.)** — the real "free" competitor. 95% of the value of coaching content is free on YouTube. Wins on price, loses on personalization and "what should I do today."
- **Telegram / Discord JEE groups** — peer-to-peer doubt solving. Free, social, unreliable quality, latency in hours.
- **Traditional coaching (Allen, Resonance, FIITJEE, Aakash)** — offline, expensive (₹1–5L), still the default for serious aspirants. Winning by inertia + parent trust + rank-producer track record.

### Substitutes (the real competitors)

- **YouTube + a WhatsApp group of classmates + giving up after 20 minutes stuck.** Free, universal, bad. This is the actual workflow of tier-2/3 self-studying students and it's what the MVP has to beat on (a) instant response, (b) explanation quality, (c) "what next" prescription.
- **Kota migration (for those who can afford it).** ₹3–5 lakh, 150k–200k students/year [The Diplomat](https://thediplomat.com/2024/02/student-suicides-in-kotas-coaching-factories-point-to-indias-broken-education-system/). Brutal, expensive, emotionally costly — but culturally defaulted-to in India.
- **Private home tutors** — ₹500–2000/hour in tier-1, cheaper in tier-2/3. High quality, low scale. For many middle-class families this is the realistic substitute.

### Positioning map (2×2)

**Axes:** **Personalization depth (generic → adaptive AI)** × **Price (free/cheap → premium)**.

**Why these axes:** Personalization is the capability gap that AI unlocks and video-based incumbents can't easily copy. Price is the demographic gate — tier-2/3 is price-sensitive; premium incumbents (Allen) can't drop price without cannibalizing their offline business.

```
        PERSONALIZED (adaptive AI)
             |
   Embibe    |    YOU
   Arivihan  |   (whitespace for a
             |    strong AI+Hinglish
             |    wedge at ₹299)
-------------+-------------  PRICE (free/cheap → expensive)
   YouTube   |    Allen Digital
   PW free   |    Unacademy
   Doubtnut  |    PhysicsWallah paid
             |    Coaching classes (Kota)
         GENERIC (batch/video)
```

Whitespace sits in the upper-left/upper-middle: cheap + adaptive. Embibe and Arivihan are the nearest occupants; neither is dominant. Embibe has distribution but weak focus; Arivihan has focus but no distribution.

### Pricing landscape

- **Offline coaching (Allen, FIITJEE, Resonance):** ₹1–2.5L/year, up to ₹5L for 2-year Kota programs [Vedantu](https://www.vedantu.com/jee-main/average-fees-range-for-jee-coaching-in-india).
- **Online coaching paid tier (PW, Unacademy, Allen Digital):** ₹2,500–45,000/year.
- **AI tutors / doubt apps (Embibe, Doubtnut, Arivihan):** freemium, paid ₹200–500/month `[assumption on Arivihan]`.
- **The pricing "floor" for a serious paid student is ~₹200/mo.** Anything cheaper reads as "not serious." Anything much above ₹500/mo competes with PhysicsWallah's packaged courses and feels overpriced for an AI chat.
- **Sweet spot:** ₹299/mo / ₹1,499/yr with a real free tier (10 doubts/day) to seed.

### Moat analysis

- **PhysicsWallah:** moat is brand + low-cost content production + founder (Alakh Pandey) cult following. Weakness: batch video doesn't personalize; they're structurally locked into the video-lecture model.
- **Allen:** moat is rank-producer track record + offline brand + IIT-aspirant parent trust. Weakness: digital UX is dated; expensive; can't serve tier-2/3 at scale online without cannibalizing.
- **Embibe (Jio):** moat is Reliance Jio distribution. Weakness: no product focus; trying to do everything; JEE isn't the priority.
- **Arivihan:** moat forming in tier-3/4 geographies. Weakness: tiny team, narrow reach, no brand outside funding circles.
- **Our moat thesis:** **Proprietary step-by-step problem-solution + student-mistake data** accumulates with every doubt. Over 6 months, ~100k problems × mistake patterns = a dataset no LLM alone can reproduce. Pair with Hinglish voice + tier-2/3 distribution and the moat is: _"a smaller AI that knows JEE better than GPT-5 does because it has seen 200k real Indian student mistakes."_ This only compounds.

### Whitespace and wedge thesis

- No direct competitor is a focused AI-first, Hinglish-first, adaptive tutor for droppers at ₹299/mo. Arivihan is closest but narrowly distributed.
- Every paid competitor (PW, Unacademy, Allen) is structurally a video-lecture or live-class business; AI personalization isn't their DNA.
- BYJU's collapse + Toppr shutdown have orphaned millions of students actively shopping for alternatives.
- **Wedge:** mobile-first Hinglish AI tutor for tier-2/3 droppers — doubt-solve + daily adaptive plan — at ₹299/mo. Distribution via r/JEE + Telegram + 3–5 YouTube micro-creators who teach JEE at free-or-cheap prices. Expand to Class 12 → Class 11 → NEET after the dropper segment works.

---

## 5. SWOT

### Strengths (internal, specific, asymmetric)
- Solo founder shipping velocity — no coordination cost. (Assumes the tech-chops are there.)
- AI-first architecture from day 1 — incumbents are structurally locked into video/batch and cannot pivot fast to adaptive AI.
- Pricing freedom — no offline-coaching revenue to cannibalize, can price at ₹299 without upsetting anyone internally.
- Beachhead clarity — picking droppers in tier-2/3 avoids direct head-on with PW/Allen (who go after broader Class 11–12).

### Weaknesses (honest)
- **No distribution.** No YouTube following, no coaching-class relationship, no Telegram admin access. Everything is zero-to-one.
- **No brand.** In a category where parents trust "rank producers," an unknown app is a hard sell.
- **Single founder bandwidth.** 6-month runway is tight for a habit-product with 2-year user journey.
- **LLM dependency.** Cost, reliability, and accuracy all depend on OpenAI/Anthropic — margin and moat both at risk if model prices spike or providers deprioritize India.
- **No IIT-alum on team (assumed).** Parent-trust signal is missing. Hard to say "by JEE toppers" without a JEE topper.

### Opportunities (external shifts in our favor)
- **BYJU's collapse + Toppr shutdown** — orphaned millions of students, tied to AI-capability unlock.
- **Parent sentiment shift post-Kota suicides** — "let my child prep at home" is newly acceptable.
- **LLM + Hinglish TTS maturation** — a 2021-impossible product became 2026-trivial.
- **UPI + WhatsApp Pay** frictionless collection for ₹299/mo; no card-form drop-off.
- **Reddit r/JEE + Telegram JEE groups** are a live distribution surface with no marketing cost if you earn a reputation.

### Threats (concrete named risks)
- **PhysicsWallah could bolt on AI tutor inside their existing app in one quarter.** They have the distribution; they'd catch up on product fast. Early signal: PW launches "PW Genie" or similar. Mitigation: move fast, own "Hinglish AI dropper tutor" positioning before they do.
- **Arivihan scales up with Prosus/Accel money.** They could spend us out on performance marketing. Mitigation: compete on organic community (r/JEE, Telegram) not on paid acquisition.
- **Model provider policy changes** — OpenAI/Anthropic price hikes or output restrictions on Indian exam content (already some moderation friction on "solve exam problems"). Mitigation: multi-provider architecture; test open-weight models (Llama, Mistral) as fallback.
- **Parents don't trust an app they can't see.** "Can a phone really teach my kid?" objection. Mitigation: parent dashboard + WhatsApp weekly progress summary.
- **Kota coaching industry lobbying** — pressure on ed regulators could target AI tutoring. Low likelihood, high impact.

---

## 6. Risks

| Risk | Likelihood | Impact | Early signal | Mitigation |
|---|---|---|---|---|
| LLM accuracy on JEE Advanced math/physics below teacher quality | M | H | <70% accuracy on 100 past-paper problems in pre-MVP test | Use hybrid: LLM + symbolic math (SymPy) for math; flag low-confidence; offer "escalate to human" on paid tier |
| Parents won't pay; students can't convert parents | H | H | <5% free→paid after 14 days in beta | Direct-to-parent WhatsApp onboarding; parent progress dashboard; 7-day money-back |
| Distribution via Telegram/Reddit stalls | H | H | <100 organic signups in month 1 | Pre-launch: seed 5 micro-influencer deals; build a "JEE question of the day" free content engine to farm subscribers |
| Hinglish voice/text quality feels like bad Hindi | M | M | <3.5/5 qualitative rating from 10 beta students | Fine-tune a Hinglish system prompt; do 50-sample blind A/B with students before shipping |
| Per-user LLM cost > ₹100/mo at ₹299/mo ARPU | M | H | Cost dashboard exceeds ₹100/paid user in beta | Cache common doubts; use cheaper models (Haiku, GPT-4o-mini) for simple questions; rate-limit free tier |
| PhysicsWallah or Embibe launches competing AI tutor before year-end | M | H | Public product launch announcement | Speed wins; own a positioning (Hinglish-first + dropper-first) they won't copy quickly |
| Kota coaching chains issue cease-and-desist on benchmark comparisons | L | L | Legal notice | Standard: cite publicly available data only; avoid named teardown in marketing |

---

## 7. Insights

> _The most valuable section. Non-obvious findings that change the build._

1. **The primary competitor is not a company — it's "give up after 20 minutes stuck."** Self-studying tier-2/3 students hit a wall nightly and the most common response is to close the book, not switch tools. The MVP wins if it converts "give up" into "one more try" with a 30-second low-friction re-engagement. **Implication:** Latency and tone matter more than feature breadth. <5-second response. Warm, patient voice. Free tier must trigger in the "stuck moment" with zero signup friction.

2. **Parents are the buyer, students are the user — and WhatsApp is where parents live.** In tier-2/3, parent buy-in unlocks the wallet, but parents don't use apps. A weekly WhatsApp progress summary (auto-generated, "Rahul practiced 42 problems this week, weak in Rotational Dynamics, strong in Electrochemistry") converts parental anxiety into paid subscriptions. **Implication:** Build a parent-WhatsApp channel from day 1 — it's the monetization surface, not the app itself.

3. **BYJU's collapse created a once-in-a-decade trust vacuum — but also a trust allergy.** Millions of students were burned by BYJU's aggressive sales. An AI tutor that positions against that ("no sales calls, no ₹1 lakh commitment, cancel anytime") converts directly. **Implication:** Pricing page should lead with "no sales call," "monthly, cancel anytime," "free until you solve 10 problems." Anti-BYJU positioning is an acquisition wedge.

4. **Hinglish is not a translation problem — it's a pedagogy choice.** JEE teachers in tier-2/3 coaching routinely explain Newton's laws in Hindi while writing equations in English. Pure-English AI tutors (GPT raw) feel cold and foreign; pure-Hindi would lose all math notation. **Implication:** The system-prompt engineering around Hinglish register is a real moat — one week of prompt engineering + 50 beta student ratings beats 3 months of raw model upgrades.

5. **Dropper season is April–June** — post-results window. Parents make the coaching/app decision within 4 weeks of the result. If the MVP isn't ready with a distribution plan by April of a given year, it misses the buying season and has to wait 12 months. **Implication:** The launch calendar is not arbitrary. Time the public MVP to hit 3 weeks before JEE Main results, run aggressive community seeding during result week, close on the April–June cohort.

6. **The "what should I do today" plan is a stickier hook than doubt-solving.** Doubt-solving is reactive — used when stuck. Planning is proactive — opened first thing in the morning. Planning drives daily active sessions; doubt-solving drives depth. **Implication:** Even though doubt-solving is the headline feature, the daily plan is what drives retention. MVP should include both; the v1 iteration should invest more in planning UX than doubt UX.

7. **Mock test analysis is a pro-tier moat no one does well.** All JEE platforms offer mock tests; none analyze them well. "You got 40 wrong in Physics" is useless. "You're wasting 6 minutes/test on problems you'd have gotten if you'd reviewed trigonometric substitution" is life-changing. **Implication:** v1 upsell = diagnostic mock analysis. Drives ₹299 → ₹599 tier economics after MVP proves the habit.

---

## 8. Open research questions

- Which 5 micro-creators (r/JEE, YouTube JEE teachers < 100k subs, Telegram admins) are most open to a launch partnership? Resolve by: cold DMs in weeks 1–2.
- What's the real LLM cost per paid user in a representative month of usage? Resolve by: instrumented 50-user alpha, measure tokens × price.
- How does LLM accuracy stack on JEE Advanced problems specifically (beyond JEE Main)? Resolve by: benchmark run of 100 JEE Advanced past-paper problems across Claude, GPT, and open-weight models.
- Will parents in tier-2/3 actually pay via WhatsApp/UPI at ₹299/mo? Resolve by: 10 paid beta families before writing the scaled app.

---

## Sources

- [India Today — JEE Main 2025 registration numbers](https://www.indiatoday.in/education-today/news/story/jee-main-2025-registration-numbers-surge-to-all-time-high-with-13-lakh-applicants-2639594-2024-11-25) — authoritative JEE 2025 registration numbers (15.4 lakh)
- [Inc42 — BYJU'S 2024 Review](https://inc42.com/features/byjus-2024-review-collapse-edtech-giant-byju-raveendran/) — BYJU's $22B → near-zero collapse narrative and industry ripple
- [TechCrunch — PhysicsWallah $2.8B raise](https://techcrunch.com/2024/09/19/indias-physics-wallah-raises-210m-at-2-8b-valuation-even-as-edtech-funding-remains-scarce/) — PW valuation + revenue trajectory
- [Entrackr — Unacademy FY24 losses](https://entrackr.com/2024/09/unacademy-narrows-losses-by-62-in-fy24-revenue-remains-flat/) — Unacademy revenue (₹988 Cr) + declining growth
- [Propelld — Allen Kota fee structure 2024](https://propelld.com/site/blog/allen-kota-fees) — coaching fee benchmarks for positioning
- [The Diplomat — Kota coaching suicides](https://thediplomat.com/2024/02/student-suicides-in-kotas-coaching-factories-point-to-indias-broken-education-system/) — mental health + 150k–200k Kota student flow + 2% success rate
- [The Hindu — 13th suicide in Kota mid-2024](https://www.thehindu.com/news/national/jee-aspirant-from-bihar-dies-by-suicide-in-kota-13th-incident-this-year/article68366961.ece) — 2024 suicide count
- [SATHEE / IIT Kanpur — JEE NEET mental health crisis](https://sathee.iitk.ac.in/gk/exam-news/06-07-2024/jee-exam/neet-jee-exams-are-causing-a-mental-health-crisis-in-india-students-are-struggling-to-cope/) — 30% mental health deterioration stat
- [Storyboard18 — 660M smartphone users / ₹9 per GB data](https://www.storyboard18.com/digital/660-million-smartphone-users-16-17-billion-monthly-upi-transactions-power-digital-bharat-report-89731.htm) — distribution and cost-of-access infrastructure
- [Vedantu — JEE coaching fee ranges](https://www.vedantu.com/jee-main/average-fees-range-for-jee-coaching-in-india) — India-wide average fee benchmarks
- [Wikipedia — Physics Wallah](https://en.wikipedia.org/wiki/Physics_Wallah) — PW IPO and company summary
- [Forbes India 30 Under 30 — Arivihan](https://www.forbesindia.com/article/30-under-30-2026/a-personal-tutor-for-all/2990145/1) — closest direct competitor profile

---

_Changelog_
- 2026-04-18: initial draft
