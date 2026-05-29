# GitHub Pages Deployment Guide

This repo publishes the portfolio from the `docs/` folder on the `main` branch.

Live site:

```text
https://zoma00.github.io/hazem-elbatawy-portfolio/
```

## Important Folders

- `docs/` is the deployed GitHub Pages site.
- `github_pages_boilerplate/` is the source/reference copy.
- Keep private notes, drafts, screenshots, credentials, and research folders out of Git unless they are intentionally redacted for public release.

## Before Editing

Check the current branch and status:

```bash
git branch --show-current
git status --short
```

You should be on:

```text
main
```

If many private folders appear as `??`, that means they are untracked. Do not run `git add .` unless you are sure every untracked file is safe to publish.

## Edit The Website

For deployed content, edit files in `docs/`:

```text
docs/index.html
docs/case-studies.html
docs/security-findings.html
docs/styles.css
docs/script.js
```

If you want the boilerplate copy to stay in sync, make the same edit in:

```text
github_pages_boilerplate/
```

## Preview Locally

Run a local static server from the repo root:

```bash
python3 -m http.server 8080 --directory docs
```

Open:

```text
http://localhost:8080
```

Stop the server with `Ctrl+C`.

## Safe Deploy Commands

Stage only the public files you changed. Example:

```bash
git add docs/index.html github_pages_boilerplate/index.html
```

Review what will be committed:

```bash
git status --short
git diff --cached
```

Commit:

```bash
git commit -m "Update portfolio content"
```

Push to GitHub:

```bash
git push origin main
```

GitHub Pages will redeploy automatically after the push.

## If You Accidentally Stage Everything

If `git status --short` shows many files staged with `A`, clear the staging area without deleting files:

```bash
git reset
```

Then stage only the safe public files:

```bash
git add docs/index.html
```

## Verify Deployment

After pushing, check the site:

```text
https://zoma00.github.io/hazem-elbatawy-portfolio/
```

If changes do not appear immediately, wait a few minutes and refresh the page. GitHub Pages can take a short time to rebuild.

## GitHub Pages Settings

In the GitHub repository:

1. Open `Settings`.
2. Open `Pages`.
3. Set source to `Deploy from a branch`.
4. Select branch `main`.
5. Select folder `/docs`.
6. Save.

## Public Safety Checklist

Before each deploy, confirm the commit does not include:

- credentials, tokens, API keys, cookies, or passwords
- private report links or private program names
- raw request/response logs
- exploit walkthroughs or payloads
- screenshots with sensitive data
- personal notes that were not meant to be public

Use this command to inspect staged files before committing:

```bash
git diff --cached --name-status
```
