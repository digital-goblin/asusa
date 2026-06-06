# Aquarium Show — Performance Tracker (asusa.digital-goblin.com)

A static dashboard for **aquariumshowusa.com**, hosted on GitHub Pages at
`asusa.digital-goblin.com`. No password, not indexed by search engines.

## Files
- `index.html` — the dashboard (reads `data.json`).
- `data.json` — the data. **This is the only file that changes between updates.**
- `CNAME` — custom domain (`asusa.digital-goblin.com`).
- `robots.txt` — blocks search engine crawling.
- `README.md` — this file.

## One-time setup (in the `asusa` repo)
1. Upload these 5 files to the repo root (`main` branch).
2. **Settings → Pages →** Deploy from a branch → `main` / `/ (root)` → Save.
3. DNS is already set (`asusa` → GitHub Pages via Cloudflare). Confirm the custom
   domain shows `asusa.digital-goblin.com` and enable **Enforce HTTPS**.

## Updating the data (manual)
When you want fresh numbers:
1. In Cowork, ask for a refreshed `data.json` (it's pulled from Shopify).
2. In the `asusa` repo, open `data.json` → **edit (pencil) →** paste the new
   contents → **Commit**. GitHub Pages redeploys automatically in ~1 minute.

That's it — only `data.json` ever needs to change.

## Privacy notes
- `robots.txt` + the `noindex` meta tag keep it out of search results.
- It has **no password**, so anyone with the URL can view it. The URL is just
  not advertised or indexed.
- Revenue figures are visible to anyone who opens the page or `data.json`
  directly. If that ever becomes a concern, add Cloudflare Access (free) in front
  of the subdomain.
