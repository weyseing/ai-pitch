# ai-pitch

This repo holds the prep for a pitch in **WFH's internal AI Challenge** — a Shark
Tank–style event. The job: take a *real* problem somewhere in the business and
pitch an AI solution for it. The bar is "does it make us better, faster, or
sharper" — not technical sophistication.

## The brief (from Mark Choo, the organiser)
- **Event:** Thursday, 4 June 2026, 2:00–3:30pm sharp (wraps before the PSC EOM).
- **Format:** 5-minute pitch per person, covering four things:
  **problem → solution → impact → how doable.**
- **Judges:** Dorcas, Jeremy (incoming Head of AI), plus a live room vote.
- **Prize:** RM1,500 cash. **Doubled to RM3,000** if the solution is still in use
  by the end of 2026 — so favour ideas that can actually ship and stick, not just
  demo well.
- **Scope:** Any area of any brand under WFH — automate something painful, replace
  a manual process, build a smarter dashboard, sharpen how we serve members, or
  free up time for you or your department.
- **Framing that matters:** "You do not need to be a tech person to win." Spot a
  real problem + a sensible idea of how AI fixes it = enough. The build gets
  figured out together if it lands.

## What "good" looks like here
- A real, specific WFH problem someone actually has — not a generic "AI could…".
- Impact stated in concrete numbers wherever possible.
- A solution that's credibly shippable and durable (remember the year-end double).
- A 5-minute story, not a feature list. Lead with the problem and the impact.
- Any prototype or demo is a supporting prop for the pitch — keep it tiny.

## Current pitch — "Ops Brain" (Google NotebookLM)
Load WFH's SOPs/policies/reports into NotebookLM once → **ask** it (cited answers) and
**digest** long reports; the same source also makes podcasts, slides, infographics.
Angle: zero build, runs in Google Workspace (our data isn't used to train models),
pilot one ops team for 2 weeks → still running by year-end.

- Deck: `slides/pitch_deck.html` (10 slides, ~5 min) — open in a browser. **Self-contained
  single file**: all images are base64-embedded at build (so it's portable and the html2canvas
  export isn't tainted). Source images still live in `slides/assets/`.
- Chrome = `example.html` engine + Claude Design "AI Workshop Deck" layouts: a bottom
  bar (Prev / Next / **Present** fullscreen / **Export PDF**), dots + counter, and the
  PSC × Tribe dual logos top-left of every slide. Nav: bar buttons, arrow keys, or
  `?slide=N`. **Export PDF** = one-click html2canvas→jsPDF download in full colour (like
  `example.html`; needs internet for the two CDN libs at click time) → falls back to browser
  print (`@media print` + `print-color-adjust:exact`, so colour survives) if offline.
  Each slide uses a distinct layout (s-cover / s-compare / s-section / s-flow / s-types /
  s-table / s-risks / s-proof / s-close); slide images live in `assets/` (cover gym+pickleball,
  slide 3 `psc-court.jpg`, slide 8 `psc-social.jpg`, slide 9 `demo-shot.jpg` = real NotebookLM
  proof screenshot). Slide 10 (the ask) is framed as a per-department rollout.
- Before pitching: drop in **real numbers** (slide 6 figures are illustrative), confirm
  the **presenter name** on the cover, and build the **live demo** (two NotebookLM
  notebooks — PSC FAQ+Pricing, and the May EOM report).
