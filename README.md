# Titus Tito — Portfolio

Personal portfolio site for Titus Tito, a Human-Centered Engineering Design student at the University of Michigan-Dearborn (Electrical Engineering Design concentration), focused on automotive UX and human factors.

**Live site:** https://ttitus0815-coder.github.io/

## What's on the site

- **Home** — intro and quick facts
- **About Me** — background, goals, and skills
- **Work Experience** — current and past jobs
- **Education** — degree, coursework, and the 4+1 program
- **Projects** — line-following robot and MATLAB heat map simulation
- **Resume** — full resume with a PDF download
- **Contact** — email, phone, and LinkedIn

## How it's built

A single static page with no build step or dependencies:

```
index.html   All markup, styles, and the small script that switches pages
assets/      Photos and the resume PDF
```

Pages use hash links (`#/about`, `#/projects`, …), so each section has its own shareable URL. Fonts load from Google Fonts.

## Editing

1. Edit `index.html`. Each page is a `<div class="page" id="page-NAME">` block.
2. To update the resume, replace `assets/Titus_Tito_Resume.pdf` (keep the same filename) and update the resume text on the Resume page to match.
3. To add a page, add a `page-NAME` block, a nav link with `data-page="NAME"`, and the name to `VALID_PAGES` and `PAGE_TITLES` in the script at the bottom.

## Previewing locally

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.

## Deploying

The site is hosted on GitHub Pages from the `main` branch. Pushing to `main` updates the live site within a minute or two.

## Contact

[ttitus@umich.edu](mailto:ttitus@umich.edu) · [LinkedIn](https://www.linkedin.com/in/titus-tito-a75008399)
