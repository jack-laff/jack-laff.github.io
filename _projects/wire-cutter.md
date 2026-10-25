---
title: From wire cutter to flexible PCB
context: Adia Thermal production
period: 2026
order: 3
summary: A low-volume production step needed lots of wires cut by hand. I automated it with a wire cutter, then designed it out entirely with a flexible PCB.
result: Cut a 3-hour wiring task to 30 minutes, then eliminated it with a flexible PCB.
cover: /assets/img/wire-cutter/cover.jpg
cover_alt: 3D printed wire cutter with two stepper motors and a lead screw
metrics:
  - value: "3 h → 30 min"
    label: wire preparation, with the wire cutter
  - value: "Eliminated"
    label: wire cutting, with the flexible PCB
tools: [Raspberry Pi Pico, Stepper motors, Fusion 360, 3D printing, KiCad, Flexible PCB]
---

## The problem

A low-volume production step needed lots of wires cut, stripped and hand-soldered. Cutting them was a recurring
3-hour job: slow, tedious and error-prone, with cut lengths that varied.

## First fix: a wire cutter

I built a desktop machine to automate the cutting and stripping.

- A **Raspberry Pi Pico** drives **two stepper motors**: one feeds the wire, the other operates the cutting and
  stripping mechanism.
- A custom **3D printed body** with mechanical subassemblies for feeding and cutting.

<figure>
  <video src="{{ '/assets/img/wire-cutter/demo.mp4' | relative_url }}" controls muted playsinline loop preload="metadata"></video>
  <figcaption>Early test footage, before the final tuning.</figcaption>
</figure>

It cut the job from **3 hours to 30 minutes** of setup and post-processing, with more accurate, repeatable cuts.

## Better fix: design the wires out

The wire cutter made the step faster, but the wiring was still there. I realised I could remove it altogether, so I
designed a **flexible PCB** in KiCad that replaces the hand-cut wires and is made cheaply in China.

- **No wire cutting** at all.
- **Faster, easier soldering.**
- **A more repeatable assembly.**

<div class="gallery">
  <figure>
    <img src="{{ '/assets/img/production-pcbs/flex-before.jpg' | relative_url }}" alt="Device with a hand-soldered wire assembly">
    <figcaption>Before: hand-cut, hand-soldered wiring.</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/img/production-pcbs/flex-after.jpg' | relative_url }}" alt="Same device with a flexible PCB in place of the wiring">
    <figcaption>After: one flexible PCB. Main board obscured.</figcaption>
  </figure>
</div>
