# Dhanuka Inc. — Website

## What this project is

Static single-page website for Dhanuka Inc., a proprietary consulting firm.
Deployed via GitHub Pages at `https://dhanuka-inc.github.io` (adjust if org name differs).

## File structure

```
dhanuka-inc.github.io/
├── index.html                   ← the entire website; only file that needs editing
├── CLAUDE.md                    ← you are here
├── .claude/
│   └── commands/
│       ├── ship.md              ← /ship: commit + push current changes
│       └── update.md            ← /update: make a targeted content change
└── .github/
    └── workflows/
        └── deploy.yml           ← DO NOT edit unless changing the Pages pipeline
```

## How the site works

- Everything is in `index.html` — one self-contained file, no build step, no dependencies
- Google Fonts loads at runtime (Playfair Display, EB Garamond, Nunito)
- The SVG logo is inlined in the HTML
- Preview locally: just open `index.html` in a browser

## Content map (where things live in index.html)

| Section | What to look for |
|---|---|
| Firm name / logo | `<header class="masthead">` |
| Navigation | `<nav>` |
| Hero headline + subtext | `<section class="hero">` |
| Services (I, II, III) | `<section class="section-outer" id="services">` |
| About / bio | `<section class="section-outer" id="about">` |
| Contact details | `<section class="section-outer dark" id="contact">` |
| Footer | `<footer>` |

## Deployment pipeline

```
edit index.html  →  git push origin main  →  GitHub Actions  →  GitHub Pages (live in ~30s)
```

The workflow in `.github/workflows/deploy.yml` handles everything after the push.
No manual deploy step exists. Push = deploy.

## Git conventions

- Branch: always work on `main` (single-page static site; no feature branches needed)
- Commit messages: lowercase, imperative, descriptive of what actually changed
  - Good: `update: services section copy` / `fix: contact email address` / `add: new about paragraph`
  - Bad: `update`, `changes`, `misc`
- Never force-push (`git push --force`)

## What you're allowed to do

- Edit `index.html` freely — content, copy, colours, layout
- Commit and push to `main`
- Read any file in the repo

## What to be careful about

- `.github/workflows/deploy.yml` — don't edit unless the Pages deployment is broken
- The inline SVG logo (inside `<header class="masthead">`) — it's hand-crafted; don't rewrite it unless specifically asked
- Google Fonts `<link>` tag in `<head>` — required for the typography to load

## Common tasks

**Change a service description:** Find `<section class="section-outer" id="services">`, locate the right `.svc` div, edit the `<p>` tag.

**Update contact email:** Search for `hello@dhanukainc.com`, replace both instances (the `href` and the display text).

**Change the hero headline:** Find `<section class="hero">`, edit the `<h1>` tag.

**Update the about paragraph:** Find `<section class="section-outer" id="about">`, edit the `<p>` tags inside `.about-right`.
