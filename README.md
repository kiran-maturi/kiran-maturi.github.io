# kiran-maturi.github.io

The landing page at **https://kiran-maturi.github.io/** — one card per kid app,
and nothing else.

| | |
|---|---|
| 🐱 [Talking Cat](https://kiran-maturi.github.io/talkingcat/) | say something and the cat repeats it in a silly voice ([source](https://github.com/kiran-maturi/talkingcat)) |
| 🧩 [Puzzle Play](https://kiran-maturi.github.io/kidpuzzles/) | drag-and-drop jigsaws, 4 to 25 pieces, ages 3–10 ([source](https://github.com/kiran-maturi/kidpuzzles)) |

Each app lives in its own repo and is served from its own path; this repo only
owns the root page that points at them.

## What is in here

One HTML file, one stylesheet, one favicon. **No JavaScript** — it is two links
and some drawing, which is all a page like this needs.

The card art is not a screenshot: the cat is drawn from the same geometry as
`talkingcat/js/cat.js`, and the jigsaw pieces come from the cutting code in
`kidpuzzles/js/pieces.js`. Both are inline SVG, so there are no image files to
go stale when an app changes.

Whole cards are links rather than the titles alone, because small fingers miss
small targets. A `@media (monochrome)` block flattens the page to high-contrast
black and white for the E Ink tablet the apps are also built for.

## Running it

```bash
python3 -m http.server 8766   # then open http://localhost:8766
```

## Deploying

The repo root is the site, published by `.github/workflows/pages.yml` on every
push to `main` (**Settings → Pages → Source: GitHub Actions**). Nothing is
built — the site is the source.
