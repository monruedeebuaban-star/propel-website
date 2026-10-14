# Propel Career Solutions — Website

This repository **is** the live website at **https://propelcareer.net** (hosted on GitHub Pages).
Whatever is on the `main` branch is what the public sees.

## How to make a change (for Claude)
1. **Always `git pull` first** — two people share this repo, so get the latest before editing.
2. Edit the relevant `.html` file(s) directly in this folder.
3. Commit and push to `main`:
   ```
   git add -A && git commit -m "describe the change" && git push origin main
   ```
4. It goes live automatically in about **1 minute**.

After pushing, you can confirm the change is live with:
`curl -s "https://propelcareer.net/?cb=$RANDOM" | grep "something you changed"`

## The pages
- `index.html` — **Home page** (bilingual EN/TH; the editable text lives in the `COPY` block in the `<script>` at the bottom of the file)
- `solutions.html` — Solutions overview
- `leadership-training-thailand.html`, `sales-training-thailand.html`, `recruitment-training-thailand.html`, `customer-service-training-thailand.html`, `ai-training-thailand.html`, `custom-corporate-training-thailand.html` — the 6 solution pages
- `how-propel-works.html`, `performance-mentoring.html`, `about.html`, `insights.html`, `contact.html` — supporting pages
- `talent-journey.html` — Talent Journey landing
- `assets/` — logo, images, and `solution.css` (shared styles for every page **except** the homepage, which has its own styles inline)

## Notes
- **Brand:** purple `#463A6B`, gold `#C3A35C`. Fonts: Montserrat (English) + Prompt (Thai).
- If you edit `assets/solution.css`, also bump its version number in each page's
  `<link rel="stylesheet" href="assets/solution.css?v=N">` (increase `N`) so returning visitors load the new styles instead of a cached copy. (This is why some computers can briefly show an old version after a change — their browser cached the old file.)
- The contact form currently opens a pre-filled email (Formspree not wired yet).
- **Do not delete `CNAME`** — it must stay as `propelcareer.net` or the custom domain breaks.
- Keep changes small and descriptive in commit messages so both editors can follow the history.
