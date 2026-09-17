# christopher-perdriau.github.io

Personal academic/industry portfolio site for Christopher Perdriau, built with
[Jekyll](https://jekyllrb.com/) and deployed on GitHub Pages.

## Theme

Uses [minimal-mistakes](https://mmistakes.github.io/minimal-mistakes/) loaded
via the `remote_theme` mechanism (see `_config.yml`), so it builds on GitHub
Pages' infrastructure with no custom build step. Chosen over `academicpages`
(a minimal-mistakes fork built specifically for academic sites) because this
site's needs — a publications list, a teaching page, a projects page, a CV
page — are fully covered by minimal-mistakes' standard pages/data-file
patterns, without academicpages' extra portfolio/talks collections and
BibTeX-import tooling this site doesn't use.

## Local development

```bash
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Structure

- `_config.yml` — site settings, nav, author/social links
- `_data/navigation.yml` — top nav
- `_data/publications.yml` — structured publication list rendered by
  `_pages/publications.md`
- `_pages/` — Research & Publications, Teaching, Projects, CV, Contact
- `index.md` — About / home page
- `assets/files/cv.pdf` — downloadable CV
- `assets/images/headshot.jpg` — profile photo (swap this single file to
  change the photo used site-wide)
- `source-materials/` — raw source documents (research/teaching statements,
  original CV, resume notes) used to write site content. Gitignored, not
  part of the published site.

## Content notes

- Publication list should be spot-checked against [Google Scholar](https://scholar.google.com/citations?user=-cDZEO8AAAAJ&hl=en)
  before relying on it — the two "under review" entries may have since been
  published.
- Contact email is assembled client-side via a small inline script
  (`_pages/contact.md`) to reduce scraping, with a `<noscript>` fallback
  pointing to GitHub/Google Scholar.
