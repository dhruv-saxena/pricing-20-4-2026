# pricing-20-4-2026

Single-file pricing page prototype (`pricing-20-4-2026.html`). Tailwind (CDN), Inter, Phosphor icons. Designed at a fixed 1280px viewport. Plan illustrations are embedded as base64 data URIs — no external assets required.

## Layout

- Three plans side-by-side: **Basic**, **Pro**, **Gold**.
- Pro is the highlighted card: gradient background, 2px brand border, floats up 21px, sits 45px taller than the others.
- Close button (top-right) and a centered "view toggle" link sit above the cards.
- Footer shows a fading brand-logo ticker (Microsoft, Google, Adobe, Meta, McKinsey, Amazon, EY).

## Interactive behaviors

### 1. Individual ↔ Team & Enterprise view toggle
- Link at top center switches between two views.
- Copy flips between:
  - Individual view → "Save more with team and enterprise plans"
  - Team view → "Buying just for yourself? See individual plans"
- Team & Enterprise view is currently an empty container (placeholder).

### 2. Gold card: yearly ↔ monthly billing toggle
- Switch at top-right of the Gold card (`role="switch"`, defaults to yearly).
- **Yearly (default):** price shows `₹8,978/mo` with strikethrough `₹17,950`, cadence "billed yearly", and a green confirmation line: "You'll save ₹107,664 this year".
- **Monthly:** price shows `₹17,950/mo`, no strikethrough, cadence "billed monthly", and the save line becomes a clickable link: "Switch to yearly to save ₹107,664" — clicking it flips the toggle back to yearly.

### 3. Pro card: countdown timer on the CTA
- Buy Now button on Pro includes a "SAVE 10% / For MM:SS" badge.
- Timer starts at `59:48` and ticks down every second, clamped at `0:00`.

### 4. Hover hints on each plan's CTA
- Hovering over any Buy Now button reveals a one-line description of who the plan is for:
  - Basic — "For those who want to make simple decks occasionally"
  - Pro — "For those who want AI to craft polished, on-brand decks regularly"
  - Gold — "For those who want the best AI models to lead mission-critical decks"

### 5. Static display elements
- Basic: shows `₹374/mo` billed yearly, "No offers available for this plan".
- Pro: shows `₹675/mo` (strike `₹750`) billed yearly, green line "You'll save ₹900 this year".
- Feature lists for each plan, with credits highlighted at top (1,500 / 5,000 / 50,000).

## Running it

Open `pricing-20-4-2026.html` directly in a browser. No build step.
