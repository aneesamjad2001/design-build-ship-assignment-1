# AGENTS.md — Design, Build, Ship · Assignment 1

## Purpose
25 versions of a landing page for one idea, plus a gallery (`index.html`) that
tells the story of the process. The idea: Anees Amjad's professional portfolio,
which should also become the foundation of a real portfolio.

- **Audience:** AI engineering recruiters, startup teams, potential collaborators.
- **A visitor should understand:** what Anees builds, what Anees personally
  contributed, how the systems work, and how to get in touch.
- **Headline:** "I build AI tools and data products for real-world decisions."

## Content rules
Use only facts from Anees's CV (shared 6 Oct 2026), verified project materials,
or explicit statements from Anees. Never invent metrics, users, adoption,
accuracy, time savings, testimonials, screenshots, deployment status, or
employment details. No phone number on the site. Never use gendered pronouns
for Anees; write in first person.

- **Intro:** "I'm a master's student in Computational Analysis and Public Policy
  at the University of Chicago. I build AI workflows, data pipelines, and
  software across energy, public service, and research."
  Supporting line: "Open to AI engineering roles, startup opportunities, and
  collaboration." Links: "Explore selected work", "Get in touch".
- **PublicPath** — Co-founder, Engineering and Data; one of two engineers.
  "I co-built PublicPath, a platform helping students and early-career
  candidates explore government careers. My work focused on API ingestion and
  data quality: cleaning, deduplicating, normalizing, and validating listings
  for search and filtering." Stack: Python, GitHub Actions, Supabase, Postgres.
  - Link: https://www.joinpublicpath.com (custom domain served from Anees's fork
    of Tahvia127/PublicPath; same homepage as tahvia127.github.io/PublicPath).
  - Do NOT feature "50+ APIs" or "50,000+ listings": the public code shows a
    handful of job-API sources and the Supabase backend currently does not
    resolve (checked 6 Oct 2026), so the jobs page fails to load. Daily
    scheduled ingestion via GitHub Actions is supported by the repo workflows.
  - Do not link the repo as evidence of individual work (public commit history
    does not show the ingestion work under Anees's account) until Anees decides.
  - Evidence asset: `assets/publicpath-home.jpg` (live homepage, captured
    6 Oct 2026; front-end design is not claimed as Anees's work).
- **Ourea Brain** — "At Ourea Energy, I designed an internal AI knowledge system
  connecting Slack, Gmail, Google Docs, and meeting notes. The system was
  designed to help teams retrieve company context, clarify ownership and
  follow-ups, and identify information gaps." Designed, not claimed deployed.
  Private; conceptual diagrams only.
- **CLARITY** (HOPE Lab, UChicago Booth; Research Assistant) — "I built a Python
  pipeline for the CLARITY healthcare-AI project that converts de-identified
  clinical-note JSON into patient-friendly explanatory videos. The workflow
  automates narration, slide generation, and MP4 production using Microsoft
  Neural TTS." Sequence: de-identified note → explanatory content → narration
  and slides → video. No accuracy/outcome claims. No examples (not public).
- **Energy Market Intelligence** (Ourea Energy) — "Built a weekly AI-assisted
  market-intelligence workflow that filtered 50+ recurring signals across energy
  storage, utilities, and data centers into leadership updates on competitors,
  investments, and partnerships." Signals ≠ sources/articles/companies. Private.
- **Chicago Eviction Risk** — "Built an interpretable machine-learning and
  geospatial workflow to explore eviction-risk patterns in Chicago." No verified
  public repo found yet: no link. No metrics; not a deployed system.
- **Political Narrative Navigator** (team project, UChicago) — "Analyzed 2,000+
  presidential campaign speeches alongside YouGov data using AI-assisted text
  workflows." Repo: https://github.com/uchicago-2026-capp30122/political-narrative-navigator
  (Anees is a listed member). Evidence asset: `assets/pnn-dashboard.jpg`
  (team dashboard graphic from the repo README; credit the team).
- **Experience:** Ourea Energy (Agentic AI Intern, Jun 2026–present); Financial
  Health Network (Research Intern, Data Analytics, Jun 2026–present); HOPE Lab,
  UChicago Booth (Research Assistant, Mar 2026–present); PublicPath (Co-Founder,
  Engineering and Data, Mar 2026–present); PAMS (Research Associate, Machine
  Learning, Mar–Sep 2025); CERP (Analyst, May 2024–Sep 2025).
- **Education:** University of Chicago, MS Computational Analysis and Public
  Policy, expected June 2027. Lahore School of Economics, BS Economics and
  Political Science, May 2024.
- **Contact:** aneesamjad@uchicago.edu · https://github.com/aneesamjad2001 ·
  https://www.linkedin.com/in/anees-amjad/ . No CV download (no public PDF).
- No GravityBank details until supporting materials establish the contribution.

## Design direction for v13+ (external AI-assisted review, not user testing)
Combine v01 (editorial type, asymmetry, project-first), v04 (explicit individual
contribution, useful system diagrams), v12 (deliberate spacing, concise labels).
Drop: simulated terminal commands; slogans that push evidence below the first
screen; decorative maps; museum/artist language; abstract art in place of
evidence; mandatory audience selection; repeated descriptions; empty fields.
Each featured project: problem and for whom → my contribution → how it works →
evidence (real screenshot/link, or a diagram labelled conceptual) → tools.
At ~1280×800 a real project must begin beside or just below the intro.

## Constraints
- Plain HTML and CSS; optional vanilla JavaScript. No frameworks, packages, build
  step, external APIs, external fonts/CDNs, or data storage. Push back on any.
- Each version is self-contained at `vNN/index.html` with its own styles, links
  back to the gallery, and keeps assignment navigation visually separate from
  the portfolio content. Core content must work without JavaScript.
- Gallery: linked preview, hypothesis, what changed / what it inherits or
  rejects, evaluation (Anees's, or clearly attributed review input, or pending).
  Final choice stays pending until Anees chooses. Never invent feedback.
- Semantic HTML, keyboard access, visible focus, responsive, reduced motion,
  alt text. Check desktop and ~390px mobile with headless Chrome.
- Commit real work as it happens. Deploy: Vercel Hobby (auto on push to main).
