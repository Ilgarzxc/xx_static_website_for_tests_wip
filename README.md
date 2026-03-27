## Project Purpose

This repository demonstrates GitHub Actions-based Continuous Integration and Continuous Deployment (CI/CD) of a static website to GitHub Pages.

- Goal: Deploy updates to GitHub Pages when `main` receives a push affecting any *.html file.
- Static site entry: `index.html` includes a text placeholder: "Hello, GitHub Actions!".

## Files Included

- `index.html` — main page for the website
- `about.html`, `projects.html`, `cv.html` — additional site pages
- `.github/workflows/deploy.yml` — GitHub Actions workflow for deployment

## Workflow Behavior

The workflow is configured in `.github/workflows/deploy.yml`:

- Trigger: `on.push.branches: [main]` with `paths: - "*.html"`.
- Action: checks out code and publishes site to `gh-pages` branch using `peaceiris/actions-gh-pages@v4`.
- Only updates done to `index.html` will trigger deployment.

## GitHub Pages URL

After setup and a successful workflow run, the site is available at:

`https://ilgarzxc.github.io/xx_static_website_for_tests_wip/index.html`

## How to Use

1. Commit changes to any *.html file in `main` branch.
2. Push to GitHub.
3. Workflow runs automatically and deploys to `gh-pages`.
4. Visit the GitHub Pages URL to verify.
