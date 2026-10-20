# Jack Lafferty: portfolio site

A simple portfolio built with Jekyll and hosted free on GitHub Pages. Each project is one Markdown file in `_projects/`;
GitHub turns them into web pages automatically. No installs are needed on your Mac.

## Before you publish

- [ ] **Founder approval for Adia content.** `adia-hub-redesign.md`, `qc-system.md` and the home page (figures and the
      "loss-making to profitable" line) all use Adia information. Remove or soften anything the founders say no to.
- [ ] Replace the placeholder images with real photos or renders (at least the Adia Hub, QC and wire cutter).
- [ ] Fill in the "What I learned" sections (search for `<!--` to find every gap).
- [ ] Add your GitHub link and CV in `_config.yml`.
- [ ] Use a CV version **without your phone number** for the public download.

## Publish it (first time, about 15 minutes)

1. Create a free account at [github.com](https://github.com). Pick a professional username, e.g. `jack-lafferty`.
2. Click **New repository** and name it exactly **`<your-username>.github.io`** (e.g. `jack-lafferty.github.io`).
   Make it **Public**.
3. On the empty repository page, click **uploading an existing file**. Drag in **everything inside this
   `portfolio` folder** (not the folder itself), including the `_layouts`, `_projects` and `assets` folders.
   Then click **Commit changes**.
4. Go to **Settings → Pages**. Under "Build and deployment", set **Source** to **Deploy from a branch**,
   branch **main**, folder **/ (root)**, then **Save**.
5. After 1–2 minutes the site is live at **`https://<your-username>.github.io`**. Put this link in your CV header and on LinkedIn.

If you'd rather use git from the terminal or GitHub Desktop, that works the same way. Push to `main` and the site rebuilds.

## Add or update a project

1. Copy `PROJECT_TEMPLATE.md` into `_projects/` and rename it, e.g. `_projects/pick-and-place-arm.md`.
2. Fill in the fields at the top and the sections below them.
3. Put images in `assets/img/<project-name>/` and set `cover:` to the main image.
4. Upload or push the changes. The site updates in a minute or two.

Quick edits can be made directly on github.com: open a file, click the pencil icon, edit, then **Commit changes**.

## Images and video

- Use **JPG** for photos and **PNG** for screenshots/CAD. Resize to about **1600 px wide** to keep pages fast.
- Card images are cropped to 16:10, so landscape photos work best for covers.
- Videos: files under ~25 MB can go in the repo as `.mp4`. Upload anything larger to YouTube as **Unlisted** and embed it
  (see `PROJECT_TEMPLATE.md`).
- **Adia images:** blur customer data, supplier names and anything the founders flag.

## Files

| Path | What it is |
|---|---|
| `_config.yml` | Name, tagline, email, LinkedIn, GitHub, CV link |
| `index.html` | Home page: intro, headline numbers, project grid, about and skills |
| `_projects/*.md` | One file per project |
| `PROJECT_TEMPLATE.md` | Copy this to start a new project |
| `assets/css/style.css` | Styling. Change `--accent` at the top to change the colour |
| `assets/img/` | Images, one folder per project |
| `files/` | Put your CV PDF here |
| `_layouts/` | Page templates (no need to edit) |

## Custom domain (optional)

Buy a domain (e.g. `jacklafferty.com`), then add it under **Settings → Pages → Custom domain** and follow GitHub's DNS
instructions.
