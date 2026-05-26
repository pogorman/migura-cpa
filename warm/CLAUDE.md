# Migura CPA — Warm Editorial Concept

Preview URL: https://pogorman.github.io/migura-cpa/warm/

One of three design options for client review. Cream background, serif type, 4-up grid of service cards (italic gold number + thumbnail + title + description).

## Stack
- Plain HTML + CSS, no build tool
- Google Fonts: Lora + DM Sans
- Lives at the `/warm/` path inside the main `migura-cpa` GitHub repo. There is **no separate repo** for this variant — all three concepts share the same repo with sibling folders (`/`, `/dark/`, `/warm/`)

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
- Keep exactly 4 service cards
- Unsplash photo URLs are intentional — do not swap them
- Cream background: `#f7f4ef` — do not change to white
- Breakpoints: 4 cards in a row > 960px, drop to 2-up at 960px, drop to 1-up at 640px

## When ready for the real domain
- Custom domain configuration is handled at the main repo level. See `../CLAUDE.md` at the repo root. Note: a single CNAME applies to the entire Pages site, so if a variant gets promoted to the live domain, the chosen variant's files should be promoted to the repo root.
