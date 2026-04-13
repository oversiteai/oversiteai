# OverSite AI -- Production Site

**https://www.oversiteai.io**

This repository hosts the compiled production website for OverSite AI,
served via GitHub Pages with a custom domain. It is a **deploy target only**
-- do not edit files here directly. All contents are overwritten on every
deploy.

## How This Repo Gets Updated

The [oversiteai.io-cms](https://github.com/oversiteai/oversiteai.io-cms)
repository contains all source code, content management, and CI/CD
workflows. When changes reach the `main` branch of that repo, a GitHub
Actions workflow:

1. Checks out the `main` branch of `oversiteai.io-cms`
2. Runs `npm run build` (Vite compiles the React SPA)
3. Pushes the compiled `dist/` output to this repository, replacing all
   existing files

Content publishes from the CMS admin panel also trigger a rebuild via
`repository_dispatch`.

## Related Repositories

| Repository | Purpose |
|---|---|
| [oversiteai/oversiteai.io-cms](https://github.com/oversiteai/oversiteai.io-cms) | CMS source code, Flask API, React admin UI, CI/CD workflows |
| [oversiteai/oversiteai.io-cms-web](https://github.com/oversiteai/oversiteai.io-cms-web) | Preprod preview site (https://oversiteai.github.io/oversiteai.io-cms-web/) |
| **oversiteai/oversiteai** (this repo) | Production site (https://www.oversiteai.io) |

## Documentation

All documentation lives in the CMS repository:

- [README.md](https://github.com/oversiteai/oversiteai.io-cms#readme) -- System overview and quick start
- [HOWTO.md](https://github.com/oversiteai/oversiteai.io-cms/blob/main/HOWTO.md) -- Developer guide
- [HOW-TO-UPDATE-THE-WEBSITE.md](https://github.com/oversiteai/oversiteai.io-cms/blob/main/HOW-TO-UPDATE-THE-WEBSITE.md) -- Operations guide for marketing and web teams
