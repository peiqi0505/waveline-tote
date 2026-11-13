# WAVELINE — The Wave Tote

Single-page product landing page for the Wave Tote, aimed at US shoppers.
Live at **https://peiqi0505.github.io/waveline-tote/**

## What is in this repo

| Path | Purpose |
| --- | --- |
| `index.html` | The whole page. Styles and scripts are inline, so there is no build step. |
| `assets/tote-01.jpg … tote-10.jpg` | Ten colorway photos, watermark-free, used by the hero and the color picker. |
| `assets/sw-01.jpg … sw-10.jpg` | Square thumbnails for the color swatches. |
| `assets/detail-texture.jpg`, `detail-base.jpg`, `detail-handle.jpg` | Close-ups for the craft section. |
| `.nojekyll` | Tells GitHub Pages to serve files as-is. |

## Editing the page

1. Open `index.html` in any editor. The CSS sits in one `<style>` block at the top, the JS in one `<script>` block at the bottom.
2. Save, refresh in a browser — no server or build step needed.
3. Publish (see below).

## Publishing (important)

`git push` over HTTPS is unreliable on this network — connections get reset. Publishing therefore
goes through the GitHub Contents API instead:

```powershell
$env:GH_TOKEN = (& "..\.tools\gh\bin\gh.exe" auth token).Trim()
python ..\scripts\publish_files.py index.html assets/tote-03.jpg
```

`publish_files.py` compares the SHA1 of the local file with the blob already in the repo and only
uploads when they differ, then re-reads the blob to confirm the bytes landed. Nothing is
force-pushed and no commit is created for identical files.

GitHub Pages rebuilds about a minute after a commit. Hard-refresh the browser (Ctrl+F5) and add
a `?v=` query when checking an image you just replaced, because Pages serves assets with a short
cache lifetime.

## Content that still needs the owner's confirmation

- Dimensions (16.5 × 12 × 5 in) and weight (16.9 oz) were estimated from the photos — confirm with the factory.
- Wash care, shipping window, and the 30-day return policy are written as standard DTC copy, not as confirmed policy.
- Checkout is a placeholder. Connect Stripe or move the page onto Shopify to take real payments.
- Social links in the footer are placeholders.
