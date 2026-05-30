# Portfolio Repo Command Guide

This guide documents the commands and repo rules used while updating the portfolio.

## Main Repo

```bash
cd /home/hazem-elbatawy/Documents/portifolio_sec_research_dev
git remote -v
git status
```

Expected main remote:

```text
git@github.com:zoma00/hazem-elbatawy-portfolio.git
```

## Important Folders

```text
docs/                     Live GitHub Pages deployment folder
github_pages_boilerplate/ Source/reference copy of the portfolio site
publick_case_sudy/        Public case-study material tracked in main repo
tips/                     Local notes; only this guide is allowed by .gitignore
```

GitHub Pages deploys from:

```text
main branch + /docs folder
```

For live website changes, edit or sync:

```text
docs/index.html
docs/styles.css
```

The boilerplate copy is:

```text
github_pages_boilerplate/index.html
github_pages_boilerplate/styles.css
```

## Check Status

Run from the main repo root:

```bash
git status --short
git log --oneline -5
```

If you are inside `docs/`, `git status` still works, but root-relative paths like `publick_case_sudy/README.md` will not work from there.

Return to repo root:

```bash
cd /home/hazem-elbatawy/Documents/portifolio_sec_research_dev
```

## Sync Boilerplate Changes To Live Docs

If you edit the boilerplate copy and want the live site to match:

```bash
cp github_pages_boilerplate/index.html docs/index.html
cp github_pages_boilerplate/styles.css docs/styles.css
git diff --check -- docs/index.html docs/styles.css
git status --short
```

Commit and push:

```bash
git add docs/index.html docs/styles.css
git commit -m "Sync deployed portfolio pages"
git push origin main
```

## Edit Main Portfolio README

Root README shown at:

```text
https://github.com/zoma00/hazem-elbatawy-portfolio
```

Commands:

```bash
cd /home/hazem-elbatawy/Documents/portifolio_sec_research_dev
git status --short
nano README.md
git diff -- README.md
git add README.md
git commit -m "Update main README"
git push origin main
```

## Edit Public Case-Study README In Main Repo

Case-study README shown at:

```text
https://github.com/zoma00/hazem-elbatawy-portfolio/tree/main/publick_case_sudy
```

Commands:

```bash
cd /home/hazem-elbatawy/Documents/portifolio_sec_research_dev
nano publick_case_sudy/README.md
git diff -- publick_case_sudy/README.md
git add publick_case_sudy/README.md
git commit -m "Update public case study README"
git push origin main
```

## Root .gitignore Rule

The repo ignores most root-level files and folders by default:

```gitignore
/*
```

Then it allows only selected public content, including:

```gitignore
!/.gitignore
!/github_pages_boilerplate/
!/github_pages_boilerplate/**
!/publick_case_sudy/
!/publick_case_sudy/README.md
!/publick_case_sudy/final_submission_public_redacted.txt
!/publick_case_sudy/assets/H1-3493_TouristOuting-553_2.jpg.webp
!/tips/
/tips/*
!/tips/portfolio_repo_command_guide.md
```

This prevents accidental upload of private folders when using:

```bash
git add .
```

## Add Ignored Files Intentionally

If a file is ignored and you intentionally want to add it:

```bash
git add -f path/to/file
```

Prefer updating `.gitignore` with a narrow exception for public files that should stay tracked.

## Nested Case-Study Repo Issue

`publick_case_sudy/` used to contain its own `.git/` directory pointing to:

```text
git@github.com:zoma00/bug-bounty-case-study.git
```

That made it a nested Git repo. Adding it from the parent repo created a warning about an embedded Git repository.

The nested metadata was moved aside locally:

```bash
mv publick_case_sudy/.git publick_case_sudy/.git.removed-from-nested-repo
```

The main repo ignores that metadata:

```gitignore
/publick_case_sudy/.git.removed-from-nested-repo/
```

Do not commit nested `.git` metadata.

## Revert A Commit In A Separate Repo

If you accidentally push to another repo:

```bash
cd /path/to/that/repo
git log --oneline -3
git revert --no-edit COMMIT_SHA
git push origin main
```

This was used to undo the README change in the separate case-study repo before adding the content to the main portfolio repo.

## Safe Deploy Checklist

Before pushing:

```bash
git status --short
git diff --check
git diff --cached --name-status
```

Push:

```bash
git push origin main
```

Verify live site:

```text
https://zoma00.github.io/hazem-elbatawy-portfolio/
```
