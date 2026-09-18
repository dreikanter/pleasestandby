# Feeder landing page

A static landing page for [Feeder](https://fffeeder.com).

## Preview

Open `index.html` in a browser, or serve this directory with `python3 -m http.server 8000`.

## Deployment

Cloudflare Workers serves the static files using `wrangler.toml` (`name = "pleasestandby"`, assets directory `.`).

Build settings live in Cloudflare: **Workers & Pages → pleasestandby → Settings → Builds**. For this site, use the repository root, no build command, and `npx wrangler deploy` as the deploy command. Confirm the production branch there; it is a dashboard setting, not part of `wrangler.toml`.

Build history is available under the Worker's **Deployments** tab and through the Cloudflare check on each built GitHub commit. For a manual deployment from an authenticated machine, run `npx wrangler deploy` in this directory.
