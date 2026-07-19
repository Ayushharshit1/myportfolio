# Ayush Harshit — Portfolio

A simple, single-page portfolio site for Ayush Harshit — final-year B.Tech CSE student, Full Stack Developer intern, and cybersecurity enthusiast. Plain HTML/CSS/JS, no build tools, no frameworks — easy to read, easy to edit, easy to deploy.

## What's inside

```
portfolio/
├── index.html        ← all markup, styles, and behavior
├── assets/
│   ├── profile.jpg   ← headshot used in the hero section
│   └── resume.pdf    ← downloadable resume (linked from the hero button)
└── README.md
```

## Sections

Hero · About · Education (academic record table) · Skills (grouped tags: Frontend, Backend, Database, Cybersecurity, AI/ML, Tools) · Experience (Secure Elements + SmartBridge internships) · Projects (filterable: All / Security / Web / Internship) · GitHub stats + contribution graph · Timeline (2023–2027) · Certifications & Achievements · Contact (info + working `mailto:` form) · Footer.

## Before you publish

1. **Resume:** `assets/resume.pdf` already has your uploaded CV. Swap the file any time — same filename, no code changes needed.
2. **Photo:** `assets/profile.jpg` is already cropped for the circular hero photo.
3. **GitHub username:** stats and the contribution graph pull from `Ayushharshit1` — update in `index.html` if it changes.
4. **Contact form:** opens the visitor's email client via `mailto:`. To collect submissions instead, wire it up to a service like Formspree or Web3Forms.

## Deploying to Vercel

**Drag and drop (fastest):**
1. Go to https://vercel.com/new
2. Drag the `portfolio` folder onto the page.
3. Vercel auto-detects it as a static site — deploy, no build step needed.

**Via GitHub:**
1. Push this folder to a GitHub repo.
2. In Vercel: New Project → Import Git Repository → select the repo.
3. Framework preset: Other (static). Build command: empty. Output directory: `.`
4. Deploy.

## Local preview

Just open `index.html` in a browser, or:
```bash
cd portfolio
python3 -m http.server 8000
# visit http://localhost:8000
```
