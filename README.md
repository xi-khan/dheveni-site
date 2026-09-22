# dheveni.com

The DheVeni landing page, privacy policy and terms. Static, no build step:
open `index.html` and it works.

Served by GitHub Pages from the repository root, with `CNAME` pointing at
`dheveni.com`.

## Files

| | |
|---|---|
| `index.html` | The landing page |
| `privacy.html` | Privacy policy. The App Store listing links here |
| `terms.html` | Terms of use |
| `site.css` | One stylesheet for all three |
| `fonts/mv-aammu.woff2` | MV Aammu FK, subset to Thaana and converted to WOFF2 (89KB to 13KB) |

## The Thaana font

`site.css` declares MV Aammu with a `unicode-range` covering the Thaana block,
so the browser only downloads it when there is Dhivehi on the page and Latin
text falls through to Figtree. That means `"MV Aammu"` can sit at the front of
every font stack without affecting English at all.

Dhivehi text needs `dir="rtl"` or the `.dv` class, which also gives it the
extra line height Thaana wants.
