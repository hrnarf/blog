# hrnarf-blog

A minimal Jekyll blog, set up to run on GitHub Pages for free, with zero build tooling required.

## What's in here

- `_config.yml` — site title, description, permalink structure
- `_layouts/` — page templates (default wrapper, home list, single post, static page)
- `_includes/` — header and footer, shared across every page
- `_posts/<year>/YYYY-MM-DD-title.md` — one Markdown file per blog post, organized into folders by year
- `about.md` / `now.md` — static pages
- `assets/css/style.css` — all the styling, one file

## Publishing this on GitHub Pages (free)

Already set up — Settings → Pages → Deploy from a branch → `main` → `/(root)`. Live at `https://hrnarf.github.io/blog/`.

## Post folder convention

Posts live in a folder per year, e.g.:

```
_posts/2026/2026-07-17-your-title-here.md
```

The `YYYY-MM-DD-` date prefix on the filename itself is required — Jekyll uses it to recognise the file as a dated post, regardless of which folder it sits in. The rest of the filename should be the post's title, slugified (lowercase, hyphens instead of spaces).

Front matter for a new post:

```markdown
---
layout: post
title: "Your Title Here"
date: 2026-07-17
---

Your post content, in Markdown, starts here.
```

## Workflow for publishing a new post

1. Draft the post (in Claude, or wherever).
2. Create a new branch, e.g. `post/2026-07-17-your-title-here`.
3. Add the post file to `_posts/<year>/` on that branch.
4. Open a pull request into `main`.
5. Review the PR (either party) and merge when ready — the site rebuilds automatically within a minute or two of merging.

## Previewing locally (optional)

```bash
gem install bundler jekyll
bundle init
bundle add jekyll
bundle exec jekyll serve
```

Then visit `http://localhost:4000`. Optional — GitHub Pages builds it for you regardless.

## Things left as placeholders

- `now.md` has placeholder goal categories — swap in your real ones from "Almost Halfway" whenever you're ready.
- `_config.yml` has an empty `url:` — fill this in once you know your final domain.
- Footer social links are commented as a placeholder — add your email/LinkedIn/X links in `_includes/footer.html`.
