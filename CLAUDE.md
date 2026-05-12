# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Serve locally with live reload
bundle exec jekyll serve

# Build static site
bundle exec jekyll build

# Install dependencies (first time)
bundle install
```

The site is deployed to GitHub Pages at `maxzin8.github.io/_portfolio`. No CI — pushes to `master` trigger GitHub Pages to rebuild automatically.

## Architecture

This is a **Jekyll static site** using the Hyde theme (modified), serving as Max Davidowitz's engineering portfolio.

**Layouts** (`_layouts/`):
- `default.html` — shell: `<head>` + sidebar + content wrapper
- `page.html` — wraps content in `.page` div; used for all portfolio project pages
- `post.html` — for blog-style posts (not currently used)

**Includes** (`_includes/`):
- `head.html` — meta, CSS links (poole + syntax + hyde), Google Fonts (Inter, Space Grotesk)
- `sidebar.html` — fixed left nav; dynamically generates links from pages with `layout: page`, sorted by frontmatter `order`

**Styling** (`public/css/`):
- `poole.css` — base reset/typography
- `hyde.css` — sidebar layout, theme colors, responsive breakpoints (48em, 58em, 64em). This is the primary file for visual changes — sidebar background is a dark gradient (`#0f172a → #1e1b4b`), accent color is indigo (`#6366f1`)
- `syntax.css` — code block highlighting

**Content pages** — Markdown/HTML files at repo root with frontmatter `layout: page` automatically appear in the sidebar nav. The `order` frontmatter key controls sort order.

**Adding a new project page**: create a `.md` file at the root with `layout: page`, `title:`, and `order:` frontmatter. Images go in `images/`.
