# Ośrodek Przystań — static mirror

This repository contains a static mirror of the public pages, articles, and categories listed in the source site's sitemaps at [osrodekprzystan.com](https://osrodekprzystan.com/), captured 5 November 2026. The pages and locally referenced assets are served from GitHub Pages.

GitHub Pages deploys the repository root on pushes to `main` using `.github/workflows/pages.yml`.

WordPress-only POST/AJAX forms are replaced with links to their original pages. Search uses the original site's search endpoint. Embedded third-party media remains embedded, and navigation to pages outside the published sitemap mirror continues to the source site.
