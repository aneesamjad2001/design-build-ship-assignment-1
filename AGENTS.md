# AGENTS.md — Design, Build, Ship · Assignment 1

## Purpose
Build 25 versions of a landing page for one idea, plus a gallery that tells the
story of the process. The idea: Anees Amjad's professional portfolio.

- **Audience:** AI engineering recruiters, startup teams, potential collaborators.
- **A visitor should understand:** what Anees builds and what Anees personally
  contributed to each project, then be able to reach out (GitHub, LinkedIn, email).
- **Positioning:** "I build AI tools and data products for real-world decisions."

## Content (use only this; do not invent)
- Intro: "I'm Anees Amjad, a graduate student in Computational Analysis and Public
  Policy at the University of Chicago. My work spans AI workflows, public-sector
  software, and applied machine learning."
- PublicPath: Co-founder, Engineering and Data. Built the platform as one of two
  engineers, working on API ingestion and data-quality workflows using Python,
  GitHub Actions, Supabase, and Postgres. What it is (from its site,
  https://tahvia127.github.io/PublicPath/): "a nonprofit platform" that "helps
  students and early-career candidates discover, navigate, and land roles in
  government, from city hall to Capitol Hill." Features: Discover, Navigate,
  Match, Get Hired; weekly digest of 5–10 hand-picked roles. Five-person team.
  (Site lists Anees as "Tech Co-lead"; use Anees's own title above unless told.)
- Ourea Brain: Designed an internal AI knowledge system connecting company
  information across communication and document sources.
- Energy Market Intelligence: Built a weekly AI-assisted workflow filtering
  energy-storage and related market signals into leadership updates.
- Chicago Eviction Risk: Built an interpretable machine-learning and geospatial
  workflow exploring Chicago eviction risk patterns.
- Contact: GitHub https://github.com/aneesamjad2001 · LinkedIn
  https://www.linkedin.com/in/anees-amjad/ · Email aneesamjad@uchicago.edu

Never invent metrics, testimonials, project links, screenshots, employment
details, or user feedback. If content is missing, leave it out and say so.

## Constraints
- Plain HTML and CSS; optional vanilla JavaScript. No frameworks, packages, build
  step, external APIs, external fonts/CDNs, or data storage. Push back on any.
- `index.html` = process gallery. Each version lives at `vNN/index.html`, is
  self-contained, and links back to the gallery.
- Gallery: linked preview per version, short process note, final choice marked
  once Anees picks it.
- Each version's note records the design intent as a **hypothesis**. Evaluation
  stays "pending" until Anees has actually reviewed it — never write it on Anees's behalf.
- Go wide first (layout, audience, mood, era, tone — not just colors/fonts), then
  converge by v20–v25.
- Semantic HTML, keyboard-accessible links, visible focus states, responsive.
- Commit real work as it happens; one version per session step unless asked.
- Deploy target: Vercel free Hobby plan (static files, no config needed).
