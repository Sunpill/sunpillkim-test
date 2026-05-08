# sunpillkim.com

Personal academic website of Sunpill Kim — Ph.D. candidate in Applied
Mathematics at Hanyang University, working on AI security.

Built with [Jekyll](https://jekyllrb.com/), hosted on
[GitHub Pages](https://pages.github.com/) at <https://sunpillkim.com>.

## Updating content

The site is deliberately small. Almost all updates happen by editing
YAML data files — no HTML required.

| What you want to do | Edit |
|---|---|
| Add a news item                | `_data/news.yml`         |
| Add a publication              | `_data/publications.yml` |
| Edit the about / hero          | `index.html`             |
| Edit the research narrative    | `research.html`          |
| Edit the teaching philosophy   | `teaching.html`          |
| Update navigation links        | `_data/nav.yml`          |
| Replace the portrait           | `assets/img/portrait.jpg`|
| Replace the CV                 | `assets/files/cv.pdf`    |
| Tweak global styles            | `_sass/main.scss`        |

### Adding a news item

```yaml
- date:    "2026-05"
  venue:   "NeurIPS 2025"
  tier:    "top"          # "top" gives the yellow highlight
  title:   "Paper title"
  authors: "<span class='me'>S. Kim</span>, et al."
```

For non-paper news (awards, talks), use `body:` instead of
`venue/title/authors`:

```yaml
- date:  "2026-02"
  body:  "Received the <strong>X Award</strong>."
```

### Adding a publication

```yaml
- title: "Paper title"
  authors: "<span class='me'>S. Kim</span>, et al."
  venue: "Full venue name"
  venue_short: "NeurIPS 2025"
  year: 2025
  category: "top-conf"   # top-conf | top-journal | conf | journal | preprint
  tier: "top"            # "top" for highlighted venues
  pdf: "https://..."     # optional
  code: "https://..."    # optional
```

Publications are auto-grouped on the page by `category`, sorted
newest-first within each group.

## Running locally

```bash
bundle install
bundle exec jekyll serve --livereload
# open http://localhost:4000
```

## Deploying

Pushes to `main` are built automatically by GitHub Pages. The custom
domain is configured via the `CNAME` file at the repo root.

## License

Site code: MIT. Content (text, photos): © Sunpill Kim, all rights reserved.
