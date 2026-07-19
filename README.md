# Alineo Insights

Source for [www.alineoinsights.com](https://www.alineoinsights.com), deployed on Cloudflare Workers.

## `sandbox` branch

This branch is a homepage redesign for review — not deployed anywhere yet.
It merges the animated hero / navy-gold visual identity from the current
`main` site with the fuller marketing structure (problem, how it works,
platform, pricing) from an earlier draft, restores rehab/behavioral-health
positioning, and adds a mocked product showcase (illustrative facility
names and figures only — no real customer data). `main` is untouched; this
branch has to be merged deliberately for any of it to go live.

To preview locally:

```
cd public
python -m http.server 5500
```

then open `http://localhost:5500`. It's a single static `index.html`, so
edits show up on refresh with no build step.

## Structure

- `public/` — static site files served by the Worker
- `wrangler.toml` — Worker config (points at `public/` as the assets directory)

## Deploying

Pushes to `main` are automatically built and deployed by Cloudflare (via the Cloudflare Workers and Pages GitHub integration). No manual deploy steps needed.
