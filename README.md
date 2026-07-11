# Ayush Harshit — Portfolio

A single-page, production-ready developer portfolio for **Ayush Harshit** — Computer Science Engineer, Full Stack Developer, Cybersecurity Enthusiast, and AI/ML learner. Built as a distraction-free, dependency-free static site so it runs instantly, anywhere, with zero build step.

## What's inside

```
portfolio/
├── index.html        ← everything: markup, styles, and behavior
├── assets/
│   └── profile.jpg   ← headshot used in the hero section
└── README.md
```

## Design direction

- **Theme:** dark-first "threat radar" identity — deep navy/charcoal surfaces, a cyan-teal "signal" accent, and an amber highlight for callouts. A rotating radar sweep renders on `<canvas>` behind the hero, tying the visual language back to ThreatLens without leaning on generic neon-on-black clichés.
- **Type:** Space Grotesk for display headings, Inter for body copy, JetBrains Mono for terminal/label details (eyebrows, tags, stats).
- **Motion:** scroll-triggered reveals (IntersectionObserver), a typing effect cycling through your roles, animated skill bars, a scanning-line effect over the profile photo, and a scroll progress bar — all restrained and purposeful, not stacked for effect.
- **Light mode:** fully implemented via a `data-theme` attribute and CSS variables; toggle persists with `localStorage`.

## Sections included

Hero · About · Education (academic record table: Matriculation, Intermediate, B.Tech with CGPA/%) · Skills (tabbed: Frontend / Backend / Database / Cybersecurity / AI-ML / DevOps) · Experience (Secure Elements internship + SmartBridge MERN internship, bullets sourced from your CV) · Projects (filterable: All / Security / Web / Internship) · GitHub stats + contribution graph · Timeline (2023–2027) · Certifications & Achievements (Quantum Computing Bootcamp, NPTEL Industry 4.0) · Testimonials & Blog placeholders · Contact (info + working `mailto:` form, downloadable resume) · Footer.

## Before you publish — checklist

1. **Resume:** `assets/resume.pdf` already contains your uploaded CV, and the "Download Resume" button links to it directly. Replace the file with a newer version any time — same filename, no code changes needed.
2. **Profile photo:** `assets/profile.jpg` is already cropped and optimized (800×1000). Swap it for a different shot any time — same filename, same aspect ratio works best.
3. **GitHub username:** the contribution graph and live stats (repos/followers/following) pull from `Ayushharshit1` via `ghchart.rshah.org` and the public GitHub API. No key needed — update the username in `index.html` if it ever changes.
4. **Contact form:** currently opens the visitor's email client via `mailto:` (no backend required). To capture submissions instead, wire the form to a service like Formspree, Web3Forms, or a small serverless function, and replace `handleContactSubmit()`.
5. **Certifications/testimonials placeholders:** a few cards are intentionally marked "In Progress" / "Coming Soon" — replace with real content as you earn certifications and collect testimonials.
6. **SEO:** update the `<title>` and `<meta name="description">` tags if your tagline or focus changes.

## Deploying to Vercel

**Option A — drag and drop (fastest):**
1. Go to https://vercel.com/new
2. Drag the `portfolio` folder onto the page (or zip and upload it).
3. Vercel auto-detects it as a static site — no build command needed. Deploy.

**Option B — via GitHub (recommended for ongoing edits):**
1. Push this folder to a new GitHub repository.
2. In Vercel, click **New Project** → **Import Git Repository** → select the repo.
3. Framework preset: **Other** (static). Build command: leave empty. Output directory: `.` (root).
4. Deploy — Vercel gives you a live URL immediately, and redeploys automatically on every push.

**Option C — Vercel CLI:**
```bash
npm i -g vercel
cd portfolio
vercel --prod
```

## Local preview

No install required — just open `index.html` in a browser, or serve it locally:

```bash
cd portfolio
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Accessibility & performance notes

- Semantic landmarks (`header`, `nav`, `section`, `footer`) and visible focus states on interactive elements.
- Images use `loading="eager"` only for the hero photo; the contribution graph is `loading="lazy"`.
- All animation is CSS/JS-driven with no layout-shifting web fonts blocking render (fonts load via `<link>` with `preconnect`).
- No external JS frameworks — nothing to install, nothing to go out of date.
