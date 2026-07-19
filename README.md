# Alineo Insights

Source for [www.alineoinsights.com](https://www.alineoinsights.com), deployed on Cloudflare Workers.

## Working directly on `main`

There is no separate staging/sandbox branch — every push to `main` deploys
straight to production at alineoinsights.com. Preview changes locally
before pushing.

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
