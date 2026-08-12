# Anchor Tree Project Context

## Immediate next task
~~Build an interactive co-founder proposal page on the website for Hakan.~~ Done. See `proposal.html`. Waiting on Hakan's response.

---

## What this is

**Anchor Tree** is a media and production company based in The Hague, Netherlands. Currently building its first product: a video interview show. Company identity and name are settled. Show name is still being decided. "Landed" was a candidate but isn't confirmed.

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

---

## Website

**File structure:**
```
anchortree/
├── index.html          ← landing page
├── proposal.html       ← interactive co-founder proposal page for Hakan
├── logo.png            ← brand mark (ink illustration: anchor + tree + roots)
├── hakan-proposal.md   ← co-founder proposal (text)
├── landed-proposal.pdf ← co-founder proposal (designed PDF)
└── CONTEXT.md          ← this file
```

**Design language:**
- Paper aesthetic: warm cream background `#f7f3ec`, subtle SVG grain texture
- Ink palette: `--ink: #1c1a15` / `--ink-mid: #5a5448` / `--ink-dim: #9c9185`
- Rule color: `rgba(28,26,21,0.12)`
- Fonts: **Playfair Display** (headings, italic) + **EB Garamond** (body) via Google Fonts
- Brand mark: `logo.png`, detailed ink illustration, use `mix-blend-mode: multiply`
- Animations: fade-up on load, staggered, subtle
- Single-file HTML preferred

**What's not done yet:**
- Show name not confirmed ("Landed" is a candidate, not locked)
- Email capture has no backend
- No Nginx config on the droplet
- No domain connected
- No deploy pipeline

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
- Show name (still open)
- Domain / droplet IP (not shared yet)
- Backend for email capture (not decided)
- Nginx / deploy setup (not started)
