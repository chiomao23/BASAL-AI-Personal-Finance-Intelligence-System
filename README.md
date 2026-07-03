# Handoff: BASAL — AI Personal Finance Intelligence System (Web Dashboard)

## Overview
BASAL is a SaaS "financial co-pilot" — it aggregates a user's bank, card, and wallet
accounts and uses ML to deliver **predictive cash-flow forecasting**, **adaptive
budgeting**, an **early-warning system**, and **actionable, one-tap recommendations**.

This bundle contains the **main web dashboard** (the "Overview" screen) as a
high-fidelity, interactive prototype.

## About the Design Files
`BASAL Dashboard.dc.html` is a **design reference created in HTML** — a prototype that
shows the intended look and behavior. It is **not production code to copy directly**.

- The `.dc.html` format is a self-contained streaming component (custom `<x-dc>` runtime).
  You do **not** need to adopt that runtime. **Open the file in a browser to see and click
  the real design**, and read it as a spec.
- Your task: **recreate this design in the target codebase's environment.** If you're
  building fresh, React + TypeScript is the natural fit (the prototype's logic is already
  structured like a React class component — state + a `renderVals()` that returns view data).
  Use your own component library, styling system, and data layer.
- All "AI" responses and all numbers in the prototype are **hard-coded sample data**. The
  real forecasting/ML and bank connections live behind this UI (see "What powers this" at
  the bottom).

## Fidelity
**High-fidelity.** Colors, typography, spacing, and interactions are final. Recreate the UI
faithfully, then wire it to real data and services.

---

## Screen: Overview Dashboard

### Layout
- Full-viewport app shell, `display:flex`, `height:100vh`, no page scroll on the shell.
- **Left sidebar**: fixed `236px`, vertical flex. Brand → nav menu → Premium upsell card →
  user profile pinned to bottom (`margin-top:auto`).
- **Main area**: flex column. Sticky **top bar** (greeting + search + "Connect account" +
  notifications), then a **scrolling body** (`overflow-y:auto`, padding `22px 26px 40px`).
- **Body grid**: `grid-template-columns: minmax(0,1fr) 348px; gap:18px; max-width:1240px`.
  - Left column (stacked, `gap:18px`): stat cards row → forecast chart → adaptive budget →
    early warnings.
  - Right rail (`348px`, stacked): AI co-pilot → connected accounts → goals.

### Components

**Sidebar nav** — 6 items (Overview active, Forecast, Budget, Alerts [red "2" badge],
Goals, Accounts). Item: `padding:9px 11px`, `border-radius:10px`, `font-size:13.5px`,
icon 17px stroke. Active item: `background:#1b2537`, `border:1px solid #27324a`, icon in
accent green. Inactive: text `#98a6bd`, hover → `background:#1b2537; color:#eef2f8`.

**Stat cards** (3, equal width) — label with colored dot, big number
(Space Grotesk 600, 29px, letter-spacing -0.5px), sub-line.
1. Total balance — `$17,260`, "▲ 2.4% vs last month" (accent).
2. Forecast low point — `$896` in **amber** (`#f2c14e`), "expected Jun 23".
3. Safe to spend — computed, "after bills & $1,500 buffer".

**Cash-flow forecast chart** — the flagship. An inline SVG (`viewBox 0 0 820 264`):
- Solid white line = actual balance (past); dashed animated accent line = forecast (future).
- Faint accent **confidence band** widening into the future.
- Dashed **amber horizontal line** = the user's safety buffer ($1,500 default).
- Dashed vertical "TODAY" divider; circular markers on income/bill events (green = money in,
  coral = money out) with labels.
- Amber dot + pill callout at the projected low when it dips below buffer:
  "⚠ Dips to $896 on Jun 23 — below buffer".
- **14D / 30D / 90D** toggle (top-right) recomputes the whole series.

**Adaptive budget** — header with a mode badge ("Suggest & confirm" / "Fully automatic").
Each category: name, `spent / cap` (mono), progress bar (accent < 85%, amber > 85%, coral if
over). Categories with a suggestion show an inline chip: *"Suggests $320 — trending 20% lower
for 3 weeks"* with **Apply** (accent) / **Keep** (ghost) buttons. Applying updates the cap and
shows a confirmation line. In "Fully automatic" mode, changes are auto-applied and labeled
rather than confirmed.

**Early warnings** — alert cards, `border` tinted by severity (amber = warning,
green = positive). Icon chip, title, timing pill ("in 5 days" etc.), body, optional CTA, and
an ✕ to dismiss. Alert #1's balance/date/timing are generated from the forecast so they stay
truthful.

**AI co-pilot** (right rail) — gradient card. Header: rounded-square avatar with a **pulsing
dot** (`@keyframes basalPulse`), name, "● Analyzing · updated 2m ago". Then a short intro and
a feed of **recommendation cards** (tag dot + label, title, body, primary action + "Not now").
Approving or dismissing removes the card and shows an **Undo toast** (bottom-center, 6s).
Bottom: a working **chat input** ("Ask about your money…") — Enter or send appends a user
bubble + a canned assistant reply keyed off words like "afford", "save", "bills", "low".

