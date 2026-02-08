# Mykhailo Ilnytskyi — Portfolio

Personal portfolio website for Mykhailo Ilnytskyi, Android Software Engineer. Built with Astro 5 and deployed via Netlify Drop.

## Tech Stack

- **Astro 5** — Static site generation, no SSR
- **TypeScript** — Strict mode
- **Netlify Drop** — Drag-and-drop deployment

## Commands

All commands are run from the root of the project, from a terminal:

| Command           | Action                                       |
| :---------------- | :------------------------------------------- |
| `npm install`     | Installs dependencies                        |
| `npm run dev`     | Starts local dev server at `localhost:4321`  |
| `npm run build`   | Build production site to `./dist/`           |
| `npm run preview` | Preview the production build locally         |

## Project Structure

```
src/
├── components/    # Astro components (Nav, Footer, Icon, Grid, etc.)
├── content/work/  # Markdown files for portfolio work items
├── pages/         # File-based routing (index, about, work)
└── styles/        # Global styles
```

## Deployment

1. Run `npm run build` to generate the production site in `dist/`
2. Go to [Netlify Drop](https://app.netlify.com/drop) and drag-and-drop the `dist/` folder
