# Codex-Playground


[![Pages](https://github.com/mtonsmann/Codex-Playground/actions/workflows/gh-pages.yml/badge.svg)](https://github.com/mtonsmann/Codex-Playground/actions/workflows/gh-pages.yml)
[![Vercel](https://github.com/mtonsmann/Codex-Playground/actions/workflows/vercel.yml/badge.svg)](https://github.com/mtonsmann/Codex-Playground/actions/workflows/vercel.yml)

Demo repo showing simple GitHub Pages and Vercel deployments.

- **GitHub Pages:** https://mtonsmann.github.io/Codex-Playground/
- **Vercel (prod):** https://<vercel-app>.vercel.app/

## How this works
1. Push to `main` triggers two GitHub Actions workflows.
2. `gh-pages.yml` publishes static files from the repo root to the `gh-pages` branch via `peaceiris/actions-gh-pages`.
3. `vercel.yml` installs the Vercel CLI and deploys a preview on every push.
4. When the push is on `main`, the same job also deploys to production using the `--prod` flag.
5. Each workflow finishes by printing the deployed URL for quick access.

## Secrets & security
- Create a Vercel token under your Vercel account settings.
- Scope the token to the desired organization and project IDs.
- Add `VERCEL_TOKEN`, `VERCEL_ORG_ID`, and `VERCEL_PROJECT_ID` to your GitHub repository secrets so the workflows can authenticate without exposing credentials.
