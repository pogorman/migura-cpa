# Migura CPA — Dark Concept Kickoff

You are building and deploying a minimal static website for Migura CPA. This is the **dark concept** — near-black background, large lightweight type hero, three tall vertical service panels with photos. It is one of three design options being built in parallel for client review. Each lives in its own GitHub repo with its own GitHub Pages URL.

## Your first tasks

1. Initialize a new git repo in the current directory
2. Read the reference file at `kick-off-doc/migura-cpa-dark.html` — this is the approved design. Treat it as the source of truth for layout, copy, color, and structure.
3. Scaffold the project (see stack below)
4. Build the site faithfully from the reference HTML
5. Write a `CLAUDE.md` at the repo root (see spec below)
6. Create a public GitHub repo named `migura-cpa-dark` and push to it
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
  │   └── migura-cpa-dark.html   ← reference only, do not serve
  └── CLAUDE.md
  ```
- **Fonts**: Google Fonts — DM Sans (300, 400, 500) only. No serif font.
- **Images**: Use the Unsplash URLs already in the reference HTML. Keep all `onerror` fallbacks.
- No JavaScript

---

## Design fidelity requirements

- Near-black background (`#111111`) throughout
- Sticky nav: all-caps brand name left, phone number right
- Hero: text only, no image — large lightweight type (font-weight 300), gold accent on "Taxes."
- Three equal-width vertical panels side by side, each with:
  - Photo top half (200px tall, darkened with opacity: 0.7)
  - Title + description bottom half
  - Each panel has a subtly different dark background tint
- Contact bar below panels: "Get in touch" label + phone + email + location
- Minimal footer: brand name left, copyright right
- Fully responsive: panels stack to single column at 640px
- Fade-up entrance animations on load (CSS only)
- Photo hover effect: opacity increases to 0.85, subtle scale

---

## Content (do not change)

**Business name**: Migura CPA
**Location**: New Braunfels, Texas
**Phone**: (830) 609-9027
**Email**: info@miguracpa.com
**Hero headline**: "Taxes. Bookkeeping. Financial planning."
  — "Taxes." is bold and gold, the rest is weight 300 white
**Sub-copy**: "A full-service CPA practice serving individuals, families, and small businesses across the New Braunfels area."

**Services** (3 panels, in order):
1. Taxes — Individual, self-employed, and business returns — filed accurately and on time.
2. Bookkeeping — Monthly or quarterly books for small businesses and LLCs.
3. Financial planning — Retirement, savings goals, and long-term financial guidance.

---

## GitHub repo + Pages deployment

- Create public repo: `gh repo create migura-cpa-dark --public --source=. --remote=origin --push`
- Enable GitHub Pages: `gh api -X PUT repos/{owner}/migura-cpa-dark/pages -f source[branch]=main -f source[path]=/`
- Live URL will be: `https://{your-github-username}.github.io/migura-cpa-dark/`
- GitHub Pages takes 1–2 minutes to go live after first deploy. Let the user know.

---

## CLAUDE.md to write

```markdown
# Migura CPA — Dark Concept

Preview URL: https://{owner}.github.io/migura-cpa-dark/

One of three design options for client review. Near-black background, big type hero, three tall vertical service panels.

## Stack
- Plain HTML + CSS, no build tool
- Google Fonts: DM Sans only (300, 400, 500)
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
- Keep exactly 3 service panels
- "Taxes." in the hero must remain bold and gold (#c8a43a)
- Background is #111111 — do not lighten it
- Panel photos use opacity: 0.7 — intentional, do not remove
- Unsplash photo URLs are intentional — do not swap them
- Mobile breakpoint: panels stack to single column at 640px

## When ready for the real domain
- Add CNAME record in GoDaddy: `www` → `{owner}.github.io`
- Add a `CNAME` file at repo root containing her domain
- Enable custom domain in repo Settings → Pages
```
