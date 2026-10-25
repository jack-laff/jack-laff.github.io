---
title: Automatic wire cutter and stripper
context: Personal project
period: 2026
order: 4
summary: A desktop machine that cuts and strips wire for low-volume production, built to automate a slow, repetitive task.
result: Cut a recurring 3-hour task to 30 minutes, with more accurate cuts.
cover: /assets/img/wire-cutter/cover.jpg
cover_alt: 3D printed wire cutter with two stepper motors and a lead screw
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

<figure>
  <video src="{{ '/assets/img/wire-cutter/demo.mp4' | relative_url }}" controls muted playsinline loop preload="metadata"></video>
  <figcaption>Early test footage, before the final tuning.</figcaption>
</figure>

## Result

- A recurring **3-hour task reduced to 30 minutes** of setup and post-processing.
- More accurate, repeatable cut lengths than cutting by hand.
