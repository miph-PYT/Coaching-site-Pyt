# parts-work.dk: coaching website

Philipp Mitterhofer's coaching website, live at **https://www.parts-work.dk**.

It's a plain website: each page is one HTML file with its own styles and scripts inside. There is no build step. Whatever is in the `main` branch is what's online (GitHub Pages publishes it within 1–2 minutes).

**Quick links**
- ✏️ Edit blog posts and workshops: **https://app.pagescms.org** (sign in with GitHub)
- 📖 How to add a workshop: **[WORKSHOPS.md](WORKSHOPS.md)**

---

## The pages

| Page | File | What's on it |
|---|---|---|
| **Home** | `index.html` | Hero, *This is for you if…* (`#who`), *How parts-work coaching can help you* (`#what-is`), *How I work* (`#offer`), *My story* (`#story`), *What I offer* with all offers and prices (`#work`), contact (`#contact`). |
| **Parts-work** | `parts-work.html` | What parts-work is and what happens in a session. |
| **Workshops** | `workshops.html` | The *Coffee with Your Inner Critic* workshop page, plus *More workshops* when you add others. Content comes from `workshops.json` (edit in Pages CMS). See [WORKSHOPS.md](WORKSHOPS.md). |
| **Blog** | `blog.html` | List of posts and the posts themselves. Content comes from `posts.json` (edit in Pages CMS). Includes the newsletter sign-up. |
| **Session reflection** | `reflect/index.html` → `parts-work.dk/reflect` | Client reflection form with a setup step only you see, and overall feedback. Hidden from search engines. |
| **First-session reflection** | `reflect-new/index.html` → `parts-work.dk/reflect-new` | *"After our first session"* reflection form, English and Danish. Hidden from search engines. |

The menu on every page links to: Parts-work, How I work, Story, Offers, Workshops, Blog, and the **Book** button.

---

## What you can edit without code (Pages CMS)

Go to **https://app.pagescms.org**, sign in with GitHub, choose **Coaching-site-Pyt** → **main**.

### Blog posts (`posts.json`)
1. **Blog posts** → **Add an entry**.
2. Fill in **Title**, **Web address** (lowercase, dashes, e.g. `my-new-post`), **Topic** (*Good kids*, *Parts work* or *Edges*), **Date**, **Reading time**, **Cover photo**, **Short intro** (shown on the blog overview) and **Text** (leave an empty line between paragraphs).
3. **Save**. The post is live after 1–2 minutes at `parts-work.dk/blog.html#` + the web address.

Cover photos you upload are stored in the `images/` folder.

### Workshops (`workshops.json`)
See **[WORKSHOPS.md](WORKSHOPS.md)** for the full step-by-step guide.

---

## What's written into the code

These things are not in the CMS. Change them in the HTML files (on GitHub: open the file → pencil icon → edit → **Commit changes**), or ask Claude to do it.

| What | Where |
|---|---|
| Offers and prices (free intro call, *A First Commitment*, *Three Months With Your Parts*, *A Full Season Inside*, single session, workshops) | `index.html`, section `#work` |
| Booking links (cal.com) | `index.html`, `parts-work.html`, `workshops.html`, `blog.html` |
| Contact email **Philipp@parts-work.dk** | Every page (footer and buttons) |
| Business address and CVR | Footer of every page |
| The menu | The `<header>` at the top of every page |
| The opening of the inner critic workshop page (label, title, question, crossed-out lines, first paragraphs) | `workshops.html`, near the top of `<main>` |

**Booking links in use**

| Link | Used for |
|---|---|
| `cal.com/philippm/coaching20` | Free 20-minute intro call |
| `cal.com/philippm/light` | *A First Commitment* |
| `cal.com/philippm/core` | *Three Months With Your Parts* |
| `cal.com/philippm/full` | *A Full Season Inside* |
| `cal.com/philippm/single-session` | Single session |

> **Design note:** Home, Parts-work and Blog share the same dark-teal styles. If you change the design of one, copy the change to the other two. The Workshops page has its own light "letter" design.

---

## How the moving parts work

| Feature | Where | How it works |
|---|---|---|
| **Floating parts** | Home, Parts-work, Blog | Soft coloured shapes drift on the right side of the page, react a little to the mouse and to scrolling, and gather together near the contact section. They're drawn in a `<canvas class="parts-layer">`. They never lock or block scrolling. People who've switched on *reduce motion* see them standing still. |
| **Journey line** | Home (*How I work*), Parts-work (*What happens in a session*) | A line draws itself between the numbered steps when the section comes into view. |
| **Crossed-out lines** | Workshops | The critic's lines get crossed out one by one, and a kinder question appears under each. |
| **Mobile menu** | Every page | On phones the top bar shows your name, **Book** and a ☰ button. Tapping ☰ opens the links as a list; tapping a link closes it. |
| **Workshops from the CMS** | Workshops | The page reads `workshops.json`. The first workshop fills the page; the others are listed under *More workshops*. Each one opens at `workshops.html#web-address`. Empty fields are hidden. |
| **Blog from the CMS** | Blog | The page reads `posts.json`. Each post opens at `blog.html#web-address`. |
| **Newsletter sign-up** | Blog | Opens the visitor's own email program with a ready-made message to Philipp@parts-work.dk (subject *Newsletter sign-up*). There's no mailing-list service behind it yet. |
| **Reflection forms** | `reflect/`, `reflect-new/` | Answers are sent to a Google Sheet through a Google Apps Script web app (the `script.google.com/macros/...` address in each form). If you ever make a new Apps Script, update that address in both forms. |

---

## Files

| File / folder | What it is |
|---|---|
| `index.html`, `parts-work.html`, `workshops.html`, `blog.html` | The main pages |
| `reflect/`, `reflect-new/` | The client reflection forms |
| `posts.json` | Blog posts (edited in Pages CMS) |
| `workshops.json` | Workshops (edited in Pages CMS) |
| `.pages.yml` | Tells Pages CMS which fields to show for blog posts and workshops |
| `images/` | Photos uploaded through Pages CMS |
| `philipp.jpg` | Photo on the home page |
| `favicon.ico`, `favicon.svg`, `apple-touch-icon.png`, `icon-192.png`, `icon-512.png`, `site.webmanifest` | Browser and phone icons |
| `CNAME` | Connects the site to www.parts-work.dk. Don't change it. |
| `README.md`, `WORKSHOPS.md` | These guides |

---

## Publishing

The site is published with **GitHub Pages**: *Settings → Pages → Deploy from a branch → `main` / `(root)`*. The domain **www.parts-work.dk** is registered at one.com and points to GitHub through the `CNAME` file.

Any change saved to `main` (from Pages CMS, from GitHub's editor or from Claude) is online after 1–2 minutes. If you don't see it, do a hard refresh (Ctrl + Shift + R / Cmd + Shift + R).

### Undo a change
Every save is stored in the repository history. On GitHub, open **Commits**, find the change, and use **Revert**, or ask Claude to undo it.
