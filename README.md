# Dhanuka Inc. — Website

Official website for **Dhanuka Inc.**, a proprietary consulting firm.

Live at: `https://dhanuka-inc.github.io` *(replace with your actual org name if different)*

---

## Deployment

Every push to `main` automatically deploys via GitHub Actions → GitHub Pages.
No manual steps needed after the first-time setup.

**Workflow:** `.github/workflows/deploy.yml`

---

## Making changes

1. Edit `index.html` locally
2. Commit and push to `main`
3. GitHub Actions picks it up — site is live in ~30 seconds

```bash
git add index.html
git commit -m "update: describe your change"
git push origin main
```

---

## Local preview

Open `index.html` directly in a browser — no build step, no dependencies.

---

## Repo structure

```
dhanuka-inc.github.io/
├── index.html               # the entire website (single file)
├── .github/
│   └── workflows/
│       └── deploy.yml       # CI/CD — auto-deploys on push to main
└── README.md
```
