# Social Norms — Visual Direction
*Creative Brief v1.0 | The document every future design decision references*

---

## The Question This Brief Answers

Before touching a single color or font, you have to be able to answer:
**What does it feel like to be inside Social Norms?**

Not what does it look like. What does it *feel* like.

---

## The Atmosphere

When someone opens this website, the experience should feel like entering a quiet, serious space at night. Not a marketplace. Not a stage. More like a master trader's studio — dark, warm, with a single source of light. The kind of room where real thinking happens.

The dominant feeling is **calm authority**. Not aggression, not flash. The confidence of someone who has seen enough of the market to stop performing.

This matters because the trading education space is dominated by two extremes: the flashy "get rich fast" energy (Lambos, screenshot culture, orange gradients everywhere), and the dry, academic energy (charts on white backgrounds, bullet points, no soul). Social Norms belongs to neither. It belongs to a third space — one that takes the craft seriously without losing warmth.

**The site should feel like the person who made it doesn't need to sell you anything.** They're just telling you what they know.

---

## The Amber

The amber (#D47A2A) is the most important single design decision in this identity. Get this wrong and everything else fails.

Amber is not decoration. It is not a brand color in the conventional sense. It is a **signal color** — it appears when something has meaning. Think of it like a single candle in a dark room. Because most of the surface is dark, the candle matters. If you light fifty candles, none of them matter anymore.

**Amber appears on:**
- The word or phrase that is the most important in any headline
- The number in a stat that carries emotional weight
- A border on the element the user should interact with most
- An active state (nav item, open accordion)
- The CTA button — one, per section, at most

**Amber does not appear on:**
- Background fills (except as the faintest tint at 6-8% opacity)
- Decorative lines or borders that aren't meaningful
- Secondary buttons
- Body copy
- Multiple things on the same visual level

When someone scrolls this page, amber should feel like it's guiding them. Every time it appears, it should feel earned.

---

## The Dark Layers

The background is not "black." It is a family of very close, warm darks that create depth without relying on shadows or borders.

Five layers, from deepest to shallowest:

| Token | Value | Use |
|-------|-------|-----|
| `--bg-void` | #0C0C0C | The deepest layer. Used behind the hero grain, in footers. |
| `--bg-base` | #131313 | The main page background. |
| `--bg-surface` | #1A1A1A | Sections with slightly more presence. |
| `--bg-raised` | #222222 | Cards, containers, boxes. |
| `--bg-overlay` | #2C2C2C | Tags, active items, hover states. |

The subtle difference between these layers is what makes the site feel alive in darkness rather than flat. You should be able to feel depth without seeing explicit borders everywhere.

---

## Typography: The Hierarchy of Importance

Typography is the primary design material on this site. Before images, before color — type creates the hierarchy, the pace, and the personality.

**The scale principle:** Use SIZE to establish hierarchy, not weight. A 72px regular-weight headline is more sophisticated than a 36px bold one. Weight should be used for emphasis within a level, not to define the level itself.

**The five typographic roles:**

### 1. Display (Hero, Section Statements)
- Size: clamp(52px, 9vw, 96px) for hero / clamp(36px, 5vw, 60px) for section titles
- Weight: 800
- Tracking: -0.02em to -0.03em (tight — large text needs to be drawn in)
- Line height: 1.1 to 1.15
- Purpose: Stop you. Make a statement. One sentence at most.

### 2. Title (Section Headings, Card Headings)
- Size: clamp(22px, 3vw, 32px)
- Weight: 700
- Tracking: -0.01em
- Line height: 1.25
- Purpose: Name the space you're entering.

### 3. Body
- Size: 17px desktop / 16px mobile
- Weight: 400
- Tracking: 0
- Line height: 1.85
- Purpose: Be easy to read for long stretches. Never fight for attention.

### 4. Label (Section markers, captions, tags)
- Size: 11px
- Weight: 700
- Tracking: 0.15em to 0.2em
- Case: ALL CAPS
- Line height: 1.4
- Color: amber (sparingly) or muted white
- Purpose: Orient. Tell you where you are without demanding attention.

### 5. Data / Number
- Size: varies (follows display or title scale depending on context)
- Weight: 800
- Feature: `font-variant-numeric: tabular-nums` — numbers align in columns
- Color: amber for the number, muted for the unit
- Purpose: Feel precise. Feel like it came from somewhere real.

**Thai text specific notes:**
- Sarabun renders beautifully at display sizes with negative tracking
- At body size, keep tracking at 0 — Sarabun's default spacing is already optimized
- For long body text, 17-18px is the sweet spot. 16px starts to feel dense in Thai.
- Avoid 500 weight — jump from 400 straight to 600 or 700. The 500 in Sarabun is unclear.

---

## Color System: Three Registers

Think about color in three emotional registers, not individual swatches:

**Register 1 — The Dark (Presence)**
The charcoal family. This is the dominant register — where everything lives. It should feel like depth, not emptiness. Warm darks, not cold grays. The market at 3am. Where patterns live before you understand them.

**Register 2 — The Signal (Amber)**
Appears only when something matters. See the Amber section above.

**Register 3 — The Truth (Text)**
Off-white (#F0EDE8) for primary content. Not pure white — pure white is harsh on dark backgrounds and reads as cold. Slightly warm white feels like paper, like something real was written on it.

Secondary text (#888078) — for context, notes, supporting information.
Muted text (#50504A) — for labels, metadata, things that orient without demanding.

---

## Spacing: The Rhythm System

Spacing is how the site breathes. Too tight = claustrophobic. Too loose = disconnected.

Base unit: **8px**. All spacing is a multiple of 8.

The most important principle: **section padding should feel generous to the point of being surprising**. Most landing pages feel rushed — one section immediately followed by the next. Social Norms gives content room to land before the next thing arrives. The target is `120px` top and bottom per section on desktop.

**Internal rhythm within sections:**
- After a label: 12px
- After a headline: 20-24px
- After a body paragraph: 28-32px before the next block
- Between cards in a grid: 20-24px gap

**The measure (line length):**
Body copy should never exceed ~65 characters per line. This maps to roughly 640px max-width for body blocks. Long lines fatigue readers. Short lines fragment attention. 60-65 characters is where reading happens naturally.

---

## Motion: Intentional, Not Decorative

The guiding principle: **animate to reveal understanding, not to attract attention.**

Motion that helps: elements appearing as you scroll down reveals the page is alive and still has more to offer. It rewards patience.

Motion that hurts: entrances that are too fast (feels cheap), entrances that are too dramatic (distracts from content), hover effects that are identical across all interactive elements (loses meaning).

**The motion tokens:**

| Name | Duration | Easing | Use |
|------|----------|--------|-----|
| `instant` | 80ms | linear | Focus rings, state changes |
| `fast` | 160ms | ease-out | Button presses, active states |
| `normal` | 280ms | ease-out | Hover transitions, accordion |
| `slow` | 480ms | ease-out | Scroll reveals, page entrances |
| `slower` | 680ms | ease-out | Hero elements, deliberate reveals |

The easing curve for almost everything: `cubic-bezier(0.16, 1, 0.3, 1)` — a quick start that decelerates smoothly. This is the easing of things that have weight. Of things that know where they're going.

**Scroll reveal behavior:**
- Translate from 18px below to 0
- Opacity from 0 to 1
- Duration: 580ms
- Stagger between sibling elements: 80ms

---

## Layout Philosophy

### The Grid
12 columns, 24px gutters on desktop. Most content lives in a centered 1100px max-width container.

### Section Rhythm
Sections alternate between "full presence" (more content, more visual weight) and "breath" (minimal content, generous space, a single statement).

### The Light Section
There's one light section in the current layout (testimonials/FAQ). On a page this dark, a light section should feel like surfacing for air — a moment of warmth and relief. Use it deliberately, not just as variety.

---

## Mobile: A First-Class Experience

- Hero headline: 40-44px. Still powerful, not compressed.
- Section padding: 72px vertical. Still generous, just scaled.
- No horizontal scrolling, ever.
- Touch targets: minimum 48px height for all interactive elements.
- The nav on mobile: hamburger that opens a full-overlay menu.
- Cards: full-width, stacked. No grids below 640px.
- Body text: 16px minimum. Never smaller.

---

## What the Site Is Not

- **Not aggressive.** No countdown timers, no "LIMITED SPOTS," no false urgency.
- **Not cluttered.** Empty space is not wasted space.
- **Not imitative.** Not trying to look like Binance, TradingView, or any other trading platform.
- **Not corporate.** The warmth comes from a real human made this.
- **Not generic Thai landing page.** No default Thai web color palettes.

---

## Ecosystem Architecture

```
/ .............. Home       — Atmosphere, positioning, direction
/mentorship .... Mentorship — Full course detail, schedule, student stories
/advanced ...... Advanced   — The flagship. Wyckoff depth. The journey.
/about ......... About      — Liew's story. Honest. Human. Not a resume.
/free .......... Free       — Basic SNS PDF download + community entry
/wwmi .......... WWMI       — Collab show page (Phase 2)
/community ..... Community  — What ชาวนอร์ม means (Phase 3)
```

---

## The Single Test

After every design decision, ask:
**Does this feel like Social Norms — or does it feel like it could be anyone?**

If the answer is "it could be anyone" — change it.

---

*This document is a living reference. Update it when the brand evolves. Every future page, component, and piece of content should be able to trace its design decisions back here.*
