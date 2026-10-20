---
# HOW TO ADD A PROJECT
# 1. Copy this file into the _projects folder and rename it, e.g. _projects/my-new-project.md
#    (lowercase, hyphens, no spaces; this becomes the page address).
# 2. Fill in the fields below. Delete any line you don't need (status, metrics, tools are optional).
# 3. Put images in assets/img/my-new-project/ and point "cover" at the main one.
# 4. Save, commit and push. The site updates in a minute or two.

title: Project name
context: Where it happened, e.g. Personal project / Imperial College London / Company name
period: 2026
order: 10                 # position on the home page (1 = first)
status: In progress       # delete this line once the project is finished
summary: One sentence describing what it is. Shown under the title on the project page.
result: One line with the key result. Shown on the home page card.
cover: /assets/img/placeholders/workshop-builds.svg   # change to e.g. /assets/img/my-new-project/cover.jpg
cover_alt: Short description of the cover image
metrics:                  # optional: big numbers shown at the top of the page
  - value: "−40%"
    label: what the number means
tools: [Tool one, Tool two, Tool three]
---

## The problem

What needed solving and why it mattered.

## My role

What you personally owned, and who else was involved.

## What I did

- Key step or decision.
- Key step or decision.

<!-- Add images like this (the file must be in the assets/img folder):
<img src="{{ '/assets/img/my-new-project/photo.jpg' | relative_url }}" alt="Description">
*Optional caption in italics.*

Several images side by side:
<div class="gallery">
  <img src="{{ '/assets/img/my-new-project/one.jpg' | relative_url }}" alt="Description">
  <img src="{{ '/assets/img/my-new-project/two.jpg' | relative_url }}" alt="Description">
</div>

A short video (under ~25 MB):
<video src="{{ '/assets/img/my-new-project/demo.mp4' | relative_url }}" controls muted playsinline></video>

A YouTube video (upload as "Unlisted"):
<iframe src="https://www.youtube.com/embed/VIDEO_ID" allowfullscreen></iframe>
-->

## Result

- Measurable outcome, with numbers where possible.

## What I learned

Two or three sentences in your own words.
