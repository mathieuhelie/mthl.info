# mthl.info — Claude Maintenance Guide

This is the personal site and CV generator for Mathieu Hélie at https://mthl.info.

## What this site is

A static site built with [Eleventy](https://www.11ty.dev/) that serves as the source of truth for professional CVs targeting different audiences. The home page is a full, detailed CV optimized for web search. Variant pages filter and summarize for specific audiences. They do not change the language but compact it to a specific format for that audience.

## Pages

| File | URL | Purpose |
|---|---|---|
| `src/index.md` | `/` | Full chronological CV — maximum detail, SEO-optimized |
| `src/cv-tech.md` | `/cv-tech/` | Tech/consulting/entrepreneurship focus — Drupal, PHP, JS, architecture |
| `src/cv-urban.md` | `/cv-urban/` | Urbanism/complexity science focus — TNOC articles, blogs, presentations, consulting |
| `src/cv-linkedin.md` | *(not published in nav)* | LinkedIn-format summary profile — reference document for updating LinkedIn manually. Nav link goes to linkedin.com/in/mhelie. |

The three public pages share one layout: `src/_includes/layouts/cv.njk`. The variant nav links to the LinkedIn profile directly (linkedin.com/in/mhelie) — not to the local cv-linkedin.md page.

Variant pages are filtered views of the same master history in `src/index.md`. They use the same voice, language, and first-person perspective — only the content changes, not the tone.

## Content model

Each page is a Markdown file with YAML front matter:

```yaml
---
layout: cv.njk
title: "Page title"
description: "Meta description for SEO"
variant: full   # full | tech | urban | linkedin
---
```

The `variant` field controls which nav link is highlighted as active in the layout.

The Markdown body is the full content for that page. Claude writes and maintains this content — the user does not edit these files directly.

## Adding a new CV variant

1. Create `src/cv-[name].md` with front matter `variant: [name]`
2. Add a nav link in `src/_includes/layouts/cv.njk` in the `.variant-nav` section
3. Add instructions for the variant to `.claude/commands/refresh-site.md`

## Source documents

User drops source documents (work experience notes, project descriptions, prior CV files, client briefs) into `content/`. Claude reads these and uses them to populate the CV pages.

The `content/` directory is not published — it's gitignored from `_site/` automatically (it's outside `src/`).

## Build

```bash
npm install          # first time only
npm run build        # generates _site/
npm start            # dev server at localhost:8080
```

Output goes to `_site/` (gitignored).

## Deploy

Merge to `gh-pages` branch. GitHub Actions (`.github/workflows/deploy.yml`) triggers on push to `gh-pages`, builds the site, and deploys `_site/` to GitHub Pages at https://mthl.info.

## Refreshing the site

Use the `/refresh-site` slash command. It reads `content/`, searches for public updates, regenerates all four CV pages, builds, and pushes. See `.claude/commands/refresh-site.md` for full instructions.

## Design system

**Colors (CSS custom properties in `src/css/style.css`):**
- `--color-bg: #F8F7F4` — warm off-white background
- `--color-text: #333333` — main text
- `--color-muted: #666666` — secondary text, dates, labels
- `--color-accent: #E04444` — red accent for links and hover states
- `--color-border: #E0DDD8` — subtle borders and dividers

**Typography:**
- Body: Lora (Google Fonts) — serif, academic feel
- Display/headings `h2`: Dorsa (Google Fonts) — thin geometric uppercase, same as emergenturbanism.com
- Sub-headings `h3`: Lora, 600 weight
- UI/nav/meta: system-ui sans-serif
- Max content width: 720px

**Markdown heading conventions in CV pages:**
- `##` — Section heading (e.g., `## Experience`, `## Published Writing`)
- `###` — Role or article title (e.g., `### Technology Senior Associate — Appnovation Technologies`)
- `####` — Organization / date metadata line (e.g., `#### Montreal, Canada | 2013`)

## Known content sources

- **content/** directory — user's primary source documents
- **thenatureofcities.com** — search for new articles by "Mathieu Hélie"
- **LinkedIn**: https://www.linkedin.com/in/mhelie
- **Emergent Urbanism**: http://emergenturbanism.com
- **GitHub**: https://github.com/mathieuhelie

## Known articles at The Nature of Cities (as of last refresh)

1. Explaining the Housing Crisis with the Theory of Constraints — Apr 2023
2. A Fractal Solution to Regional Complexity and Governance — Jan 2020
3. Neighborhoods that Change in Non-linear Ways — Jul 2019
4. Neural Networks — A New Model for 'The Kind of Problem a City Is' — Apr 2018
5. The Effect of Iteration on Urban Form, Part II — Jun 2017
6. The Effect of Iteration on Urban Form, Part I — Jun 2017
7. Uses and Abuses of Preservation — Nov 2016
8. Common Threads: Jane Jacobs and Elinor Ostrom — May 2016
9. Neighborhoods and Urban Fractals — Oct 2012

## Images

Portrait: `src/images/portrait.jpg` — 90×90px circle in the header. To replace, swap the file.

For image galleries (future): use `@11ty/eleventy-img` — it generates thumbnails automatically. See Eleventy docs for usage.
