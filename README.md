# Portfolio Template

A single-page, bilingual (AR/EN) portfolio website — **vanilla HTML, CSS, and JavaScript**,
no framework, no build step, no dependencies. Drop it on any static host and it works.

## Features

- 🌗 **Dark / light theme** (dark by default), persisted across visits.
- 🌐 **Bilingual AR / EN** with a full RTL flip — edit the `I18N` dictionary in `script.js`.
- ✨ **Animated hero** — Canvas constellation background, gradient title, typing role loop.
- 🖥️ **Working terminal / command palette** — press `/` or `⌘/Ctrl + K`. Try `help`, `whoami`,
  `projects`, `open projects`, `theme`, `lang`.
- 📈 Animated stat counters, 3D-tilt project cards, magnetic buttons, cursor spotlight.
- ♿ Every motion effect respects `prefers-reduced-motion`; keyboard-navigable terminal + skip link.
- 📄 Printable **`resume.html`** (print-to-PDF), SEO meta + Open Graph, `robots.txt` + `sitemap.xml`.

## Structure

```
index.html              # the whole page (sections + i18n attributes + JSON-LD)
resume.html             # printable bilingual résumé (print-to-PDF)
styles.css              # tokens (dark/light), all sections, animations, RTL-safe, @media print
script.js               # theme, i18n, reveal, counters, typing, terminal, canvas, tilt, magnetic
favicon.svg             # logo placeholder (edit initials/gradient as you like)
robots.txt / sitemap.xml
.github/workflows/      # GitHub Pages deploy workflow
```

## Getting started — replace the placeholders

Every piece of personal content is a clearly marked placeholder. Search each file for the
strings below and replace them with your own info:

| Placeholder | Where | Replace with |
|---|---|---|
| `[Your Name]` | `index.html`, `script.js`, `resume.html`, `favicon.svg` | Your full name |
| `your@email.com` | `index.html`, `script.js`, `resume.html`, `license.txt` | Your email |
| `your-username` | `index.html`, `script.js`, `resume.html` | Your GitHub username |
| `yourdomain.com` | `index.html`, `robots.txt`, `sitemap.xml`, `resume.html` | Your live domain |
| `[Your University]` / `[Your City, Country]` | `index.html`, `script.js`, `resume.html` | Your education/location |
| `PUT-YOUR-IMAGE-URL-HERE` | `index.html` (`og:image` / `twitter:image`) | A hosted 1200×630 social preview image |
| Project A / Project B | `index.html`, `script.js`, `resume.html` | Your real project names, links, and screenshots |

The Arabic (`ar`) strings inside `I18N` in `script.js` and inside the embedded dictionary in
`resume.html` mirror the English content — update both languages together to keep them in sync.

## Run locally

No build step — just serve the folder:

```bash
python3 -m http.server 8000
# or
npx serve .
```

Then open <http://localhost:8000>.

## Deploy

Pushing to `main` triggers the GitHub Pages workflow (`.github/workflows/deploy.yml`). Enable
**Settings → Pages → Source: GitHub Actions** once, and the site publishes automatically.
Any other static host (Vercel, Netlify, Cloudflare Pages, etc.) works too — there's no build step.

## License

See [`license.txt`](license.txt) for the three usage tiers (Single-client, Extended, Unlimited/Agency).
