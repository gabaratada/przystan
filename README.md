# Ośrodek Przystań — static mirror

This repository contains a static mirror of the public pages, articles, categories, and linked archives found from the source site's sitemaps at [osrodekprzystan.com](https://osrodekprzystan.com/), captured 6 November 2026. GitHub Pages serves the Jekyll-built site.

## Source layout

- `pages/` contains the mirrored HTML sources. Each page declares a Jekyll `permalink` so the public URL stays the same even though the source files are grouped separately.
- `assets/media/` contains captured uploads; `assets/theme/` contains theme resources; `assets/vendor/` contains plugin, runtime, and icon assets; `assets/external/` contains captured third-party resources; and `assets/css/` contains local stylesheets.
- `_includes/` contains the shared header, navigation, footer, consent panels, and recurring sidebar widgets.
- `pages/legacy-routes/` contains small redirects that preserve the former `/wordpress/.../` URLs and point to the canonical pages.

GitHub Actions builds pull requests with Jekyll using `.github/workflows/jekyll-check.yml`. The deployment workflow builds and publishes the generated `_site` directory to GitHub Pages on pushes to `main` using `.github/workflows/pages.yml`. `_config.yml` sets the site URL and project `baseurl` for generated asset, redirect, and navigation links.

Backend POST/AJAX forms are replaced with links to their original pages. Search and three gallery load-more controls still use the source site's endpoints. Embedded third-party media remains embedded. Old source links with no working destination are routed to the nearest current local archive.
