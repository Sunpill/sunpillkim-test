# sunpillkim.com

Personal academic website of Sunpill Kim — Ph.D. candidate in Applied
Mathematics at Hanyang University, working on AI security.

Built with [Jekyll](https://jekyllrb.com/), hosted on
[GitHub Pages](https://pages.github.com/) at <https://sunpillkim.com>.

## Updating content

Almost all updates happen by editing YAML data files — no HTML required.

| What you want to do | Edit |
|---|---|
| Add a news item                | `_data/news.yml`         |
| Add a publication              | `_data/publications.yml` |
| Edit the about / hero          | `index.html`             |
| Edit the research narrative    | `research.html`          |
| Edit teaching / mentoring      | `teaching.html`          |
| Update navigation links        | `_data/nav.yml`          |
| Replace the portrait           | `assets/img/portrait.jpg`|
| Replace the CV                 | `assets/files/cv.pdf`    |
| Tweak global styles            | `_sass/main.scss`        |

### Adding a news item

```yaml
- date:    "2026-05-12"
  venue:   "NeurIPS 2026"
  tier:    "top"          # "top" gives the yellow highlight
  title:   "Paper title"
  authors: "<span class='me'>S. Kim</span>, et al."
```

For non-paper news (awards, talks, project starts), use `body:` instead of
`venue/title/authors`:

```yaml
- date:  "2026-02-05"
  body:  "Received the <strong>X Award</strong>."
```

### Adding a publication

```yaml
- title: "Paper title"
  authors: "<span class='me'>S. Kim</span>, et al."
  venue: "Full venue name"
  venue_short: "NeurIPS 2025"
  year: 2025
  category: "top-conf"   # top-conf | top-journal | conf | journal | preprint | other
  tier: "top"            # "top" for highlighted venues
  pdf: "https://..."     # optional
  code: "https://..."    # optional
  note: "co-first author · acceptance 24%"   # optional, free-form
```

Publications are auto-grouped on the page by `category`, sorted
newest-first within each group.

## Deployment

This repo can be deployed in two configurations. The `_config.yml` documents
both. Switch the `url` and `baseurl` values when moving between them.

### (1) Test deployment

`https://sunpill.github.io/sunpillkim-test/`

```yaml
url: "https://sunpill.github.io"
baseurl: "/sunpillkim-test"
```

The `CNAME` file should be **deleted** in this scenario.

### (2) Production at sunpillkim.com

```yaml
url: "https://sunpillkim.com"
baseurl: ""
```

The `CNAME` file should contain `sunpillkim.com`.

## Running locally

```bash
bundle install
bundle exec jekyll serve --livereload
# open http://localhost:4000
```

## License

Site code: MIT. Content (text, photos): © Sunpill Kim, all rights reserved.
