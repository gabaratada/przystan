# Ośrodek Przystań — static mirror

This repository contains a static mirror of the public pages, articles, categories, and linked archives found from the source site's sitemaps at [osrodekprzystan.com](https://osrodekprzystan.com/), captured 6 November 2026. The pages and locally referenced assets are served from GitHub Pages.

GitHub Actions builds the repository with Jekyll and deploys the generated `_site` directory to GitHub Pages on pushes to `main` using `.github/workflows/pages.yml`. The captured pages use shared Jekyll includes for the site header, navigation, footer, consent panels, and recurring sidebar widgets. `_config.yml` preserves the `_external` directory and sets the project `baseurl` for links rendered from includes.

WordPress-only POST/AJAX forms are replaced with links to their original pages. Search uses the original site's search endpoint. Embedded third-party media remains embedded. Old source links with no working destination are routed to the nearest current local archive.
