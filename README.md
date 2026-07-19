# Shweta Sai Machiraju — Portfolio

A static one-page portfolio site (plain HTML/CSS, no build step, no dependencies to install).

## Files

```
.
├── index.html      ← the page
├── style.css       ← all styling
├── assets/         ← project images (used by index.html)
└── .nojekyll       ← tells GitHub Pages not to run Jekyll processing
```

## How to deploy on GitHub Pages

1. **Create a new repository** on GitHub (e.g. `portfolio`).
2. **Upload all the files in this folder** to the repository, keeping the same
   structure — `index.html`, `style.css`, `.nojekyll`, and the `assets/` folder
   must all sit in the same top-level directory (the repo root).
   - Easiest way: on the repo page click **Add file → Upload files**, then drag
     in `index.html`, `style.css`, `.nojekyll`, and the whole `assets` folder.
   - Or via git:
     ```bash
     git clone https://github.com/<your-username>/portfolio.git
     cd portfolio
     # copy index.html, style.css, .nojekyll, and assets/ into this folder
     git add .
     git commit -m "Add portfolio site"
     git push
     ```
3. **Turn on Pages**: in the repo, go to **Settings → Pages**.
   - Under "Build and deployment", set **Source** to **Deploy from a branch**.
   - Set **Branch** to `main` (or `master`) and folder to `/ (root)`.
   - Click **Save**.
4. Wait a minute, then refresh the Pages settings page — it will show your live
   URL, typically:
   ```
   https://<your-username>.github.io/portfolio/
   ```

That's it — no build process, no npm install, nothing else needed.

## Editing content

- Text: open `index.html` and edit directly — all copy (bio, project
  descriptions, captions) is plain text in the markup.
- Images: swap files in `assets/` (keep the same filenames, or update the
  `src="assets/..."` paths in `index.html` if you rename them).
- Styling (colors, spacing, type): edit `style.css`. Key variables (colors,
  fonts, max page width) are defined at the top of the file under `:root`.
- Prototype links: the "HB1 Figma Prototype →" and "Junbi Figma Prototype →"
  links currently point to `#` — replace with your real Figma share links in
  `index.html`.

## Notes

- The page uses Google Fonts (Newsreader + Inter) loaded via `<link>` tags in
  `index.html`. This requires an internet connection to load (works fine once
  deployed — this only matters if you're viewing the file completely offline).
- Fully responsive — tested down to mobile widths.
