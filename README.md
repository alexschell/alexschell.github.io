# Personal site

A minimal Jekyll starter for a personal site + blog with a retro Times New Roman look. The whole thing is about 50 lines of CSS and four short HTML layouts. It's meant to be read, modified, and made yours.

## Structure

```
.
├── _config.yml             site-wide settings
├── _layouts/
│   ├── default.html        shared shell: nav, CSS, optional KaTeX
│   ├── post.html           blog post wrapper
│   └── essay.html          essay wrapper
├── _posts/                 dated blog posts (YYYY-MM-DD-slug.md)
├── _essays/                undated longer pieces
├── assets/
│   └── style.css           the entire visual design
├── index.md                homepage
├── blog.md                 list of all posts
├── essays.md               list of all essays
└── contact.md              contact page
```

## Running locally

You'll need Ruby installed. Then:

```
bundle install
bundle exec jekyll serve
```

Visit http://localhost:4000.

## Deploying to GitHub Pages

1. Create a repo. If you name it `yourusername.github.io`, the site will live at the root of that domain. Otherwise it'll live at `yourusername.github.io/reponame`.
2. Push these files to the `main` branch.
3. In repo Settings → Pages, set the source to "Deploy from a branch" → `main` → `/ (root)`.
4. Wait ~30 seconds. Done.

## Adding a blog post

Drop a Markdown file in `_posts/` named `YYYY-MM-DD-title.md`:

```
---
title: My new post
date: 2026-05-15
---

Write here.
```

## Adding an essay

Drop a Markdown file in `_essays/`. No date required in the filename, but you can include one in frontmatter if you want it shown:

```
---
title: Some essay
date: 2024-09
---
```

## Adding LaTeX

Set `math: true` in the frontmatter of any post or essay. KaTeX will load on that page only. Use `$...$` for inline math and `$$...$$` for display math.

## Customizing

- **Site title, your name, email**: edit `_config.yml`.
- **Nav links**: edit `_layouts/default.html`.
- **Visual style**: edit `assets/style.css`. Almost everything visual is in there.
- **Adding a new top-level page** (e.g. `now.md`, `reading.md`): create the file at the root with frontmatter `layout: default` and `permalink: /now/`.
