# sadra-barikbin.github.io

My personal notebook — a culture-first site built with [Jekyll](https://jekyllrb.com/)
and the [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) theme,
tuned toward an editorial / literary feel.

Live at **https://sadra-barikbin.github.io** once GitHub Pages is enabled
(Settings → Pages → Build from the `main` branch).

## What's here

```
_config.yml              Site settings, author links, navigation defaults
_data/navigation.yml     Top navigation bar
index.html               Home — short intro + recent pieces
_pages/                  About, Pieces (archive), Contact
_posts/                  The pieces themselves (sample essay, verses, photo-essay)
assets/css/main.scss     Editorial typography + warm palette overrides
assets/images/           Abstract SVG artwork (placeholder — replace with your own)
_includes/head/custom.html   Loads the Playfair Display + Spectral webfonts
```

## Everyday tasks

**Add a new piece** — drop a Markdown file in `_posts/` named
`YYYY-MM-DD-the-title.md`:

```markdown
---
title: "The title"
date: 2026-06-06
categories: [pieces]
tags: [essay]          # essay · poetry · photographs · …
excerpt: "One line that shows up in the list."
header:
  teaser: /assets/images/teaser-essay.svg   # optional thumbnail
---

Your words here.
```

**Add an occasional technical report** — it's just a piece with a different tag:

```markdown
---
title: "A short technical note"
date: 2026-06-06
categories: [pieces]
tags: [technical]
---
```

**Use your own pictures** — add image files to `assets/images/` and point the
`teaser:` / `gallery:` paths at them. The included `.svg` files are placeholders.

**Personalise** — search the project for `[brackets]` and edit
`_pages/about.md`, `_pages/contact.md`, and the `author:` block in `_config.yml`.
To show a portrait in the footer/meta, add `assets/images/avatar.svg` (or `.jpg`)
and uncomment `author.avatar` in `_config.yml`.

## Preview locally (optional)

GitHub Pages builds the site automatically on every push, so this is only needed
if you want a live preview while editing:

```bash
bundle install
bundle exec jekyll serve   # → http://localhost:4000
```

Requires Ruby. The theme is pulled in as a remote theme, so there are no theme
files to manage locally.
