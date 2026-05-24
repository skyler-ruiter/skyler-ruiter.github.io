# Local Development

## Prerequisites

- Docker Desktop (v28+)
- Docker Compose (v2+)

## Starting the site

```bash
docker compose up
```

Site is available at http://localhost:4000

The server watches for file changes and live-reloads automatically. Changes to `_config.yml` trigger a full Jekyll restart.

## Stopping the site

```bash
docker compose down
```

Or just `Ctrl+C` in the terminal running `docker compose up`.

## Rebuilding the image

Only needed when `Gemfile` changes (adding/removing gems):

```bash
docker compose down
docker compose build
docker compose up
```

## Key directories

| Path | Purpose |
|---|---|
| `_config.yml` | Site-wide settings, social links, feature flags |
| `_pages/` | Static pages (about, cv, projects, etc.) |
| `_posts/` | Blog posts (filename: `YYYY-MM-DD-title.md`) |
| `_projects/` | Project cards shown on the projects page |
| `_bibliography/papers.bib` | Publications (BibTeX format, rendered by jekyll-scholar) |
| `_news/` | News/announcement items shown on the homepage |
| `assets/img/` | Images |
| `old_site/` | Old Minima site — excluded from build, kept for reference |

## Notes

- `Gemfile.lock` is gitignored — it is generated fresh inside the container on each startup.
- JS minification is handled by `jekyll-minifier` (`jekyll-terser` was removed as it is not on rubygems).
- The published site uses GitHub Actions to build (required for `jekyll-scholar`). See `.github/workflows/` for the deploy workflow.
