# Migura CPA — Site Kickoff

You are building and deploying a minimal, production-ready static website for Migura CPA, a certified public accounting firm in New Braunfels, Texas.

## Your first tasks

1. Initialize a new git repo in the current directory
2. Read the reference file at `kick-off-doc/migura-cpa.html` — this is the approved design. Treat it as the source of truth for layout, copy, color, and structure.
3. Scaffold the project (see stack below)
4. Build the site faithfully from the reference HTML
5. Write a `CLAUDE.md` at the repo root (see spec below)
6. Create a public GitHub repo named `migura-cpa` using the GitHub CLI and push to it
7. Enable GitHub Pages on the repo and output the live preview URL

---

## Stack

- **Framework**: plain HTML/CSS — no build tool, no bundler, no framework needed. This is a single-page static site.
- **Structure**:
  ```
  /
  ├── index.html
  ├── css/
  │   └── styles.css
  ├── kick-off-doc/
  │   └── migura-cpa.html   ← reference only, do not serve
  └── CLAUDE.md
  ```
- **Fonts**: Google Fonts — Lora (400, 500, italic) + DM Sans (300, 400, 500). Already in the reference file.
- **Images**: Use the Unsplash URLs already in the reference HTML. Each `<img>` should have a meaningful `alt` attribute and the `onerror` fallback from the reference.
- **No JavaScript** beyond what's already in the reference (there is none). Keep it pure HTML/CSS.

---

## Design fidelity requirements

- Match the reference exactly: nav, photo strip, intro section, 3×2 service grid, footer
- Sticky nav with the phone number CTA as a tap-to-call link (`tel:`)
- All six service tiles must have: a photo, a title, and a one-line description
- Footer must have: map link, phone link, email link, copyright
- The site must be fully responsive — the service grid should collapse to 1 column on mobile
- Smooth fade-up entrance animations on page load (CSS only, already in reference)

---

## Content (do not change any of this)

**Business name**: Migura CPA  
**Location**: New Braunfels, Texas  
**Phone**: (830) 609-9027  
**Email**: info@miguracpa.com  
**Tagline**: "Taxes and accounting, done right the first time."  
**Sub-copy**: "A full-service CPA practice serving individuals, families, and small businesses across the New Braunfels area."

**Services** (in order, 3×2 grid):
1. Individual taxes — W-2, 1099, and complex personal returns filed accurately and on time.
2. Business taxes — S-Corp, LLC, and sole proprietor filings handled with care.
3. Tax planning — Year-round strategy to reduce what you owe next April.
4. Bookkeeping — Monthly or quarterly books for small businesses and LLCs.
5. Financial planning — Retirement, savings goals, and long-term financial guidance.
6. Payroll services — Payroll setup and processing for small business owners.

---

## GitHub repo + Pages deployment

- Use the **GitHub CLI** (`gh`) to create and deploy. If `gh` is not installed, install it first.
- Create a public repo: `gh repo create migura-cpa --public --source=. --remote=origin --push`
- Enable GitHub Pages from the `main` branch root: `gh api -X PUT repos/{owner}/migura-cpa/pages -f source[branch]=main -f source[path]=/`
- After enabling Pages, output the live URL — it will be `https://{your-github-username}.github.io/migura-cpa/`
- Note: GitHub Pages can take 1–2 minutes to go live after first enable. Let the user know.

---

## CLAUDE.md to write

Once the repo is scaffolded, create a `CLAUDE.md` at the root with the following content:

```markdown
# Migura CPA — Site

Single-page static site for Migura CPA, New Braunfels TX.
Preview URL: https://{owner}.github.io/migura-cpa/

## Stack
- Plain HTML + CSS, no build tool
- Google Fonts: Lora + DM Sans
- Hosted on GitHub Pages (main branch, root)

## Structure
- `index.html` — the entire site
- `css/styles.css` — all styles
- `kick-off-doc/` — reference files only, not served

## Deploy
git add -A && git commit -m "your message" && git push

## Key rules
- Do not change any copy (names, phone, email, service descriptions) without being asked
- Do not add JavaScript unless explicitly requested
- Do not introduce a framework or build step
- Keep the service grid at exactly 6 tiles
- Unsplash photo URLs are intentional — do not swap them out
- Mobile breakpoint: collapse grid to 1 column at 640px

## When she's ready to go live on her real domain
Point her GoDaddy DNS to GitHub Pages:
- Add a CNAME record: `www` → `{owner}.github.io`
- Add a file named `CNAME` at the repo root containing her domain (e.g. `www.miguracpa.com`)
- Enable custom domain in repo Settings → Pages
```
