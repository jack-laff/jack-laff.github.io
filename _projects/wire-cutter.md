---
title: Automatic wire cutter and stripper
context: Personal project
period: 2026
order: 3
summary: A desktop machine that cuts and strips wire for low-volume production, built to automate a slow, repetitive task.
result: Cut a recurring 3-hour task to 30 minutes, with more accurate cuts.
cover: /assets/img/placeholders/wire-cutter.svg
cover_alt: Automatic wire cutter and stripper
metrics:
  - value: "3 h → 30 min"
    label: recurring task time
  - value: "2"
    label: stepper motors, Pico-controlled
tools: [Raspberry Pi Pico, Stepper motors, Fusion 360, 3D printing]
---

## The problem

Cutting and stripping wires by hand for low-volume production was a recurring 3-hour job, and the cut lengths varied.

## What I built

- A **Raspberry Pi Pico** drives **two stepper motors**: one feeds the wire, the other operates the cutting and stripping mechanism.
- A custom **3D printed body** with mechanical subassemblies for feeding and cutting.

<!-- VIDEO TO ADD: the single most valuable thing on this page.
Option A, small file (under ~25 MB): save as assets/img/wire-cutter/demo.mp4 and uncomment:
<video src="{{ '/assets/img/wire-cutter/demo.mp4' | relative_url }}" controls muted playsinline></video>
Option B, larger file: upload to YouTube as "Unlisted", then paste the embed link:
<iframe src="https://www.youtube.com/embed/VIDEO_ID" allowfullscreen></iframe>
-->

<!-- IMAGES TO ADD (save in assets/img/wire-cutter/):
<div class="gallery">
  <img src="{{ '/assets/img/wire-cutter/cad.png' | relative_url }}" alt="CAD of feed and cut mechanisms">
  <img src="{{ '/assets/img/wire-cutter/build.jpg' | relative_url }}" alt="Finished machine">
</div>
-->

## Result

- Reduced a recurring **3-hour task to 30 minutes** of setup and post-processing.
- More accurate, repeatable cut lengths than cutting by hand.

## What I learned

<!-- Write 2–3 sentences in your own words. -->
