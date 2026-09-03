# III Workshop 2027 — website

Website for **Incentives, Institutions, and Innovation: Workshop for Young
Researchers in Applied Microeconomics** (14–15 January 2027, University of
Lausanne).

Plain static site — no build step. Edit `index.html`, push, done.

## Publish on GitHub Pages (one-time setup)

```bash
cd /Users/ahalewsk/Documents/conference/website
git init
git add .
git commit -m "Workshop website: initial version"
# create the repo on GitHub (public), e.g. iii-workshop-2027:
gh repo create iii-workshop-2027 --public --source=. --push
```

Then on GitHub: **Settings → Pages → Build and deployment →
Source: “Deploy from a branch” → Branch: `main`, folder `/ (root)` → Save.**

The site goes live a minute later at
`https://<your-username>.github.io/iii-workshop-2027/`.

## Updating content

| Section | Where | What to do |
|---|---|---|
| Call for papers | `index.html`, `<section id="cfp">` | Replace the dashed placeholder block with deadlines + submission instructions (comments inside mark what to include) |
| Program | `index.html`, `<section id="program">` | Replace placeholder with one `<table>` per day once speakers are confirmed |
| Keynote photos | `keynote-card` divs | Drop images in `img/`, uncomment the `<img>` line |
| Second keynote | `<div class="keynote-tbd">` in `<section id="keynotes">` | Currently "to be announced" — once confirmed, replace with a normal `keynote-card` (see the Docquier card for the pattern) |
| SNSF logo | `<p class="funding">` in `<footer>` | Drop the official logo at `img/snsf-logo.png` (or `.svg`), then uncomment the `<img>` line and delete the placeholder text above it |
| Mailing list | `<section id="mailing-list">` | Currently a `mailto:` subscribe link; swap in a Google Form iframe if you prefer structured sign-ups |

After any edit: `git add -A && git commit -m "update" && git push` — Pages
redeploys automatically.
