# Anchor Tree — Landing Page Brief

## Context
Anchor Tree is a student production company based in The Hague. Two co-founders, Noe and Hakan. Currently producing a video interview show (name TBD) and a political podcast for a third party. The company is young, scrappy, and real — not corporate. The landing page should feel like something students built because they actually wanted to, not because they had to.

Design system is already established in `index.html`. Use the same tokens.

---

## Design System (from index.html)

```css
--paper:   #f7f3ec   /* warm cream background */
--ink:     #1c1a15   /* near-black, all headings and strong text */
--ink-mid: #5a5448   /* body text */
--ink-dim: #9c9185   /* labels, captions, muted elements */
--rule:    rgba(28,26,21,0.12)  /* dividers and borders */
```

**Fonts:** Playfair Display (headings, italic) + EB Garamond (body) via Google Fonts
**Logo:** `logo.svg` — use inline SVG, `mix-blend-mode: multiply`
**Texture:** paper grain via SVG filter on body background
**Animation:** fade-up on load and scroll, staggered, subtle
**Single file HTML** — no separate CSS/JS files

---

## Page Structure

### 1. Nav (minimal)
- Logo mark (SVG inline, ~28px tall) + wordmark "Anchor Tree"
- Right side: one link — "Work with us" anchors to contact section
- Sticky, transparent background, border-bottom appears on scroll
- No hamburger menu — keep it flat

---

### 2. Hero
**Headline (Playfair Display, large, italic):**
> *We make things.*

**Sub (EB Garamond, ink-mid):**
> A production company from The Hague. Video, podcasts, events — for students, by students.

**CTA:** Two links side by side — "See our work" (anchors to productions) and "Work with us" (anchors to contact). Styled as text links with an underline, not buttons.

---

### 3. What We Do
**Label:** `What we do`

Three items in a row (stack on mobile). Each is a simple card — label + one line description. No icons, no illustrations.

- **Video** — Interview series, short-form content, event coverage
- **Podcasts** — Full production from recording to distribution
- **Events** — On-the-ground filming and production support

---

### 4. Productions
**Label:** `Our work`

**Headline:** *Currently in production.*

Two cards side by side (stack on mobile):

**Card 1 — The Show (name TBD)**
- Tag: `Video series`
- Description: A street interview show set in The Hague. Real people, real cafés, real stories. How did you end up here?
- Status badge: `In production` — small, subtle, ink-dim coloured dot + text

**Card 2 — Podcast (name TBD)**
- Tag: `Podcast`
- Description: A political interview podcast. Produced by Anchor Tree.
- Status badge: `In production`

Cards should be minimal — border `1px solid var(--rule)`, no shadows, paper background, hover lifts slightly (`transform: translateY(-2px)`).

---

### 5. Who We Are
**Label:** `The team`

Two columns, one per person. Keep it short and human.

**Noe**
> Interviews, outreach, production. Good with people, better with a mic.

**Hakan**
> Technical direction, editing, post-production. Makes it look like something.

No headshots for now. Just names and one-liners.

---

### 6. Work With Us
**Label:** `Work with us`

**Headline:** *Got something to make?*

**Body (EB Garamond, ink-mid):**
> We're a small team and we work with people we find interesting. If you have a podcast, a video series, an event, or just an idea — tell us about it.

**What we offer:**
Three lines of plain text (not a list):
- Podcast production — recording, editing, distribution
- Video — interviews, event coverage, short-form content
- Production support for student associations and events

**CTA:** A simple email link — `hello@anchortree.com` — styled large, Playfair Display italic, with a subtle underline. No form needed.

---

### 7. Footer
- Logo mark (small, ~20px)
- "Anchor Tree — The Hague"
- "© 2026"
- Right side: Instagram link placeholder (`@anchortree`) — text only, no icon

---

## Tone
- Direct, no fluff
- No corporate language ("solutions", "leverage", "deliverables")
- Talks to students as peers, not as clients
- A little rough around the edges is fine — this is a student company, not an agency

## What this page is NOT
- Not a coming soon page (that's index.html — can be retired or repurposed)
- Not trying to be Spotify or a big agency
- Not heavy on visuals — the writing does the work

---

## Files in the repo
```
anchortree/
├── index.html          ← current coming-soon page (can be replaced)
├── proposal.html       ← interactive co-founder proposal for Hakan
├── logo.svg            ← vector logo (USE THIS, not logo.png)
├── logo.png            ← original ink illustration (reference only)
├── CONTEXT.md          ← full project context
└── landing-brief.md    ← this file
```
