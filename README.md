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

### Drafts

Add `draft: true` to a post's front matter to preview it on the live site without announcing it:

```markdown
---
title: Work in progress
draft: true
---
```

A draft is built and reachable at its URL (marked "Draft" next to the date), but it's left off the home page and the feed, and asks search engines not to index it. To publish, delete the `draft` line and push. The repository is public, so drafts are readable on GitHub too.

## Layout

- `_layouts/` — page templates (`default`, `post`)
- `index.html` — the home page post list
- `assets/css/style.css` — all styling
- `_config.yml` — site settings
