# jonathanivorhill.github.io

GitHub Pages **user site**. The repo name has to stay exactly
`jonathanivorhill.github.io` — that is what makes it serve from the domain
root rather than a `/project-name/` subdirectory.

It exists for one load-bearing reason: **`app-ads.txt` is only ever crawled
from the root of a domain.** AdMob derives that domain from the developer
website on the Play store listing, and `github.io` is a private suffix on the
Public Suffix List, so the one URL that counts is:

```
https://jonathanivorhill.github.io/app-ads.txt
```

Without it, programmatic buyers treat Slingstar's inventory as unauthorized
and bid less, or not at all.

## Setup

1. Push to `main`.
2. Settings → Pages → Source: *Deploy from a branch*, `main` / `/ (root)`.
3. Confirm `https://jonathanivorhill.github.io/app-ads.txt` returns the file
   as `text/plain` — not a 404, and not an HTML error page.
4. Play Console → store listing → set the **Website** field to
   `https://jonathanivorhill.github.io/`. AdMob reads that field, not the
   privacy policy field, when deciding which domain to crawl.
5. AdMob → Apps → Slingstar → app-ads.txt → *Check for updates*. Crawls are
   not instant; allow a day or so.

The privacy policy itself lives in the separate `slingstar-privacy` repo and
is linked from `index.html`.
