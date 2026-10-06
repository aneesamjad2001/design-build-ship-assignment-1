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

- **Intro (v21+):** "I'm Anees Amjad, a master's student in Computational
  Analysis and Public Policy at the University of Chicago. My work includes an
  internal AI assistant at Ourea Energy, a public-sector careers platform I
  co-founded, and research tools that turn complex data into usable outputs."
  (v13–v20 used the earlier intro.) Describe mechanisms, not perfect outcomes:
  scheduled ≠ always succeeded, dedup ≠ perfect uniqueness, validated ≠ reliable.
  Supporting line: "Open to AI engineering roles, startup opportunities, and
  collaboration." Links: "Explore selected work", "Get in touch".
- **PublicPath** — "Co-founder, Engineering and Data" (use consistently); one of two engineers.
  "I co-built PublicPath, a platform helping students and early-career
  candidates explore government careers. My work focused on API ingestion and
  data quality: cleaning, deduplicating, normalizing, and validating listings
  for search and filtering." Stack: Python, GitHub Actions, Supabase, Postgres.
  - Link: https://www.joinpublicpath.com, labelled "Project website" (confirmed
    by Anees). Never "try the app". While job search fails, add one short note:
    "Job search was not loading when checked on 6 Oct 2026." Do not repair it.
  - Do NOT feature "50+ APIs" or "50,000+ listings": the public code shows a
    handful of job-API sources and the Supabase backend currently does not
    resolve (checked 6 Oct 2026), so the jobs page fails to load. Daily
    scheduled ingestion via GitHub Actions is supported by the repo workflows.
  - Public commit attribution is incomplete evidence; keep the stated role and
    do not claim the repo proves authorship of every component. No repo link.
  - `assets/publicpath-home.jpg` illustrates the team's product (captured
    6 Oct 2026); it does not prove Anees's interface or backend work. Pair it
    with the ingestion/data-quality diagram and role text.
- **Ourea Brain** — BUILT and deployed internally (confirmed by Anees, 6 Oct 2026).
  Title "Ourea Brain"; subtitle "Company knowledge, accessible through Slack.";
  role "Builder · Agentic AI Intern, Ourea Energy"; status "Built and deployed
  internally". Core copy: "I built and deployed Ourea Brain, an internal AI
  assistant that brings company context into Slack. It connects information
  across Slack, Gmail, Google Docs, and meeting notes to help colleagues retrieve
  project context, identify owners, and follow up on decisions. The application
  runs on Google Cloud Run and uses Anthropic's Claude API; an early live
  deployment answered a Slack question using meeting-note context."
  Supported tech: Slack integration, Anthropic Claude API, Google Cloud Run,
  Google Workspace sources, meeting-note integration, Secret Manager credentials.
  Diagram (label "Simplified architecture"): Slack question → app on Cloud Run →
  company context + Claude API → response in Slack. Never invent vector DBs,
  embeddings, frameworks, accuracy, users, or time savings; never fake a Slack
  screenshot. Don't present digests, Granola→Asana, scheduling, or GravityBank
  as core Brain features. Keep Energy Market Intelligence separate.
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
  geospatial workflow to explore eviction-risk patterns in Chicago." Private
  repository: no link, never imply public code. No metrics; not deployed.
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
