# Tavio Website

Production-quality React, Vite, and Tailwind CSS marketing website for **Tavio**.

## Highlights

- React + Vite single-page app with React Router
- Tailwind CSS design system with light and dark mode
- Framer Motion micro animations
- SEO metadata with React Helmet, canonical URLs, Open Graph, Twitter cards, and structured data
- Responsive pages for Home, Features, Solutions, Industries, Demo, Pricing, Roadmap, About, Blog, FAQ, Contact, Waitlist, Privacy, Terms, and 404
- Reusable components for navigation, footer, cards, dashboard previews, pricing, FAQ accordions, forms, CTAs, and page sections
- Placeholder Formspree forms and analytics hooks for Google Analytics and Microsoft Clarity
- GitHub Pages-friendly Vite base config and SPA fallback

## Getting Started

```bash
npm install
npm run dev
```

The local site will run at the URL printed by Vite.

## Build

```bash
npm run build
npm run preview
```

## GitHub Pages

The production build uses `/` as the base path so it works correctly on `https://tavio.com`.

You can publish the `dist` directory using the included deploy script:

```bash
npm run deploy
```

The `public/CNAME` file tells GitHub Pages to serve the site from `tavio.com`.

## Forms

Forms use a placeholder Formspree endpoint:

```txt
https://formspree.io/f/your-form-id
```

Replace it in `src/components/LeadForm.jsx` before launch.

## Analytics

Analytics are intentionally placeholders. Add these environment variables when ready:

```bash
VITE_GA_ID=G-XXXXXXXXXX
VITE_CLARITY_ID=xxxxxxxxxx
```

Then replace the console placeholders in `src/analytics/placeholders.js` with approved production snippets.

## Structure

```txt
src/
  analytics/
  components/
  data/
  hooks/
  layouts/
  pages/
  styles/
  utils/
```

Most website content is data-driven from `src/data/siteData.js`, which keeps the marketing layer easy to connect to a CMS, app API, or full SaaS dashboard later.
