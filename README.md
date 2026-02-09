# sudarshan-sh.com

Personal website of Sudarshan Sharma — Machine Learning Engineer at Apple.

Built with Jekyll using the Minimal Mistakes theme, hosted on GitHub Pages.

## Live Site

[www.sudarshan-sh.com](https://www.sudarshan-sh.com)

## Local Development

**Prerequisites:** Ruby, Bundler, Node.js

```bash
# Install dependencies
bundle install
npm install

# Serve locally
bundle exec jekyll serve

# JS asset rebuilds
npm run build:js    # one-time uglify
npm run watch:js    # watch mode
```

## Project Structure

```
_config.yml       # Site settings, author profile, plugins
_pages/           # Static pages (about.md = homepage, blog)
_posts/           # Blog posts (YYYY-MM-DD-slug.md)
_includes/        # Reusable HTML partials
_layouts/         # Page layout templates
_sass/            # SCSS source files
_data/            # Navigation and author metadata
assets/           # CSS, JS, and fonts
images/           # Static images
```

## License

Based on [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) Jekyll theme, MIT License.
Forked from [AcademicPages](https://github.com/academicpages/academicpages.github.io).
