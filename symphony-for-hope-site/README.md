# Symphony for Hope — Website

Static site for **Symphony for Hope**, presented by Second Harvest Food Bank of Northwest North Carolina in partnership with the Winston-Salem Symphony.

This is a plain HTML/CSS static site — no build step, no framework, no dependencies. Every page is a real `.html` file, so it works as-is on any static host (Netlify, GitHub Pages, S3, etc.).

## Structure

```
index.html              Home
about/index.html        About
the-music/index.html    The Music & Artists
events/index.html       Events
sponsorship/index.html  Sponsorship
donate/index.html       Donate
contact/index.html      Contact
404.html                Custom not-found page
assets/style.css        Shared stylesheet (all pages link to this)
assets/images/          Photos and logos used across the site
```

Each page folder uses the `folder/index.html` pattern so links resolve to clean URLs (e.g. `/events/` instead of `/events.html`) with zero server configuration.

## Running locally

No install needed. From this folder:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000/`.

## Deploying

This site is designed to be pushed to GitHub and deployed on Netlify (see the build guide for step-by-step instructions). Netlify's defaults work out of the box — no build command, publish directory is the repo root (`.`).

## Editing content

There's no templating system — the header, nav, and footer are duplicated at the top/bottom of every page file. When editing shared content (nav links, footer text, contact info), update it in all 7 page files (plus `404.html`) to keep them in sync.
