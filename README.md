# dheveni.com

The DheVeni landing page, privacy policy and terms. Static, no build step:
open `index.html` and it works.

Deployed on Vercel. `vercel.json` turns on `cleanUrls`, so `privacy.html` is
served at `/privacy` and anyone who hits `/privacy.html` is redirected there.
The app links to `/privacy` and `/terms`, so those are the real URLs.

## Files

| | |
|---|---|
| `index.html` | The landing page |
| `privacy.html` | Privacy policy. The App Store listing links here |
| `terms.html` | Terms of use |
| `site.css` | One stylesheet for all three |
| `vercel.json` | Clean URLs, cache headers for the font, a few security headers |
| `fonts/mv-aammu.woff2` | MV Aammu FK, subset to Thaana and converted to WOFF2 (89KB to 13KB) |

## The Thaana font

`site.css` declares MV Aammu with a `unicode-range` covering the Thaana block,
so the browser only downloads it when there is Dhivehi on the page and Latin
text falls through to Figtree. That means `"MV Aammu"` can sit at the front of
every font stack without affecting English at all.

Dhivehi text needs `dir="rtl"` or the `.dv` class, which also gives it the
extra line height Thaana wants.
