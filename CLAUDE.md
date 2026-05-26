# Migura CPA — Site

Single-page static site for Migura CPA, New Braunfels TX.
Preview URL: https://pogorman.github.io/migura-cpa/

## Stack
- Plain HTML + CSS, no build tool
- Google Fonts: Lora + DM Sans
- Hosted on GitHub Pages (main branch, root)

## Structure
- `index.html` — the entire site
- `css/styles.css` — all styles
- `images/` — served images (currently `hero.jpg`, resized to 2400px wide and ~170KB)
- `kick-off-doc/` — reference files only, not served

## Deploy
git add -A && git commit -m "your message" && git push

## Key rules
- Do not change any copy (names, phone, email, service descriptions) without being asked
- Do not add JavaScript unless explicitly requested
- Do not introduce a framework or build step
- Keep the service grid at exactly 6 tiles
- The service cards still use Unsplash photo URLs — leave those in place unless asked
- New hero/page images go in `images/`. Resize to ~2400px wide and ~80% JPEG quality before committing — full-size camera files (multi-MB) will tank page load
- Mobile breakpoint: collapse grid to 1 column at 640px

## When she's ready to go live on her real domain
Point her GoDaddy DNS to GitHub Pages:
- Add a CNAME record: `www` → `pogorman.github.io`
- Add a file named `CNAME` at the repo root containing her domain (e.g. `www.miguracpa.com`)
- Enable custom domain in repo Settings → Pages
