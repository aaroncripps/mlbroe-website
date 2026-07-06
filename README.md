# mlbroe.com

The website for **Mary Lynn Broe** — Caroline Werner Gannett Professor of Humanities, Rochester Institute of Technology.

A full rebuild of the original (frameset-era) site into a single, modern, responsive static page. Same stack as stagetwopartners.io: hand-written HTML/CSS/JS in one file, Google Fonts (DM Serif Display + Inter), deployed via GitHub Pages with a custom domain.

## Structure

```
index.html          The entire site (markup + CSS + JS in one file)
CNAME               Custom domain for GitHub Pages (mlbroe.com)
images/             Portraits, book covers, and gallery photos
  books/            Book cover scans
  gallery/          Family and dog photos
DEPLOY.md           Step-by-step deployment guide
```

## Sections

Hero · Biography · Books · Scholarship (essays, papers, grants) · Courses · Gallery · Contact

## Content notes

All copy, images, and content were migrated from the original site. Contact details
(RIT email, department address, phone) are carried over from the original site and may
need updating. The original home-page portrait (`mlb1.jpg`) was missing from the source
files, so `broe_main.jpg` is used as the hero portrait.

## Editing

Everything lives in `index.html`. Edit text or styles there and re-commit; GitHub Pages
redeploys within about a minute. See `DEPLOY.md` for first-time setup and DNS.
