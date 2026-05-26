# Migura CPA — Warm Editorial Concept Kickoff

You are building and deploying a minimal static website for Migura CPA. This is the **warm editorial concept** — cream background, serif type, horizontal service rows with thumbnails. It is one of three design options being built in parallel for client review. Each lives in its own GitHub repo with its own GitHub Pages URL.

## Your first tasks

1. Initialize a new git repo in the current directory
2. Read the reference file at `kick-off-doc/migura-cpa-warm.html` — this is the approved design. Treat it as the source of truth for layout, copy, color, and structure.
3. Scaffold the project (see stack below)
4. Build the site faithfully from the reference HTML
5. Write a `CLAUDE.md` at the repo root (see spec below)
6. Create a public GitHub repo named `migura-cpa-warm` and push to it
7. Enable GitHub Pages and output the live preview URL

---

## Stack

- Plain HTML/CSS — no build tool, no bundler, no framework
- **Structure**:
  ```
  /
  ├── index.html
  ├── css/
  │   └── styles.css
  ├── kick-off-doc/
  │   └── migura-cpa-warm.html   ← reference only, do not serve
  └── CLAUDE.md
  ```
- **Fonts**: Google Fonts — Lora (400, 500, italic variants) + DM Sans (300, 400, 500)
- **Images**: Use the Unsplash URLs already in the reference HTML. Keep all `onerror` fallbacks.
- No JavaScript

---

## Design fidelity requirements

- Cream background (`#f7f4ef`) throughout
- Sticky nav: italic serif brand name left, phone number right
- Hero: full-bleed photo left half, intro text right half (50/50 split)
- Gold bordered badge above the headline in the hero
- Services as horizontal rows (not a grid) — each row has: italic number, title + description, small thumbnail on the right
- Dark brown footer (`#1e1610`) with italic serif brand name
- Fully responsive: stacks to single column at 640px
- Fade-up entrance animations on load (CSS only)

---

## Content (do not change)

**Business name**: Migura CPA
**Location**: New Braunfels, Texas
**Phone**: (830) 609-9027
**Email**: info@miguracpa.com
**Tagline**: "Taxes and accounting, done right the first time."
**Sub-copy**: "A full-service CPA practice serving individuals, families, and small businesses across the New Braunfels area."

**Services** (4 rows, in order):
1. Taxes — Individual, self-employed, and business returns — filed accurately and on time.
2. Tax planning — Year-round strategy to reduce what you owe next April.
3. Bookkeeping — Monthly or quarterly books for small businesses and LLCs.
4. Financial planning — Retirement, savings goals, and long-term financial guidance.

---

## GitHub repo + Pages deployment

- Create public repo: `gh repo create migura-cpa-warm --public --source=. --remote=origin --push`
- Enable GitHub Pages: `gh api -X PUT repos/{owner}/migura-cpa-warm/pages -f source[branch]=main -f source[path]=/`
- Live URL will be: `https://{your-github-username}.github.io/migura-cpa-warm/`
- GitHub Pages takes 1–2 minutes to go live after first deploy. Let the user know.

---

## CLAUDE.md to write

```markdown
# Migura CPA — Warm Editorial Concept

Preview URL: https://{owner}.github.io/migura-cpa-warm/

One of three design options for client review. Cream background, serif type, horizontal service rows.

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
- Do not change any copy without being asked
- Do not add JavaScript unless explicitly requested
- Do not introduce a framework or build step
- Keep exactly 4 service rows
- Unsplash photo URLs are intentional — do not swap them
- Cream background: #f7f4ef — do not change to white
- Mobile breakpoint: single column at 640px

## When ready for the real domain
- Add CNAME record in GoDaddy: `www` → `{owner}.github.io`
- Add a `CNAME` file at repo root containing her domain
- Enable custom domain in repo Settings → Pages
```