**Connected accounts** — list with mono initials badge, name, masked number, balance
(coral if negative), plus an "Encrypted" chip and a security footnote.

**Goals** — progress bars toward Emergency fund and Japan trip.

---

## Interactions & Behavior
- **Forecast range toggle** (14D/30D/90D): recomputes series, gridlines, markers, low point,
  and every derived stat. Default 30D.
- **Budget Apply/Keep**: Apply sets cap = suggested value + shows "✓ Applied"; Keep shows
  "Kept your limit".
- **Recommendation Approve/Dismiss**: removes card, shows Undo toast (auto-hides ~6s; Undo
  restores the card).
- **Alert dismiss**: removes the card.
- **Co-pilot chat**: Enter/click → append user + assistant bubbles.
- **Animations**: forecast line dash-flow (`~1.7s linear infinite`), co-pilot pulse
  (`~2.2s`), card rise-in (`~0.35s`).

## State Management
Prototype state (mirror in your framework): `range` ('14D'|'30D'|'90D'), `recs[]`, `budget[]`
(each: spent, cap, suggest, status), `alerts[]`, `chat[]`, `toast`. Derived per render: the
forecast series, gridlines, markers, low point, safe-to-spend, and all formatted strings.
**In production, replace the hard-coded series/data with API responses** (accounts, transactions,
forecast, recommendations).

Tweakable settings exposed in the prototype (make these real user settings):
`budgetMode` (Suggest & confirm | Fully automatic), `showConfidenceBand` (bool),
`riskThreshold` (safety buffer $, default 1500).

## Design Tokens (current design: light, friendly, emerald)
Colors (hex):
- Background `#eef1f6`, card `#ffffff`, inset `#f1f4f9`, hover `#eaeef4`, border `#e4e8ef`
- Text: primary `#1a2233`, secondary `#5b6577`, muted `#98a1b2`
- Accent (emerald — money & calm) `#1f8a6d`, secondary sage `#4bb39a`,
  positive `#1f9d6b`, warning amber `#e0a63a`, danger `#e5533d`

Type: **Plus Jakarta Sans** only — 400/500 body, 600/700 headings, 800 big numbers.
Radius 18px cards; soft shadows `0 8px 24px -10px rgba(20,30,50,.12)`.

Key UX features to preserve: the top "Ask BASAL anything" bar with one-tap
quick-question chips (feeds the co-pilot chat), the waving-hand greeting, the
plain-language labels, hover tooltips on every nav item, and the chart hover
crosshair (exact date + amount + Actual/Forecast).

Accessibility (color-blind support — preserve these): forecast line is dashed vs
solid (pattern, not just color); chart events use shape coding — circles = money in,
diamonds = money out — with text labels on each; alert severity uses glyphs (!, ~, ✓)
plus a left border; negative amounts always carry a minus sign; text colors meet
contrast on white. Never encode meaning in color alone.

Radius: cards 15–16px, chips/buttons 7–11px, pills 20px.
Spacing: card padding 16–18px, grid/stack gap 14–18px.

## Assets
No external images. Icons are simple inline SVGs; swap for your icon library. Fonts load from
Google Fonts.

## Files
- `index.html` — the marketing landing page (hero, features, how-it-works, security/CTA).
  Embeds the dashboard as a live, clickable demo. Named `index.html` so it opens
  automatically on GitHub Pages / any web host.
- `dashboard.html` — the interactive dashboard prototype, fully self-contained.
  Keep both files in the same folder — the landing page links to this by name.
- `preview.png` — static screenshot of the dashboard.

---

## What powers this (backend / ML — for planning the real build)
The UI is the visible 20%; these systems are what make it real:

1. **Account aggregation** — connect to banks/cards/wallets via an aggregator
   (e.g. Plaid, MX, TrueLayer, Tink). Store accounts, balances, and transactions; keep them
   fresh with webhooks/scheduled syncs. Read-only, tokenized — never store bank credentials.
2. **Transaction enrichment** — categorize transactions and detect **recurring** items
   (salary, rent, subscriptions) and their cadence. This is what the forecast is built on.
3. **Cash-flow forecast** — project the daily balance forward = current balance + expected
   recurring inflows/outflows + a model of discretionary daily spend, with a **confidence band**
   that widens with horizon. Start simple and honest (recurring-events + moving-average / a
   time-series model like Prophet or a gradient-boosted regressor) before anything fancier.
4. **Early-warning engine** — scan the forecast for points below the user's safety buffer, or
   spending anomalies vs. their own baseline, and fire alerts **days ahead**.
5. **Recommendations** — turn forecast + goals into specific, reversible actions
   ("move $200 to savings"), each tied to an executable step.
6. **Adaptive budgeting** — periodically re-fit category limits to recent behavior; respect the
   Suggest-vs-Automatic setting.
7. **Platform** — auth, encryption at rest/in transit, subscription tiers (freemium + premium),
   web + mobile clients against one API.

Suggested sequence: aggregation & enrichment first → basic forecast → alerts → recommendations →
adaptive budgeting → premium features (multi-account consolidation, scenario planning, shared
budgets).
