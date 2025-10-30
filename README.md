**Sizzle 'N Slice Website**

Proudly Halaal restaurant in Observatory, Cape Town — wood‑fired pizza, kebabs, pasta, gelato, mocktails and more. Visit the live site at `https://sizzlenslice.co.za/`.

## Overview
This repository contains the production-ready static build of the Sizzle 'N Slice marketing website. It is optimized for fast load times, reliability, and search visibility. Content is served as static assets (HTML/CSS/JS, images, fonts) and can be deployed on any modern static hosting platform with a CDN.

## Technology & Architecture
- **Static site**: Pure HTML/CSS/JS; no server-side runtime required.
- **Performance-first**: Preloaded hero media, optimized asset delivery, and CDN caching friendly.
- **SEO-ready**: Open Graph and Twitter metadata are included for rich sharing.
- **Analytics-ready**: Google Tag Manager (GTM) hooks are present for analytics and marketing tags.
- **Responsive design**: Mobile-first styles for consistent experience across devices.

## Repository Structure
- **`zaatarandzzas/`**: Site root containing `index.html` and all static assets
  - **`index.html`**: Primary entry point
  - **`wp-content/`**: Images, fonts, styles, and compiled scripts delivered as static assets
  - Additional vendor assets as needed for UI components and media

## Local Development
No build step is required. You can run a simple static server to preview locally.

- **Using Python (built-in on macOS):**
```bash
cd zaatarandzzas
python3 -m http.server 8080
```
Then open `http://localhost:8080` in your browser.

- **Using Node (if preferred):**
```bash
npm i -g serve
serve zaatarandzzas -l 8080
```

## Deployment
This site can be hosted on any static hosting/CDN provider. A typical deployment uploads the contents of `zaatarandzzas/` to the hosting platform and enables global caching.

Recommended settings:
- **Caching**: Cache HTML conservatively; cache static assets (CSS/JS/images/fonts) with long TTLs and content hashing.
- **Compression**: Enable Brotli and Gzip.
- **HTTP/2 or HTTP/3**: For improved multiplexing and lower latency.
- **Redirects**: Ensure canonical domain (`https://sizzlenslice.co.za/`) and HTTPS are enforced.

## Content & SEO
- **Metadata**: Open Graph and Twitter card tags are present for social sharing.
- **Sitemaps**: If adding new pages, include/refresh a sitemap and submit to search consoles.
- **Images**: Provide high-quality, optimized images with descriptive alt text.

## Analytics & Consent
- **GTM**: The site includes Google Tag Manager integration for analytics and marketing tags. Configure tags, triggers, and consent settings in your GTM container according to your privacy policy.

## Security
- **Static surface area**: No server-side code reduces attack vectors.
- **Headers**: Configure security headers at the CDN/host (HSTS, CSP, X-Content-Type-Options, Referrer-Policy).

## Maintenance Workflow
1. Create a feature branch for changes.
2. Update HTML/CSS/assets under `zaatarandzzas/`.
3. Preview locally with a static server.
4. Open a pull request for review.
5. Deploy after approval.

## License
All rights reserved. © Sizzle 'N Slice. If you need licensing or usage permissions, please contact the website administrators.

## Contact
For reservations or general inquiries, please visit the live site at `https://sizzlenslice.co.za/` and use the contact information provided there.
