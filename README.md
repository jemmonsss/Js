# Portfolio

A personal portfolio site built with **Jekyll** and deployed to **GitHub Pages**
via GitHub Actions. Combines a data-driven links hub with a scalable projects
gallery.

## Features

- **Links hub** — edit `_data/links.yml` to add/remove links (no code changes).
- **Projects gallery** — add a Markdown file under `_projects/` to publish a
  project with its own page.
- Dark-gray + purple theme, fully responsive, self-hosted SCSS (no CDN build deps).
- Automated SEO (`jekyll-seo-tag`), RSS (`jekyll-feed`), and `sitemap.xml`
  (`jekyll-sitemap`).
- Auto-build + deploy on every push to `main`.

## Local development

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Adding content

### A link

Append to the relevant category (or add a new one) in `_data/links.yml`:

```yaml
Socials:
  - title: GitHub
    url: https://github.com/yourname
    icon: fa-brands fa-github
```

Each entry supports one of `icon` (FontAwesome class), `image` (URL), or `svg`
(raw HTML).

### A project

Copy `templates/project-template.md` to `_projects/<slug>.md` and fill in the
front matter. The gallery and a per-project page are generated automatically.

## Deployment

1. Push to `main`.
2. In repo **Settings → Pages**, set **Source = GitHub Actions**.

The `.github/workflows/jekyll.yml` workflow builds and deploys on every push.

## Configuration

Edit `_config.yml`:

- `title`, `description`, `author`, `url` — site identity.
- `baseurl` — `""` for a user/org site, `"/repo"` for a project page.
- `collections.projects` — gallery settings.
- `plugins` — GitHub-Pages-safelisted only.
