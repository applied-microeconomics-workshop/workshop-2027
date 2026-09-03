# III Workshop 2027 — website

Website for **Incentives, Institutions, and Innovation: Workshop for Young
Researchers in Applied Microeconomics** (14–15 January 2027, University of
Lausanne).

Plain static site — no build step. Edit `index.html`, push, done.

## Status

- Repo created and pushed: https://github.com/annamariahalewska/workshop-2027
- GitHub Pages is **not enabled yet** — still deciding whether this should
  live as a subpage of an existing website instead. Once decided, either:
  - enable Pages on this repo (see below), or
  - copy `index.html`, `style.css`, and `img/` into the target site instead.

## Publish on GitHub Pages (if used)

Repo is already created and pushed. To go live, on GitHub:
**Settings → Pages → Build and deployment →
Source: “Deploy from a branch” → Branch: `main`, folder `/ (root)` → Save.**

The site goes live a minute later at
`https://annamariahalewska.github.io/workshop-2027/`.

## Updating content

| Section | Where | What to do |
|---|---|---|
| Call for papers | `index.html`, `<section id="cfp">` | Deadline (15 Oct 2026) and decision date (mid-Nov 2026) are filled in; update if dates change |
| Program | `index.html`, `<section id="program">` | Replace placeholder with one `<table>` per day once speakers are confirmed |
| Keynote photo | `keynote-card` div in `<section id="keynotes">` | Drop image in `img/`, uncomment the `<img>` line |
| SNSF logo | `<p class="funding">` in `<footer>` | Drop the official logo at `img/snsf-logo.png` (or `.svg`), then uncomment the `<img>` line and delete the placeholder text above it |
| Submission form | `<section id="submit">` | Links to the Google Form for paper/abstract submissions |
| Scientific committee | `<ul class="committee">` in `<section id="committee">` | Keep alphabetical by last name |

After any edit: `git add -A && git commit -m "update" && git push` — Pages
redeploys automatically (once enabled).
