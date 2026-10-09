# Personal website of Dakshansh Chawda

Static site served by GitHub Pages from the `main` branch. GitHub builds it with Jekyll on every push; there is no other build step.

## Structure

- `*.md` in the root: one file per page. `cv.md` is published as `cv.html`, and so on.
- `index.html`: the home page. It keeps its own HTML because of the image cards.
- `_layouts/default.html`: the shared shell (head, logo, menu, footer, scripts).
- `_layouts/page.html`: turns a Markdown page into the boxed layout. Text before the first `## heading` goes in the big title block; each `## heading` starts a new box; `### heading` is a sub-section inside a box.
- `_data/nav.yml`: the menu, in order. `_data/social.yml`: the icons next to it.
- `assets/`: the HTML5 UP "Massively" template. `assets/css/main.css` is edited by hand; the Sass in `assets/sass` is kept in step but is not compiled by the build.

## Page front matter

- `title`: browser tab title. `heading`: big title on the page, if different. `label`: small line above the title.

## Conventions

- A button: `[Label](https://example.com){: .button .small target="_blank"}`
- To add a page: create `name.md` with `layout: page`, then add it to `_data/nav.yml`.
- Do not write body text for the owner. Sections are left empty on purpose for him to fill in.

## Preview locally

`bundle install` once, then `bundle exec jekyll serve --livereload` and open http://localhost:4000
