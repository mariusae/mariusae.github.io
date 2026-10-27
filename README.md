# mutable

Source for [mutable.org](https://mutable.org), built by GitHub Pages with Jekyll.

## Publishing

Add a Markdown file to `_posts/` named `YYYY-MM-DD-slug.md`:

```markdown
---
title: My post
---

Text goes here.
```

Commit and push to `main`. GitHub rebuilds the site, usually within a minute, and the post appears at `https://mutable.org/slug/`.

## Layout

- `_layouts/` — page templates (`default`, `post`)
- `index.html` — the home page post list
- `assets/css/style.css` — all styling
- `_config.yml` — site settings
