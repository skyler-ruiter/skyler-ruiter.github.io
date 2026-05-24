# skylerruiter.dev

Personal website for Skyler Ruiter, built with [Jekyll](https://jekyllrb.com/) using the [al-folio](https://github.com/alshedivat/al-folio) theme and hosted on GitHub Pages.

## Local Development

Requires [Docker](https://www.docker.com/). Technically not impossible to avoid using Docker, but it's likely not worth it.

```bash
docker compose pull && docker compose up
```

Site runs at `http://localhost:4000`. Rebuild after changing dependencies:

```bash
docker compose up --build
```

## License

The al-folio theme is available under the [MIT License](LICENSE).
