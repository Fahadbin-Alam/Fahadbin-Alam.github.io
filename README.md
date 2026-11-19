# Fahadbin-Alam.github.io

The files for the GitHub user site `https://fahadbin-alam.github.io`. They live in the Muslimo repo under
`user-site/` and are copied into the `Fahadbin-Alam.github.io` repository, which GitHub publishes from its
`main` branch.

Why it exists: the Muslimo repo used to be called `Islamic-Learning-Duolingo-Style`, and GitHub Pages does not
redirect a project site after a rename. Store listings, Play's Data safety form and every app build made before
the rename still open `https://fahadbin-alam.github.io/Islamic-Learning-Duolingo-Style/...`, so this site keeps
those links alive:

- `Islamic-Learning-Duolingo-Style/*.html` send the reader on to the same page under `/Muslimo/`.
- `Islamic-Learning-Duolingo-Style/app-version.json` is a real copy, not a redirect, because old builds fetch it
  for the "update available" banner. Every app that reads this old address is a pre-rename build, so once the
  first post-rename builds are live in both stores, set this copy to those build numbers once and leave it.
- `index.html` at the root sends visitors to the Muslimo support page. An AdMob `app-ads.txt` can go here too,
  since AdMob only looks at the root of the domain.

## `Muslimo/`: a standby copy of the main site

`Muslimo/` is a copy of the built Muslimo site (`scripts/build-site.mjs` in the Muslimo repo): support page,
privacy policy, delete-account, terms, stats, newsletter, log-in and `app-version.json`.

While the Muslimo repo is public, GitHub serves `https://fahadbin-alam.github.io/Muslimo/` from that repo's own
Pages site, which wins over this folder, so this copy is not seen. Once the Muslimo repo is private (GitHub Pages
then stops serving it on a free plan), this folder answers the same addresses, so the store links, the privacy and
delete-account links inside every app build and the "update available" check (`Muslimo/app-version.json`) keep
working without a new build.

Do not edit it by hand: the Muslimo repo's "Publish support and privacy pages" workflow copies the fresh build here
on every site change (it needs the `USER_SITE_TOKEN` secret in the Muslimo repo).
