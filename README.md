# synoralabs.eu — production metadata package

Drop every file into the ROOT of the GitHub Pages repo (same level as
index.html), then paste head-snippet.html into <head>.

| File | Purpose |
|---|---|
| favicon.svg | Primary favicon — vector, crisp at any size, all modern browsers |
| favicon.ico | Fallback for legacy browsers + tools that blindly request /favicon.ico (16/32/48) |
| apple-touch-icon.png | iOS home-screen / Safari icon (180×180, iOS rounds corners itself) |
| icon-192.png / icon-512.png | Android / PWA icons referenced by the manifest (512 is maskable-safe) |
| site.webmanifest | Site name, icons, theme color for Android + install surfaces |
| robots.txt | Allows all crawlers, points to the sitemap |
| sitemap.xml | Single-URL sitemap — add <url> entries as pages appear, bump <lastmod> |
| og-image.png | 1200×630 link preview for OG + Twitter (referenced absolutely in head snippet) |
| 404.html | GitHub Pages serves this automatically for unknown paths; branded, noindex |
| CNAME | Required by GitHub Pages for the synoralabs.eu custom domain |
| .nojekyll | Disables Jekyll processing (faster deploys, no underscore-file surprises) |
| head-snippet.html | Exact <head> tags to paste — reference only, not deployed |

Deliberately omitted:
- browserconfig.xml / msapplication tiles — only IE11 and legacy Edge read them; both are gone.
- The old wall of sized favicons — svg + ico + touch-icon + two manifest PNGs cover all 2026 browsers.

Before launch: finalize the description copy in head-snippet.html and
site.webmanifest, validate previews at opengraph.xyz, and submit
sitemap.xml in Google Search Console.
