# Anchor Tree Project Context

## Immediate next task
~~Build an interactive co-founder proposal page on the website for Hakan.~~ Done. See `proposal.html`. Waiting on Hakan's response.

~~Replace the coming-soon page with the real company landing page.~~ Done. See `index.html`, built from `landing-brief.md`.

---

## What this is

**Anchor Tree** is a student production company based in The Hague, Netherlands. Two co-founders, Noe and Hakan. Young, scrappy, real, not corporate. Currently producing a video interview show (name TBD, "Landed" was a candidate but isn't confirmed) and a political interview podcast (name TBD) produced for a third party.

---

## The show

**Format:** 10 to 20 minute interviews filmed in a different café in The Hague every episode. Long-form cut for YouTube, each episode also cut into 5 to 6 short clips for TikTok.

**Concept:** Ask people how they ended up where they are: career, life, path. Students and working people. No politicians. Mix of local Dutch and the massive international community in The Hague (diplomats, ICC staff, UN workers, lawyers, NGO people).

**Reference:** Career Ladder by Max Klymenko on TikTok. Similar format, different city and angle.

**Why The Hague:** One of the most internationally diverse cities in Europe. Essentially zero local content creators. Nobody is telling these stories. Wide open market.

**Three things happen in every episode:**
- You discover a café in The Hague
- You discover a person
- You learn something from their story

---

## The team

**Noe**, co-founder. Interviewer, front of camera, guest outreach, cold calls, sales. Good with people, learns fast, confident on camera. Based in The Hague.

**Hakan**, co-founder. Technical side of shoots, editing, post-production. Student, has time. Equal partner. Noe and Hakan are close friends, have filmed a podcast together before.

---

## Production plan

- **2 shooting days per month**
- **3 episodes per shoot day = 6 episodes per month**
- **Release 5, keep 1 in the bank** as a buffer
- Edit time: ~3 to 4 hours per episode, ~20 to 25 hours/month for Hakan
- First shoot: September or October 2026
- Launch: after first 3 episodes are cut and ready

**Content output per month:** 5 YouTube episodes + ~25 to 30 TikTok clips

---

## Infrastructure

- **Company:** Anchor Tree
- **Hosting:** DigitalOcean droplet
- **Repo:** https://github.com/kebabmax/anchortree.git
- **SSH key:** `~/.ssh/id_ed25519`, linked to droplet
- **Connect to server:** `ssh root@<droplet-ip>`
- **Domain:** anchortree.net (DNS at Gandi). Apex points at the droplet. HTTPS via Certbot in progress, `www` needed a DNS fix (Gandi's Web Redirection feature was pointing it at Gandi's own parking service instead of the droplet)

---

## Website

**File structure:**
```
anchortree/
├── index.html          ← company landing page (nav, hero, what we do, productions, team, contact)
├── proposal.html       ← interactive co-founder proposal page for Hakan
├── logo.svg            ← vector brand mark, traced from logo.png, used inline via <symbol>/<use>
├── logo.png            ← original ink illustration (anchor + tree + roots), reference only
├── hakan-proposal.md   ← co-founder proposal (text)
├── landed-proposal.pdf ← co-founder proposal (designed PDF)
├── landing-brief.md    ← brief this landing page was built from
└── CONTEXT.md          ← this file
```

**Design language:**
- Paper aesthetic: warm cream background `#f7f3ec`, subtle SVG grain texture
- Ink palette: `--ink: #1c1a15` / `--ink-mid: #5a5448` / `--ink-dim: #9c9185`
- Rule color: `rgba(28,26,21,0.12)`
- Fonts: **Playfair Display** (headings, italic) + **EB Garamond** (body) via Google Fonts
- Brand mark: `logo.svg` inline (nav ~28px, footer ~20px), `mix-blend-mode: multiply`. `logo.png` kept for reference only
- Favicon: small square crop of the mark (centered on the anchor), embedded as base64 PNG in `index.html`
- Animations: fade-up on load and on scroll (staggered, IntersectionObserver), subtle
- Single-file HTML preferred

**What's not done yet:**
- Show name not confirmed ("Landed" is a candidate, not locked); podcast name also TBD
- No Nginx config confirmed working end-to-end on the droplet yet
- HTTPS certificate not yet issued (DNS fix for `www` just applied, re-run Certbot once it propagates)
- No confirmed deploy pipeline (cron-pull instructions were given, not confirmed run)

---

## Brand

- **Company name:** Anchor Tree
- **Mark:** Ink illustration. Tree canopy grows from anchor body, root system spreads below. Tattoo/etching style, black on white.
- **Feel:** Paper-like, analog, grounded, minimal, human
- **Voice:** Direct, no corporate language, a bit rough around the edges in a good way
- **Not** Serenzer-branded. Its own identity

---

## Business model (early thinking)

- Start: build audience through the show
- Revenue eventually: brand deals, sponsored episodes, event production in The Hague
- The Hague international community (expats, diplomats, students) is underserved for events and experiences. Event production is a natural adjacent business
- No outside funding planned, ~€20k max budget to get started

---

## What to ask Noe if unclear
- Show name and podcast name (both still open)
- Whether Nginx/cron-pull deploy setup on the droplet was actually completed
- Real Instagram handle to confirm `@anchortree` in the footer is correct
