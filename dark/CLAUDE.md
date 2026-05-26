# Migura CPA — Dark Concept

Preview URL: https://pogorman.github.io/migura-cpa/dark/

One of three design options for client review. Near-black background, large lightweight type hero, three vertical service panels.

## Stack
- Plain HTML + CSS, no build tool
- Google Fonts: DM Sans only (300, 400, 500)
- Lives at the `/dark/` path inside the main `migura-cpa` GitHub repo. There is **no separate repo** for this variant — all three concepts share the same repo with sibling folders (`/`, `/dark/`, `/warm/`)

## Structure
- `index.html` — the entire variant
- `css/styles.css` — all styles
- `kick-off-doc/` — reference files only, not served

## Deploy
git add -A && git commit -m "your message" && git push

## Key rules
- Do not change any copy without being asked
- Do not add JavaScript unless explicitly requested
- Do not introduce a framework or build step
- Keep exactly 3 service panels
- "Taxes." in the hero must remain bold and gold (`#c8a43a`)
- Background is `#111111` — do not lighten it
- Panel photos use `opacity: 0.7` — intentional, do not remove
- Unsplash photo URLs are intentional — do not swap them
- Mobile breakpoint: panels stack to single column at 640px

## When ready for the real domain
- Custom domain configuration is handled at the main repo level. See `../CLAUDE.md` at the repo root. Note: a single CNAME applies to the entire Pages site, so if a variant gets promoted to the live domain, the chosen variant's files should be promoted to the repo root.
