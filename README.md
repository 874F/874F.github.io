# misc.lol

Personal homepage — open source, self-hosting & privacy-first infrastructure.

**Live:** <https://874f.github.io/>

A deliberately minimal, standards-compliant static site. No frameworks, no build
step, no JavaScript, no trackers. Just HTML, CSS, five photos and a Brewfile —
because some of us still subscribe to c't.

## Structure

| Path                          | Purpose                                                  |
|-------------------------------|----------------------------------------------------------|
| `index.html`                  | The entire site                                          |
| `Linux.jpeg`                  | Linux — user and occasional admin since 2000             |
| `print.jpeg`                  | Print tech magazines (loyal c't subscriber)              |
| `mini-rack.jpeg`              | Homelab — mini rack with Pis and Ugreen DXP2800 TrueNAS  |
| `desk.jpeg`                   | Desk setup — GrapheneOS Android Desktop Mode             |
| `3d-printer.jpeg`             | 3D printer — Bambu Lab P1S (LAN-only)                    |
| `robots.txt`                  | Crawler rules (allow all) + sitemap reference            |
| `sitemap.xml`                 | Single-URL sitemap for search engines                    |
| `.nojekyll`                   | Tells GitHub Pages to skip Jekyll processing             |
| `.github/workflows/html-check.yml` | Strict W3C + lint validation + link check (non-blocking) |

## Features

- Responsive layout (mobile-first), automatic dark mode via `prefers-color-scheme`
- SEO metadata: description, canonical URL, Open Graph tags, sitemap, robots.txt
- Inline SVG favicon and hand-drawn blue Tux mascot — no extra asset files
- Accessible: heading hierarchy, `:focus-visible`, `prefers-reduced-motion`,
  print stylesheet
- `rel="noopener noreferrer"` on all external links

## Development

No build step — edits go straight to `main`.

## Quality checks

Every push containing HTML files is validated by the [Nu HTML Checker](https://validator.github.io/validator/)
(W3C reference validator) and `html-validate`, plus a link checker for dead
URLs. Results appear as annotations on commits and in the job summary —
the pipeline reports issues but never fails the build.

## License

All rights reserved. The site content is personal; feel free to browse and
get inspired, but please don't copy it wholesale.
