# Fahadbin-Alam.github.io

The files for the GitHub user site `https://fahadbin-alam.github.io`: Fahadbin Alam's portfolio at the root, plus
redirects that keep old Muslimo links working.

GitHub only serves a repository at the root of `https://fahadbin-alam.github.io` when the repository is named
exactly `Fahadbin-Alam.github.io` (case does not matter) and Pages is turned on for its `main` branch. Under any
other name it is a project site served at `https://fahadbin-alam.github.io/<repo-name>/`, and none of the paths
below work.

The Muslimo redirect files were first written in the Muslimo repo under `user-site/` and copied here. The root
portfolio (`index.html`, `404.html`, `favicon.svg`, `og-image.png`, `robots.txt`, `sitemap.xml`) is maintained
in this repository; if you copy `user-site/` over again, don't overwrite those files.

## Portfolio

- `index.html` is a single self-contained page (inline CSS, no JavaScript, no web fonts) so it loads fast.
- To link a résumé PDF, commit it as `resume.pdf` and point the two "Résumé" links in `index.html` at it
  (search for `RESUME`).
- `og-image.png` is the 1200x630 preview image shown when the link is shared on LinkedIn, Slack, etc.

## Muslimo redirects

Why they exist: the Muslimo repo used to be called `Islamic-Learning-Duolingo-Style`, and GitHub Pages does not
redirect a project site after a rename. Store listings, Play's Data safety form and every app build made before
the rename still open `https://fahadbin-alam.github.io/Islamic-Learning-Duolingo-Style/...`, so this site keeps
those links alive:

- `Islamic-Learning-Duolingo-Style/*.html` send the reader on to the same page under `/muslimo/`.
- `Islamic-Learning-Duolingo-Style/app-version.json` is a real copy, not a redirect, because old builds fetch it
  for the "update available" banner. Every app that reads this old address is a pre-rename build, so once the
  first post-rename builds are live in both stores, set this copy to those build numbers once and leave it.
- An AdMob `app-ads.txt` can go at the root of this repo, since AdMob only looks at the root of the domain.
  (The root `index.html` used to redirect to `/muslimo/`; it is now the portfolio, which links to Muslimo.)
