# juanluisdb.github.io

Personal site and writing space for Juan Luis Domínguez, built with Astro and Tailwind CSS.

## Stack

- Astro 6
- Tailwind CSS 4
- Markdown content collections
- GitHub Pages deployment target

## Structure

```text
src/
  content/
    blog/
  content.config.ts
  layouts/
    Base.astro
    Post.astro
  pages/
    index.astro
    blog/
      index.astro
      [...slug].astro
  styles/
    global.css
```

## Content

Blog posts live in `src/content/blog/` as Markdown files with frontmatter:

```md
---
title: "Post title"
description: "One sentence summary."
pubDate: 2026-04-01
---
```

## Commands

- `pnpm dev` starts the local development server
- `pnpm build` creates the production build in `dist/`
- `pnpm preview` previews the production build locally

## Deployment

This site is intended for GitHub Pages deployment. The Astro `site` setting is configured for `https://juanluisdb.github.io`.
