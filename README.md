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

### Writing published elsewhere

To list an essay hosted elsewhere, add a post with `layout: external` and its address:

```markdown
---
layout: external
title: RPC Redux
external: https://monkey.org/~marius/redux.html
---
```

If you only know the year, date the file January 1 and add `year_only: true`; the home page then shows just the year.

It's listed on the home page by its date, with an arrow, and links straight out. Its mutable.org URL redirects there. It's left out of the feed.

## Layout

- `_layouts/` — page templates (`default`, `post`, and `page` for standalone pages like `about.md`)
- `index.html` — the home page post list
- `assets/css/style.css` — all styling
- `_config.yml` — site settings
