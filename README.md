# Jack Lafferty: portfolio site (lean)

Jekyll site on GitHub Pages, live at https://jack-laff.github.io. Push or upload to `main` and it rebuilds in 1–2 minutes.
Kept out of search engines (`noindex`); it's shared via the CV link only.

| Path | What it is |
|---|---|
| `_config.yml` | Name, tagline, email, LinkedIn, GitHub, CV link |
| `index.html` | Home: intro, headline numbers, projects, "Now building", about and skills |
| `_projects/*.md` | One file per project page |
| `assets/img/<project>/` | Images: drop in a file with the name listed in the project's front matter and it appears |
| `files/` | CV PDF (no phone number) |

## Adding a project page later

Copy an existing file in `_projects/`, rename it, edit the front matter and text, then add its images to
`assets/img/<new-name>/`. Move the matching line out of "Now building" in `index.html`.

## Adia rules

Relative figures only (no £ amounts), approved images only, never the main PCBA, not linked publicly on LinkedIn.
