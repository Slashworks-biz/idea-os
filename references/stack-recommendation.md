# Stack Recommendation

Recommend three stack options: **conservative**, **modern**, **cutting-edge**. Each with pros/cons and a clear fit-for-whom. Then pick one.

Adjust defaults by tier:
- **T1/S1** — strong bias toward managed + familiar. Shipping speed beats everything.
- **T2/S2** — modern default. The builder can handle some novelty.
- **T3/S3** — modern or cutting-edge only where it's a durable advantage; conservative for everything else.

## Three-option template

Always write three, even if one obviously wins. The exercise forces the user to see tradeoffs.

### Option A — Conservative
- "Boring tech" that works. Well-documented. Easy to hire for. Slow to change.
- Pick when shipping speed matters, team is junior, or stakes are high.

### Option B — Modern
- The current pragmatic default. Popular, productive, mature enough.
- Pick for most T2 / T3 builds.

### Option C — Cutting-edge
- Newer tools that offer a real edge (speed, DX, capability) but with risk — breaking changes, smaller community, incomplete docs.
- Pick only where the edge is strategic and the team can absorb churn.

For each option, capture:

| Field | Notes |
|---|---|
| **Frontend** | Framework + styling + UI kit |
| **Backend** | Language + framework + runtime |
| **Database** | Primary DB + any secondary stores |
| **Auth** | Managed or self-hosted |
| **Hosting** | Platform + CI/CD |
| **AI / ML** (if relevant) | Model provider + orchestration |
| **Observability** | Logging + errors + analytics |
| **Pros** | 2–3 bullets |
| **Cons** | 2–3 bullets |
| **Best for** | One-line archetype |

## Common defaults by product type

Use as a starting point — adjust to the specific idea.

### Web SaaS (T2 default)
- **Frontend:** Next.js + Tailwind + shadcn/ui
- **Backend:** Next.js API routes (or a small Node/Python service)
- **Database:** Postgres (managed — Supabase, Neon, or RDS)
- **Auth:** Clerk / Auth.js / Supabase Auth
- **Hosting:** Vercel / Railway / Fly.io
- **AI:** Anthropic / OpenAI / Vercel AI SDK
- **Observability:** Sentry + PostHog

### Mobile-first consumer app (T2)
- **Conservative:** React Native + Expo
- **Modern:** Expo + EAS Build + TypeScript
- **Cutting-edge:** SwiftUI for iOS-only MVP (less portable, better feel)
- **Backend:** Supabase or Convex (real-time out of box) or Firebase
- **Payments:** RevenueCat (standard for mobile subscriptions)
- **Push:** Expo push or Firebase Cloud Messaging

### CLI / developer tool (T1–T2)
- **Language:** TypeScript (Node + npm distribution) or Go (single binary) or Rust (performance, harder)
- **Distribution:** npm / Homebrew / cargo
- **Auth (if needed):** device-code flow → token
- **Hosting (if there's a backend):** Fly / Railway / Cloudflare Workers

### AI product / AI wrapper (T2)
- **Frontend:** Next.js + Vercel AI SDK (streaming built in)
- **Backend:** Edge runtime for low latency or Node for flexibility
- **Models:** Anthropic (Claude) for reasoning, OpenAI for images/embeddings where applicable
- **Vector DB (if RAG):** pgvector (cheap) / Pinecone / Turbopuffer / Qdrant
- **Eval/monitoring:** LangSmith / LangFuse / Braintrust
- **Queue:** BullMQ / Inngest for background jobs (LLM calls can be slow and bursty)

### Marketplace (T3)
- **Frontend:** Next.js (SSR for SEO matters)
- **Backend:** Dedicated service (Rails / Django / Node + TypeScript)
- **DB:** Postgres with careful schema for listings + transactions
- **Search:** Algolia / Typesense / Postgres full-text for MVP
- **Payments:** Stripe Connect (for marketplace payouts)
- **Background:** Proper queue (Sidekiq / Celery / BullMQ)

### Content / blog / SEO play (T1–T2)
- **Conservative:** Astro or Hugo (fast, static)
- **Modern:** Next.js with MDX
- **Hosting:** Cloudflare Pages / Vercel
- **CMS:** Contentful / Sanity / plain markdown in repo

### Browser extension (T1–T2)
- **Framework:** Plasmo (React-based extension framework)
- **Bundler:** Vite
- **Cross-browser:** Write for Chromium, port to Firefox later

### Hardware / IoT (T3)
- **Firmware:** C / Rust / MicroPython (depending on MCU)
- **Gateway:** Raspberry Pi / custom hardware with MQTT
- **Cloud:** AWS IoT Core / Google IoT / self-hosted MQTT + Postgres

## Anti-patterns in stack choice

- **Picking a stack for the v5 product you imagine, not the v1 you're shipping.** Build the MVP in the fastest tool. Rewrite when there's proof.
- **Kubernetes for an MVP.** No.
- **Microservices day 1.** No. Monolith first.
- **Self-hosting everything.** Use managed services for the MVP unless you have a specific reason. Engineering time is not free.
- **Resume-driven choices.** If the stack is chosen because the builder wants to learn it, flag that honestly. Learning is fine, shipping is also fine; mixing them silently isn't.
- **Greenfield rewrite of an existing tool.** If a managed product does 80% of what you need, use it for the MVP and keep the optionality to rewrite.

## Output format for `plan.md`

One section titled **Stack recommendation**.

1. The table with all three options (Conservative / Modern / Cutting-edge)
2. **Recommended:** one-line pick + 2-bullet reason
3. **Migration path:** when and why you might change stack later (what signal triggers a rethink)
