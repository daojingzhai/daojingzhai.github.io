# Daojing Zhai — Personal Website

Source for [daojingzhai.github.io](https://daojingzhai.github.io), the personal academic homepage of Daojing Zhai (PhD Candidate in Finance, Yale University).

Built with Jekyll, Bootstrap, and served via GitHub Pages.

## Local development

Requires Ruby + Bundler. From the repo root:

```bash
bundle install        # first time only
bundle exec jekyll serve
```

The site is then available at `http://localhost:4000`.

## Project structure

```
.
├── _config.yml         # Jekyll config
├── _layouts/default.html   # Page template (sidebar nav + content)
├── _includes/nav-bar.html  # Sidebar with avatar + nav links
├── index.html          # Home page (bio + research papers)
├── notes.html          # Notes page (asset pricing lecture notes)
├── css/, js/, fonts/   # Bootstrap assets
├── img/                # Avatar, name banner, favicon
├── pdfs/               # CV and job-market talk slides
├── papers/             # Working-paper PDFs linked from the home page
└── teaching/           # Lecture-note PDFs linked from the notes page
```

Full history and unpublished materials live in the private repository `daojingzhai.github.io-archive`.

## Adding a new paper to the home page

Each paper on `index.html` is a `<dd>` block containing the title link, an
optional coauthor line, action buttons (Abstract / Slides / etc.), and a
hidden `.abstract-box` toggled by `toggleAbstract(...)`. To add a paper, copy
an existing block and increment the abstract `id` (`abs1`, `abs2`, ...).

## Styling notes

Site-wide styling lives inline in `_layouts/default.html`:

- Unified Palatino Linotype typography.
- Yale-blue link palette (`#2C5DAA` / `#00356B`).
- `.action-btn` pill buttons for paper links.
- `.abstract-box` collapsible blocks for paper abstracts.
