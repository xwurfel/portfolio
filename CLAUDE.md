# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a portfolio website built with Astro 5, based on the Astro Portfolio starter template. It is designed for deployment via Netlify Drop (drag-and-drop the `dist/` folder).

## Commands

- `npm run dev` — Start dev server at localhost:4321
- `npm run build` — Build production site to `./dist/`
- `npm run preview` — Preview the production build locally

No test runner or linter is configured.

## Architecture

**Framework:** Astro 5 with static site generation (no SSR). TypeScript in strict mode.

**Pages** (`src/pages/`): File-based routing. The `work/[...slug].astro` dynamic route generates pages from the `work` content collection using `getStaticPaths`.

**Layout:** Single `BaseLayout.astro` wraps all pages, providing `<head>` (via `MainHead`), `Nav`, and `Footer`. It manages background images with CSS custom properties and supports light/dark themes via the `theme-dark` class on `<html>`.

**Content Collection** (`src/content/work/`): Markdown files for portfolio work items. Schema defined in `src/content.config.ts` with required fields: `title`, `description`, `publishDate`, `tags`, `img`, and optional `img_alt`. Loaded via Astro's `glob` loader.

**Theme System:** Dark/light mode toggled by `ThemeToggle` component, which adds/removes `theme-dark` class on `<html>`. Background images are lazy-loaded after page load (`.loaded` class) and swap between light/dark variants via CSS custom properties.

**Components** (`src/components/`): All `.astro` files. `Icon.astro` renders SVG icons using path data from `IconPaths.ts`. `Grid.astro` supports `variant` prop (`offset` or `small`) for different layouts.
