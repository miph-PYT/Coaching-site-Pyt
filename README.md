# parts-work.dk — coaching site

Static site, no build step. Published with GitHub Pages at www.parts-work.dk (see `CNAME`).

- `index.html` — home page
- `parts-work.html` — parts-work explainer
- `blog.html` — blog; posts come from `posts.json`
- `reflect/`, `reflect-new/` — session reflection forms for clients
- `.pages.yml` — Pages CMS setup for editing blog posts (cover photos go in `images/`)

Each page is self-contained: its styles and scripts are inside the HTML file. The three main pages share the same styles, so a design change in one should be copied to the other two.

## Publish with GitHub Pages
1. Upload these files to the root of the repo.
2. Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
