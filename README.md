# kellyj83.github.io

Personal site for Jonathan Kelly — [kellyj83.github.io](https://kellyj83.github.io).

A single-page Jekyll site, deployed automatically by GitHub Pages from `master`.

## Layout

| Path | What it's for |
| --- | --- |
| `index.md` | The "About" prose. Everything else is generated. |
| `_data/projects.yml` | The project cards — title, summary, image, tags, stats, links. |
| `_config.yml` | Name, role, tagline, contact details, social links. |
| `_layouts/homepage.html` | Page structure and `<head>` metadata. |
| `_sass/site.scss` | All styling. Colours live in the custom properties at the top. |
| `assets/js/site.js` | Sticky-nav shadow and scroll reveal. |
| `files/`, `images/` | Project write-ups (PDFs / exported notebooks) and their figures. |

## Adding a project

Append an entry to `_data/projects.yml`:

```yaml
- title: Name of the project
  image: /images/figure.png
  alt: What the figure shows
  summary: >-
    A couple of sentences on what it does and how.
  stats:                      # optional
    - label: Sharpe ratio
      value: "~2.0"
  tags: [Python, Something]   # optional
  links:
    - label: Project doc
      url: /files/write-up.html
      primary: true
```

Set `featured: true` on one project to give it the wide card at the top of the
grid. Figures sit on a white tile at 16:10 (16:9 when featured) and are scaled
to fit, so exported matplotlib plots work as-is.

## Running it locally

```bash
bundle install
bundle exec jekyll serve
```

Then open <http://localhost:4000>.

## Credits

Originally forked from the [Strata Academic](https://github.com/yaoyao-liu/strata-academic)
theme, itself based on [Strata](https://html5up.net/strata) by HTML5 UP. The
layout and stylesheet have since been rewritten.
