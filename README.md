# PixlFit

Static marketing and app site for **PixlFit** — a browser-based tool to upload images, pick output sizes (presets), crop, apply filters, and download batches. Processing runs in the client; nothing is uploaded to a PixlFit server for editing.

Built with [Astro](https://astro.build/) (static output).

## Requirements

- [Node.js](https://nodejs.org/) **22.12+** (see `package.json` `engines`)

## Setup

```sh
npm install
```

## Scripts

| Command           | Description                                      |
| ----------------- | ------------------------------------------------ |
| `npm run dev`     | Dev server (default: http://localhost:4321)      |
| `npm run build`   | Production build to `dist/`                      |
| `npm run preview` | Serve `dist/` locally to verify the build        |

## Project layout

| Path            | Role |
| --------------- | ---- |
| `src/pages/`    | Routes: home (`index.astro`), ideas, privacy, terms |
| `src/components/` | Shared UI (e.g. footer)                         |
| `src/layouts/`  | HTML shell, fonts, favicon links                 |
| `src/styles/`   | Global CSS (`pixlfit.css`)                      |
| `public/`       | Static assets (favicons, etc.), copied to `dist/` root |
| `dist/`         | Build output (not committed)                     |

## Deployment (Netlify)

[`netlify.toml`](netlify.toml) sets `publish = "dist"` and `npm run build` as the build command.

### Ideas form

The **Got an Idea?** page uses [Netlify Forms](https://docs.netlify.com/forms/setup/) (`name="pixlfit-ideas"`). Submissions appear in the Netlify dashboard under **Forms**. To receive email notifications (for example to `perennialwebstudio@gmail.com`), configure **Site configuration → Forms → (your form) → Notifications & webhooks** in the Netlify UI — that is not defined in this repo.

## License / credits

Content and branding are project-specific. Astro and tooling follow their respective licenses.
