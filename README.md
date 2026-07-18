# Alineo Insights

Source for [www.alineoinsights.com](https://www.alineoinsights.com), deployed on Cloudflare Workers.

## Structure

- `public/` — static site files served by the Worker
- `wrangler.toml` — Worker config (points at `public/` as the assets directory)

## Deploying

Pushes to `main` are automatically built and deployed by Cloudflare (via the Cloudflare Workers and Pages GitHub integration). No manual deploy steps needed.
