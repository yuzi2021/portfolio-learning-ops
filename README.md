# Portfolio — Sarah Yuzi Sandström

Learning coordination · LMS operations · Digital training

**Live site:** https://yuzi2021.github.io/portfolio-learning-ops/

A static portfolio presenting learning and digital training coordination work (international stakeholder coordination, LMS operations, content upkeep, staff training and documentation), built as plain HTML and CSS and deployed with GitHub Pages. Adapted from the HR technology portfolio.

## Pages

- `/` — homepage
- `/projects/` — selected work
- `/projects/privacy-security-awareness/` — GDPR guide & staff workshop case study
- `/about/` — about
- `/cv/` — CV

The CV PDF lives at `documents/Sarah_Sandstrom_CV.pdf` and is linked from the download button at the top of `cv/index.html`. To swap in a newer version, replace that file, keeping the filename so the link stays valid.

## Run locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000. Serve it this way rather than opening the files directly, so the fonts and styles load.

## Structure

Plain HTML per route with a shared `styles.css` for base styling and responsive breakpoints. Internal links are relative, so the site works both at the GitHub Pages sub-path and under a custom domain.

Note that `styles.css` targets the inline `style` strings in the markup (for example `[style*="300px minmax(0, 1fr)"]` and `[style*="padding: 0 80px 128px"]`) to fold the desktop layout down for tablet and mobile. New markup should reuse those exact inline strings, or it will not respond at the breakpoints.
