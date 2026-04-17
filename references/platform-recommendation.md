# Platform Recommendation

The platform decision — web vs mobile vs desktop vs CLI vs browser extension vs hybrid — is almost always determined by the user's context, not by preference. Research the context first; recommend second.

## Decision factors (rank these)

Weight factors 1–5 by how load-bearing they are for this product. Then pick the platform that scores best across the heavy factors.

### 1. Where the user is when they hit the pain
- In front of a laptop, heads-down in work → **web or desktop**
- On the move, hands busy, stolen moments → **mobile**
- Inside another tool (Gmail, browser, code editor) → **extension or plugin**
- Terminal-native workflow → **CLI**
- At a desk doing deep focus work → **desktop** (or heavy web app)

### 2. Input requirements
- Fast text typing, long-form input → web/desktop wins
- Quick capture, voice, photo → mobile wins
- Structured data entry across many fields → web/desktop
- Single action, one tap, contextual → mobile or extension

### 3. Output consumption
- Dashboards, comparison, multi-pane → web/desktop
- Notifications, glanceable info → mobile
- Inline in another context (email, browser) → extension
- Piped/scripted → CLI

### 4. Distribution
- App stores have gatekeepers, high CAC, discovery via search + social
- Web has URL-shareability, SEO, zero install friction
- CLI distributes through GitHub / Homebrew / npm — zero CAC if you hit the right community
- Extensions distribute through Chrome Web Store — lower friction than app stores, but narrow audience

### 5. Monetization
- Subscription web app is easiest to monetize
- Mobile has App Store 30% cut (15% for small biz) but frictionless payments
- CLI is historically hard to monetize directly — usually a wedge into a paid web/SaaS product
- Extension — typically supports a paid SaaS, rarely the main product

### 6. Team / builder capability
- Who's building? What do they know? One-person team should pick the stack they can ship in.
- Single platform for MVP. Do not do "mobile + web + desktop in v1." Pick one.

## Common patterns (from the wild)

### Consumer productivity for busy parents / commuters
→ **Mobile-first** (maybe iOS-only for MVP). Users capture in stolen moments. Web can come later as a "review" surface.

### B2B SaaS (most categories)
→ **Web**. Buyers are at desks; workflows are heavy; integrations are URL-based.

### Developer tool
→ **CLI first**, then GitHub / VS Code integration. Web dashboard for team features later.

### Content / writing tool
→ **Web** (desktop-class web app). Writers are at computers.

### Salesperson / field worker
→ **Mobile**. They're out of the office.

### Hobbyist creator
→ Depends on craft — photographers want desktop, TikTokers want mobile, writers want web.

### AI chat wrapper
→ **Web** first (cheap, fast). Mobile only if the use case is intrinsically mobile (voice, on-the-go).

### Browser-data tool (tabs, bookmarks, reading)
→ **Browser extension** — you need to live where the user browses.

### E-commerce storefront
→ **Web** with mobile web that works well. Native app only after $10M+ scale.

## Hybrid approach — when it's right

"Build for web + mobile with one codebase" (React Native, Flutter, PWA) can be right if:
- The feature set is identical across surfaces
- The team is small and needs one codebase
- The experience is data-display-centric, not platform-native feel

It's wrong if:
- The core interaction is genuinely platform-specific (camera use, notifications, deep OS integration)
- You need to ship in 3 weeks and don't know React Native
- Performance / polish is the primary differentiator

**Default: pick one surface for MVP. Add others after proven.**

## Output format for `plan.md`

One section titled **Platform recommendation**. Include:

1. **Recommended platform** — one line: the pick.
2. **Why** — 3–5 bullets tying to research findings. Reference the user journey explicitly. ("Target user is a dog trainer holding a leash in one hand mid-session — mobile with voice capture is the only form factor that lets them log during the session rather than after, which is where existing tools fail.")
3. **Alternatives considered and rejected** — 1–2 alternatives with a one-line reason each.
4. **Future platforms** — when to add them, triggered by what signal. ("Add web after 200 MAU and clear demand for reviewing sessions on a larger screen — specifically when >30% of users are exporting notes to email/PDF.")

Rigor here matters. Bad platform pick can kill an otherwise great idea.
