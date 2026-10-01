# Ziqi Xu — personal site

Plain HTML, CSS, and a little JavaScript. No framework, no build step.

## What's where

| Path | What it is |
|---|---|
| `index.html` | Home page: hero, projects, experience, about, contact |
| `projects/<project>/index.html` | One case study per project |
| `assets/css/style.css` | All styles. Colors and fonts are tokens at the top (light + dark) |
| `assets/js/main.js` | Theme toggle, scroll reveals, copy-email button, slide lightbox |
| `assets/img/` | Images: headshot, and Allianz slides exported from the final deck |
| `404.html` | "Page not found" page for GitHub Pages |

## Preview locally

```bash
python3 -m http.server 4173
```

Then open http://localhost:4173.

## Before publishing

Draft text and fill-in notes are marked with `class="note"` and `class="draft"`.
This must print nothing before the site goes live:

```bash
grep -rnE 'class="([^"]* )?(note|draft)( [^"]*)?"' --include='*.html' .
```

## Publish on GitHub Pages

1. Create a **public** repository named `<your-username>.github.io`.
2. Push this folder to the `main` branch.
3. In the repository, open **Settings → Pages** and choose **Deploy from a branch → main → / (root)**.
4. The site goes live at `https://<your-username>.github.io` within a minute or two.
