# CLAUDE.md - Project Context

## Project Overview

Personal website for Sudarshan Sharma (MLE @ Apple). Built with Jekyll and hosted on GitHub Pages at `www.sudarshan-sh.com`.

## Tech Stack

- **Static Site Generator:** Jekyll 3.9.3
- **Theme:** Minimal Mistakes Jekyll Theme (skin: "neon")
- **Template Origin:** AcademicPages fork (cleaned up)
- **Hosting:** GitHub Pages (auto-deploys from `master` branch)
- **Domain:** www.sudarshan-sh.com (CNAME configured)
- **CSS:** SCSS/SASS compiled by Jekyll
- **JS:** jQuery 1.12.4 + plugins (minified via uglify-js)
- **Templating:** Liquid
- **Markdown Engine:** kramdown with Rouge highlighting
- **Comments:** Disqus
- **Analytics:** Google Universal Analytics

## Local Development

```bash
bundle exec jekyll serve
```

For JS asset rebuilds:
```bash
npm run build:js    # one-time uglify
npm run watch:js    # watch mode
```

Ruby deps managed via `Gemfile` / `bundle install`. Node deps via `package.json` / `npm install`.

## Directory Structure

```
_config.yml          # Main Jekyll config (site settings, author, collections, plugins)
_config.dev.yml      # Dev overrides (disables analytics, expanded SCSS)
_data/
  navigation.yml     # Top nav menu items
  authors.yml        # Author metadata
_layouts/            # Page layout templates (default, single, archive)
_includes/           # Reusable HTML partials (head, footer, sidebar, analytics, comments)
_pages/              # Static pages (about.md is the homepage at permalink: /)
_posts/              # Blog posts (YYYY-MM-DD-slug.md format)
_sass/               # SCSS source files + vendor styles
assets/
  css/main.scss      # Main stylesheet entry point
  js/                # JavaScript (source + minified)
  fonts/             # Font files
images/              # Static images and icons
files/               # PDFs (research papers, downloadables)
```

## Key Files

| File | Purpose |
|------|---------|
| `_config.yml` | All site-wide settings, author profile, collection definitions, plugin list |
| `_pages/about.md` | **Homepage** (permalink: `/`). Main profile and bio content |
| `_pages/publications.md` | Publications listing page |
| `_data/navigation.yml` | Top navigation menu structure |
| `assets/css/main.scss` | CSS entry point (imports theme + custom overrides) |
| `CNAME` | Custom domain configuration |

## Content Conventions

- **Blog posts** go in `_posts/` with filename format `YYYY-MM-DD-slug.md`
- **Front matter** typically includes: `title`, `date`, `permalink`, `tags`, `author_profile`, `comments`, `share`, `related`
- **Navigation** is defined in `_data/navigation.yml` (currently: Publications, Blog)
- **Portfolio** collection is configured in `_config.yml` with `output: true`
- **PDFs** for papers are stored in `files/`
- **Images** go in `images/`

## Theme Customizations

- Link color overridden to red in `assets/css/main.scss`
- Paragraph indent enabled
- Neon skin selected in `_config.yml`
- HTML compression via `_layouts/compress.html`

## Plugins

jekyll-feed, jekyll-seo-tag, jemoji, jekyll-redirect-from, jekyll-gist, jekyll-paginate

## Important Notes

- The `_site/` directory is the build output (gitignored, auto-generated)
- The about page (`_pages/about.md`) serves as the homepage
- Publications are inline in `_pages/publications.md` (not a Jekyll collection)
- Vendor directory and `.bundle/` are gitignored
