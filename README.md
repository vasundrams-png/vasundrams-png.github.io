# M S Vasundra: Portfolio

A single-page portfolio (HTML, CSS and JavaScript all inside `index.html`). No frameworks, no build step, no backend.

## Folder structure
```
portfolio/
├── index.html
├── README.md
└── assets/
    ├── resume.pdf              <- your resume (replace this file to update it)
    ├── certs/
    │   ├── aws/                <- 4 AWS practice exam completion certificates
    │   └── mongodb/            <- 5 MongoDB certificates
    ├── projects/               <- project screenshots
    └── events/                 <- optional: put event photos/certificates here
```

## Open in VS Code
1. Unzip the folder and open it in VS Code (File > Open Folder > `portfolio`).
2. Install the **Live Server** extension, right-click `index.html`, choose **Open with Live Server**.
   (PDF previews and fonts work best through a server rather than double-clicking the file.)

## Publish on GitHub Pages
1. Create a new repository on GitHub, for example `portfolio` (public).
2. Upload everything inside this folder (`index.html`, `README.md`, `assets/`) so `index.html` sits at the top level of the repo.
   Or from a terminal inside the folder:
   ```
   git init
   git add .
   git commit -m "Add portfolio"
   git branch -M main
   git remote add origin https://github.com/vasundrams-png/portfolio.git
   git push -u origin main
   ```
3. In the repo go to **Settings > Pages**. Under *Build and deployment*, set Source to **Deploy from a branch**, Branch **main**, folder **/ (root)**, then Save.
4. After a minute your site is live at `https://vasundrams-png.github.io/portfolio/`.

## How to update things
All editable content is in the `CONFIG` block at the start of the `<script>` in `index.html`:
- **LeetCode:** set `LEETCODE_URL` to your profile link. Until then the button stays hidden.
- **Project screenshots:** drop an image into `assets/projects/` and set that project's `image` path. Projects with `image:""` show a CSS placeholder. InfraPulse AI and the blood group idea use SVG concept diagrams (editable in any text editor).
- **Certificates:** add the PDF to `assets/certs/...` and add an entry to `CERTS`. Dates are copied from the certificates.
- **Events:** edit the `EVENTS` list. No dates were provided, so none are shown.
- **Resume:** replace `assets/resume.pdf` with a new file of the same name.

## Notes
- The AWS certificates are completion certificates for *official practice exams*, and the site labels them that way.
- The contact form uses a `mailto:` link, so it opens the visitor's email app. Nothing is sent from the site itself.
