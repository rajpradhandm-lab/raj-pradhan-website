# Raj Pradhan — personal website (v1)

A modern creative React website for **rajpradhan.com.np**. Light mode is the default; the header toggle switches to dark mode and saves the choice in browser storage.

## Pages
- `/` — homepage, selected work, short introduction, Journal, and contact call-to-action
- `/about` — professional introduction and areas of work
- `/work` — filterable collection of five candidate portfolio projects
- `/work/:slug` — individual project overview
- `/journal` — searchable and filterable editorial index
- `/journal/:slug` — individual article pages
- `/contact` — email and LinkedIn links

## Run locally

Requires Node.js 20.19+ or 22.12+.

```bash
npm install
npm run dev
```

Visit the local URL printed in the terminal (usually `http://localhost:5173`).

## Build

```bash
npm run build
npm run preview
```

The publishable static site is generated in `dist/`.

## Cloudflare Pages deployment (option)

1. Push this source to a private GitHub repository.
2. In Cloudflare Pages, connect the repository.
3. Framework preset: **Vite**; build command: **npm run build**; output directory: **dist**.
4. Add `rajpradhan.com.np` as a custom domain and configure DNS per Cloudflare's instructions.
5. Check that deep links such as `/journal/brand-is-more-than-a-logo` load via Pages SPA fallback (the generated build has no top-level `404.html`).
6. Verify HTTPS, mobile navigation and forms/links after deployment.

Alternatively host the `dist` directory on a static host supporting SPA routing.

## Content editing
- Update the `projects` array in `src/data.js` for portfolio details.
- Update `articles` in `src/data.js` for Journal posts.
- Change site email and LinkedIn URLs at the top of `src/main.jsx`.
- Replace the typographic portrait placeholder once photography is supplied.
- The decorative project and article artwork is original CSS/typography, not client-owned brand imagery.

## Important publication checks
- Current project descriptions are **candidate overviews**, not validated case studies. Obtain permission before publishing client work, brand assets or outcomes.
- Journal posts are **editorial drafts** for review, not yet approved for public release.
- LinkedIn profile details, education, dates, certifications, job titles and measurable outcomes were not automatically verifiable; none are fabricated.
- There's no admin dashboard or backend in v1. Decide on CMS after reviewing this site. A headless CMS or Git-based Markdown workflow can be added without changing the visual language.
- Site-specific legal/privacy and analytics requirements should be reviewed before production launch.

## SEO considerations
Home metadata, Open Graph title/description, and favicon are included. For production, add unique server-rendered or pre-rendered metadata for each page (or migrate to Next.js / Astro), a sitemap, robots.txt, social sharing images and verified Search Console ownership. The current SPA uses JavaScript-managed page titles and descriptions, which is not ideal as a final SEO architecture for an actively updated Journal.
