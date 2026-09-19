# Vatsh Van Portfolio

This repository is a modular Hugo + Hugo Blox portfolio. The site is designed so you can add new content by dropping Markdown files into the right folder, while keeping the core configuration stable.

## What Goes Where

- `config/_default/` contains site-wide settings, menus, and theme parameters.
- `content/authors/admin/_index.md` controls the About section and profile data.
- `content/experience/` contains experience entries.
- `content/project/` contains project entries.
- `content/publications/` is ready for publication entries.
- `layouts/` contains the custom homepage and list/single templates.
- `static/css/site.css` controls the visual design.
- `static/uploads/` is where shared files such as the resume PDF should live.

## Horizontal Changes

Horizontal changes mean adding more items of the same kind without changing the site architecture.

### Add a new experience entry

1. Create a new folder under `content/experience/`, for example `content/experience/new-role/`.
2. Add an `index.md` file inside that folder.
3. Put the front matter and content in that file.
4. Add an optional `featured.svg`, `featured.png`, or similar image in the same folder.

Example:

```text
content/experience/new-role/index.md
content/experience/new-role/featured.svg
```

### Add a new project

1. Create a new folder under `content/project/`.
2. Add an `index.md` file in that folder.
3. Add local assets next to the Markdown file if needed.
4. Use tags and summary fields so the homepage card renders cleanly.

Example:

```text
content/project/my-project/index.md
content/project/my-project/featured.svg
content/project/my-project/demo.gif
```

### Add a publication

1. Create a new folder under `content/publications/`.
2. Add an `index.md` file.
3. Add any figures or PDFs in the same folder.

### Add or replace the resume

1. Put the PDF in `static/uploads/`.
2. Name it `Vatsh_Van_Resume.pdf` to match the existing menu link.
3. If the filename changes, update `config/_default/menus.yaml`.

## Vertical Changes

Vertical changes mean changing how the site works or looks globally.

### Change the homepage layout

- Edit `layouts/index.html` to change section order, add new blocks, or change how cards are rendered.
- Edit `layouts/_default/baseof.html` if you want to change the global wrapper, header, footer, fonts, or math loading.

### Change the visual design

- Edit `static/css/site.css` to update colors, spacing, typography, shadows, and responsiveness.
- If you want a very different look, change the CSS variables at the top of the file first.

### Change global navigation

- Edit `config/_default/menus.yaml` to add, remove, or rename menu links.
- Keep the anchor targets in sync with the homepage sections in `layouts/index.html`.

### Change site metadata

- Edit `config/_default/hugo.yaml` for title, base URL, and module imports.
- Edit `config/_default/params.yaml` for theme mode and math support.

## Content Rules

- Use one Markdown file per item.
- Keep images or supporting files inside the same folder as the Markdown file when the asset belongs to a single item.
- Prefer bundle folders like `content/project/name/index.md` over loose files when a page needs its own assets.
- Use plain Markdown for content whenever possible.
- Use the existing front matter fields when adding new entries so the homepage can render them automatically.

## Adding A New Section

If you want a brand-new section, such as `awards`, `talks`, or `blog`:

1. Create a new folder under `content/`, for example `content/awards/`.
2. Add an `_index.md` file for the section.
3. Add one `index.md` file per item inside a folder or as standalone pages, depending on how much asset isolation you need.
4. Update `layouts/index.html` if you want the new section on the homepage.
5. Update `config/_default/menus.yaml` if you want it in the top navigation.

## Build And Deploy

- GitHub Pages deployment is configured in `.github/workflows/hugo.yaml`.
- The workflow builds with `hugo --gc --minify` and deploys to GitHub Pages.
- Keep the site static and asset-light for fast loading.

## Recommended Workflow

1. Add or edit Markdown in `content/`.
2. Add any local images or files inside the same content folder.
3. Only edit `layouts/` or `config/` if you are changing site behavior or appearance.
4. Commit and deploy.

## Notes

- The site is modular by design, so most new content should not require config changes.
- If a page looks wrong, check the front matter first, then the matching template in `layouts/`.
- If you want a new homepage card style, update the template and the CSS together.