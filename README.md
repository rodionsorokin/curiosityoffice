# curiosityoffice.com

Static one-page site. No build step: GitHub Pages serves `index.html` from the root of `main`.

## Publish

1. Settings → Pages → Source: **Deploy from a branch**, Branch: **main**, folder **/ (root)**. Save.
2. Custom domain is already set by the `CNAME` file (`curiosityoffice.com`).
3. Add the DNS records below at your domain registrar.
4. When Pages shows the DNS check as passed, tick **Enforce HTTPS** (the certificate can take up to an hour).

## DNS records

Remove any old A / AAAA / CNAME records for `@` and `www` first (for example, the ones pointing to Readymag).

| Type  | Name  | Value                   |
|-------|-------|-------------------------|
| A     | @     | 185.199.108.153         |
| A     | @     | 185.199.109.153         |
| A     | @     | 185.199.110.153         |
| A     | @     | 185.199.111.153         |
| AAAA  | @     | 2606:50c0:8000::153     |
| AAAA  | @     | 2606:50c0:8001::153     |
| AAAA  | @     | 2606:50c0:8002::153     |
| AAAA  | @     | 2606:50c0:8003::153     |
| CNAME | www   | rodionsorokin.github.io |

MX records for email (rodion@curiosityoffice.com) stay as they are.

## Editing

- `index.html` holds all markup and CSS.
- `img/` holds the drawings and client logos.
- Body font: Graphik is listed first in `--sans`; until woff2 files are added and declared with `@font-face`, browsers fall back to Inter from Google Fonts. Testimonials use Crimson Pro italic.
