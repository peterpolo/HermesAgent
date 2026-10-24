# HermesAgent

A modern, single-file **Todo web app** (Add / Delete / Mark Done) with a cute rabbit mascot, clean indigo-accent UI, filters, a progress bar, and local persistence.

## Live site

Deployed to **GitHub Pages** — the URL is shown at the top of this page once the
[Build and deploy to GitHub Pages](.github/workflows/pages-build-deploy.yml) workflow finishes.

## Features

- ➕ **Add** tasks (Enter or button)
- ✅ **Mark done** — click the circle to toggle (keyboard accessible)
- 🗑 **Delete** — slide-out animation
- 🔍 **Filters** — All / Active / Done
- 📊 **Progress bar** with completion percentage
- 💾 **Persistence** via `localStorage`
- 🐇 **Rabbit mascot** (white fur, red eyes) in the header + empty state

## Build & deploy (CI/CD)

`.github/workflows/pages-build-deploy.yml` runs on every push to `main`:

1. **CI** — validates the static site (HTML sanity check + no leaked secrets in the payload)
2. **Build** — assembles the deployable site into `build/`
3. **Deploy** — publishes to GitHub Pages via `actions/deploy-pages`

## Run locally

No build step required. Open the static file directly, or serve it:

```bash
# Python
python3 -m http.server 8000
# then open http://localhost:8000/index.html
```

## Repository layout

```
index.html                                # the todo app (single file, self-contained)
.github/workflows/pages-build-deploy.yml # CI/CD -> GitHub Pages
```
