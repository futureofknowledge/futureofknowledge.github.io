# Future of Knowledge — Amsterdam 2026

Site for a two-day convening at the University of Amsterdam,
16–17 November 2026.

A Jekyll site served by GitHub Pages from the `master` branch. It uses the
[minimal](https://github.com/pages-themes/minimal) theme as a gem, via
`github-pages` — the theme's own layouts, SCSS and fonts are not vendored
here, so this repo holds only what is specific to the convening.

## Editing

| File | Contents |
|---|---|
| `index.md` | Overview |
| `programme.md` | Schedule |
| `public-session.md` | The open afternoon |
| `practical.md` | Venue, travel, expenses |
| `_config.yml` | Title, dates, sidebar navigation |
| `_layouts/default.html` | Page shell — sidebar, nav, footer |
| `assets/css/style.scss` | Styling on top of the theme |

Anything in [SQUARE BRACKETS] is a placeholder still to be filled.

To add a page: create `<name>.md` with `layout: default`, a `title:` and a
`permalink:`, then add it to `nav:` in `_config.yml`.

For a favicon or analytics, add the tags to the `<head>` in
`_layouts/default.html`.

## Local preview

Needs **Ruby 3.x** — `commonmarker`, pulled in by `github-pages`, declares
`< 4.0`, so Ruby 4 cannot resolve the bundle at all. CI builds on 3.2.

    bundle install
    bundle exec jekyll serve

Then open <http://localhost:4000>.

`Gemfile.lock` is deliberately not committed: GitHub Pages resolves its own
gem versions at build time, and pinning them here only drifts from what
actually ships.

## CI

Every push and pull request builds the site and runs
[html-proofer](https://github.com/gjtorikian/html-proofer) over the output to
catch broken internal links and missing images.
