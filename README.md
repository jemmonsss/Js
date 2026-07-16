# Portfolio

A personal portfolio site built with **Jekyll** and deployed to **GitHub Pages**
via GitHub Actions. Combines a data-driven links hub with a scalable projects
gallery.

## Features

- **Links hub** — edit `_data/links.yml` to add/remove links (no code changes).
  Includes a client-side search box.
- **Projects gallery** — add a Markdown file under `_projects/` to publish a
  project with its own page. Filter by category (tabs) and search by title/tag.
- Dark-gray + purple theme, fully responsive, self-hosted SCSS (no CDN build deps).
- Automated SEO: `jekyll-seo-tag` (OG/Twitter + **Person JSON-LD**),
  RSS (`jekyll-feed`), `sitemap.xml` (`jekyll-sitemap`, with 404/drafts
  excluded), and `robots.txt`.
- Favicon set (PNG + SVG + Apple Touch icon).
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

The `image` field is **optional**: if omitted, the card embeds a live preview
(`iframe`) of the project's `live_url` (the actual external site) instead of a
screenshot. Use `live_url` for the external site and `repo` for the source.

### Redirects (old/renamed URLs)

`jekyll-redirect-from` is enabled. Add to any page/project front matter:

```yaml
redirect_from:
  - /old-url/
  - /projects/old-slug/
```

### Search & filtering

Both the links hub and projects page have a search box (client-side, no plugin).
Projects additionally show category filter tabs. Cards carry `data-search` /
`data-category` attributes consumed by `_includes/filter-js.html`.

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
