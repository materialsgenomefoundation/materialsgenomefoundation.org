# materialsgenomefoundation.org

Source for the [Materials Genome Foundation](https://materialsgenomefoundation.org) website: a static site built with [Hugo](https://gohugo.io) 

## Quick start

```sh
hugo server            # live preview
hugo --gc --minify     # production build into ./public
```

## Common edits

**Add a workshop.** Add an entry to the top of `data/workshops.yaml`. Workshops dated after the build date appear under "Upcoming workshops" automatically, and move to "Past workshops" on the first build after that date. Add `playlist:` (the ID after `list=` in a YouTube playlist URL) if recordings exist, and `featured: true` to also show the playlist under "Recordings".

**Add or edit software.** Edit `data/software.yaml`. Logos go in `static/images/logos/` (SVG preferred). The order in the file is the order on the page. To change which tools appear in the home page banner, edit `featured:` in `content/_index.md`. Banner tools look best with a `badge:` image: a square version of the logo, optically centered and sized to sit inside the circle (see `static/images/logos/badges/`). Without one, the regular logo is centered by its bounding box.

**Colors and type.** the colors `--green` and `--blue` are sampled from the logo mark; the `-ink` variants are darker shades used for text so it stays readable on white.

## Deploying

The site is deployed to Cloudflare Pages on commits to main.
Deployments are set up and managed on Cloudflare's dashboard.
The development server can be viewed by https://materialsgenomefoundation-org.pages.dev

