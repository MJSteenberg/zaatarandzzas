## Static site for Za'atar & Zza'ss

This folder is a static export suitable for GitHub Pages. It was scraped from WordPress and cleaned to remove dynamic dependencies (admin-ajax, REST, oEmbed, Elementor AJAX, Contact Form 7, Instagram dynamic JS).

Deploy on GitHub Pages by pushing this directory as the repository root (or to the `gh-pages` branch) and enabling Pages in Settings. The `.nojekyll` file disables Jekyll processing.

Notes:
- External WordPress endpoints are disabled. Interactive features relying on AJAX will not work.
- Most assets are local under `wp-content/` and `wp-includes/`.
- Update PDFs and images in `wp-content/uploads/` as needed.

