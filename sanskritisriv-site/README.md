# sanskritisriv.me

Personal portfolio of Sanskriti Srivastava. One static page, no build step.

## What's in here

| File | What it does |
|---|---|
| `index.html` | The whole site: styles, mascot, notes and scripts are all inside. Photos are embedded too. |
| `favicon.svg` | The sticky-note icon in the browser tab. |
| `CNAME` | Tells GitHub Pages to serve the site on sanskritisriv.me. |
| `.nojekyll` | Tells GitHub Pages to serve files as they are. |
| `robots.txt`, `sitemap.xml`, `llms.txt` | SEO and AI-search basics. |
| `assets/photos/` | Original copies of the three "in the room" photos (the page doesn't load these; they're kept for editing). |

## Put it on GitHub Pages

1. Create a new public repository on GitHub, for example `sanskritisriv.me`.
2. Upload everything in this folder (including `.nojekyll` and `CNAME`) to the root of the repository.
   - Hidden files: on Mac press `Cmd + Shift + .` in Finder to see `.nojekyll`.
3. In the repository, go to **Settings → Pages**.
   - Source: **Deploy from a branch**
   - Branch: **main**, folder **/ (root)** → Save
4. Under **Custom domain**, type `sanskritisriv.me` and save. Tick **Enforce HTTPS** once it becomes available (can take up to a day).

## Point the domain at GitHub

In your domain provider's DNS settings:

| Type | Name / Host | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| CNAME | www | `<your-github-username>.github.io` |

Remove any old A or CNAME records that point to your previous host. DNS changes usually take a few minutes to a few hours.

## After it's live

1. Add the site to **Google Search Console** and **Bing Webmaster Tools**, and submit `https://sanskritisriv.me/sitemap.xml`.
2. Check `https://sanskritisriv.me/robots.txt`, `/sitemap.xml` and `/llms.txt` all open.
3. Run the homepage through **PageSpeed Insights**.

## Editing

- **Notes:** search `index.html` for `var NOTES = [`. Each note is one block; the comment above it explains every field.
- **Photos:** each photo is an `<img>` inside the "in the room" section. To replace one, put the new file in `assets/photos/` and change its `src` to `assets/photos/your-file.jpg`.
- **Sitemap date:** update `<lastmod>` in `sitemap.xml` when you make big changes.
