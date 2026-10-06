# Design, Build, Ship · Assignment 1 — Accelerated Prototyping

Twenty-five landing-page versions of one idea — Anees Amjad's professional
portfolio — plus a process gallery that tells the story of how the final design
was chosen.

- **Gallery (assignment submission):** https://design-build-ship-assignment-1.vercel.app
- **Final selection (v25):** https://design-build-ship-assignment-1.vercel.app/v25/

## View locally

Plain HTML and CSS (a little vanilla JavaScript in v08, v11 and v16). No build step.

```bash
open index.html                 # or:
python3 -m http.server 8000     # then visit http://localhost:8000
```

Each version lives at `vNN/index.html` and links back to the gallery.
`assets/` holds the two real images used: a PublicPath homepage screenshot
(captured 6 Oct 2026) and the Political Narrative Navigator team dashboard
(from that team's README, credited on the pages).

## Process

1. **Explore (v01–v12):** twelve deliberately different directions — layout,
   tone, era and interaction, not just colour.
2. **Converge (v13–v24):** an external AI-assisted design review (not user
   testing) suggested combining v01's editorial type, v04's contribution
   diagrams and v12's labels. Content moved to verified CV facts. Anees chose
   v21's AI-first order over v22's product-first order; v23 and v24 tested a
   fast overview against artifact-led cases.
3. **Decide (v25):** Anees selected v25, a persistent-sidebar portfolio with
   continuous case studies. The reasoning is recorded at the top of the gallery.

Late structural revisions (v14, and later v16/v18/v20 where noted) and all
factual corrections are labelled in the gallery and visible in the Git history.

## AI assistance

Built with Claude Code. Anees set the audience, content, constraints and every
direction choice, and supplied the facts. Claude wrote the HTML/CSS, proposed
and built the versions, ran the screenshot, keyboard, contrast and link checks,
and drafted the gallery notes. AI-assisted critique is labelled as such in the
gallery and is never presented as Anees's own evaluation or as user testing.
`AGENTS.md` records the content rules the agent followed.
