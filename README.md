# Titus Tito — Portfolio

Personal portfolio site for Titus Tito, a Human-Centered Engineering Design student at the University of Michigan-Dearborn (Electrical Engineering Design concentration), focused on human factors and design research.

**Live site:** https://ttitus0815-coder.github.io/

## What's on the site

- **Home** — intro and quick facts
- **About Me** — background, goals, and skills
- **Work Experience** — current and past jobs
- **Education** — degree, coursework, and the 4+1 program
- **Projects** — line-following robot and MATLAB heat map simulation (each with its full report as a PDF download), plus Tito's Definitely Not Sketchy Bank, a Figma mobile app prototype from ART 210
- **Resume** — full resume with a PDF download
- **Contact** — email, phone, and LinkedIn

## How it's built

A single static page with no build step or dependencies:

```
index.html   All markup, styles, and the small script that switches pages
assets/      Photos and the PDF documents
```

### Documents

All PDFs are hosted in `assets/`, so they download straight from the site with no Google Drive or sign-in needed:

| File | Where it's linked | What it is |
|---|---|---|
| `Titus_Tito_Resume.pdf` | Resume page | One-page resume |
| `Line_Following_Robot_Report.pdf` | Projects → Line-Following Robot | Critical Design Review report (5 pages) |
| `Heat_Distribution_Report.pdf` | Projects → Heat Map Simulation | MATLAB heat distribution report (4 pages) |

Each document has a **Download** button (saves the file) and an **Open in new tab** link (views it in the browser).

Pages use hash links (`#/about`, `#/projects`, …), so each section has its own shareable URL. Fonts load from Google Fonts.

## Editing

1. Edit `index.html`. Each page is a `<div class="page" id="page-NAME">` block.
2. To update the resume, replace `assets/Titus_Tito_Resume.pdf` (keep the same filename) and update the resume text on the Resume page to match.
3. To update a project report, replace its PDF in `assets/` with the same filename. If the page count changes, update the "PDF · N pages" label next to its buttons in `index.html`.
4. To add a report to a new project, put the PDF in `assets/` and copy a `<div class="proj-actions">` block from an existing project card, changing the filename in both links.
5. To update the Figma bank app card, replace its screenshots in `assets/` (`bank-splash.jpg`, `bank-home.jpg`, `bank-send.jpg`, same filenames). The **Try the Prototype** and **View Design File** links are in that project card in `index.html`; update them if the Figma file moves.
6. To add a page, add a `page-NAME` block, a nav link with `data-page="NAME"`, and the name to `VALID_PAGES` and `PAGE_TITLES` in the script at the bottom.

## Previewing locally

```bash
python3 -m http.server 8000
```

If Python is not set up on your Mac, Ruby comes built in and works the same way:

```bash
ruby -run -e httpd . -p 8000
```

Then open http://localhost:8000.

## Deploying

The site is hosted on GitHub Pages from the `main` branch. Pushing to `main` updates the live site within a minute or two.

## Contact

[ttitus@umich.edu](mailto:ttitus@umich.edu) · [LinkedIn](https://www.linkedin.com/in/titus-tito-a75008399)
