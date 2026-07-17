# hrnarf-blog

A minimal Jekyll blog, set up to run on GitHub Pages for free, with zero build tooling required.

## What's in here

- `_config.yml` — site title, description, permalink structure
- `_layouts/` — page templates (default wrapper, home list, single post, static page)
- `_includes/` — header and footer, shared across every page
- `_posts/` — one Markdown file per blog post, filename format `YYYY-MM-DD-title.md`
- `about.md` / `now.md` — static pages, same idea as your current site
- `assets/css/style.css` — all the styling, one file

## Publishing this on GitHub Pages (free)

1. Repo: `hrnarf/blog` (public).
2. Push everything in this folder to that repo.
3. In the repo, go to **Settings → Pages**.
4. Under "Build and deployment", set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
5. GitHub will build the site automatically — Jekyll is built into GitHub Pages, so no GitHub Actions or extra config needed.
6. Your site will be live at `https://hrnarf.github.io/blog/` (or your custom domain, if you set one up under Settings → Pages → Custom domain).

## Writing a new post

Add a new file to `_posts/`, named like:

```
_posts/2026-07-17-your-title-here.md
```

With this at the top:

```markdown
---
layout: post
title: "Your Title Here"
date: 2026-07-17
---

Your post content, in Markdown, starts here.
```

Commit and push — the live site updates automatically within a minute or two.

## Previewing locally (optional)

If you want to see changes before pushing, you'll need Ruby + Jekyll installed locally:

```bash
gem install bundler jekyll
bundle init
bundle add jekyll
bundle exec jekyll serve
```

Then visit `http://localhost:4000`. This step is optional — GitHub Pages will build it for you regardless.

## Next steps / things left as placeholders

- `now.md` has placeholder goal categories — swap in your real ones from "Almost Halfway" whenever you're ready.
- `_config.yml` has an empty `url:` — fill this in once you know your final domain (GitHub subdomain or custom domain).
- Footer social links are commented as a placeholder — add your email/LinkedIn/X links in `_includes/footer.html`.
