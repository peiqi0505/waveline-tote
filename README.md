# Waveline — The Wave Tote landing page

Static landing page for the Wave Tote, built for a US audience. No build step: it is plain HTML, CSS and a little vanilla JS.

## Files

- `index.html` — the whole page (styles and scripts are inline)
- `assets/` — product photography and detail crops referenced by the page
- `.nojekyll` — tells GitHub Pages to serve the files as-is

## Editing

Open `index.html` in any text editor. Text sits in plain HTML; the ten colorways are the `COLORS` array at the bottom of the file. Every price, shipping promise and FAQ answer is written in the page, so update those before going live if your terms differ.

## Deploying

This folder is a git repository. Push it to GitHub and Pages serves it from the `main` branch root:

```bash
git add .
git commit -m "Update landing page"
git push
```

The published URL has the form `https://<your-account>.github.io/<repo-name>/`.
