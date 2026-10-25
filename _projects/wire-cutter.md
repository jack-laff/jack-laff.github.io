---
title: Automatic wire cutter and stripper
context: Personal project
period: 2026
order: 3
summary: A desktop machine that cuts and strips wire for low-volume production, built to automate a slow, repetitive task.
result: Cut a recurring 3-hour task to 30 minutes, with more accurate cuts.
cover: /assets/img/wire-cutter/cover.jpg
cover_alt: Automatic wire cutter and stripper
video: /assets/img/wire-cutter/demo.mp4
gallery:
  - src: /assets/img/wire-cutter/cad.png
    alt: CAD of the feed and cut mechanisms
    caption: Feed and cut mechanisms in Fusion 360.
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

- A **Raspberry Pi Pico** drives **two stepper motors**: one feeds the wire, the other operates the cutting and
  stripping mechanism.
- A custom **3D printed body** with mechanical subassemblies for feeding and cutting.

## Result

- A recurring **3-hour task reduced to 30 minutes** of setup and post-processing.
- More accurate, repeatable cut lengths than cutting by hand.
