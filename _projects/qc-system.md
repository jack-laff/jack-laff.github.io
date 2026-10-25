---
title: Automated quality control system
context: Adia Thermal
period: 2025 – 2026
order: 2
summary: Wrote and optimised the end-of-line QC software used on every smart device, and designed custom PCBs to remove tedious production steps.
result: 4,000+ units tested, failure rate cut from 11% to under 1%.
cover: /assets/img/qc-system/cover.png
cover_alt: QC results dashboard (data blurred)
gallery:
  - src: /assets/img/qc-system/pcb-layout.png
    alt: Production PCB layout in KiCad
    caption: Custom production PCB in KiCad.
  - src: /assets/img/qc-system/pcb-photo.jpg
    alt: Assembled production PCB
    caption: Made by PCBWay.
metrics:
  - value: "4,000+"
    label: units tested
  - value: "11% → <1%"
    label: failure rate
tools: [Python, Raspberry Pi, PIC18, Web dashboard, KiCad, PCBWay]
---

## The problem

Adia's smart devices needed a consistent way to be inspected, calibrated and tested before shipping, with results
that could be tracked and analysed.

## How it works

Each device has a PIC18 microcontroller that talks to a Raspberry Pi running the QC script. The script:

1. Guides the operator through a manual inspection.
2. Calibrates the device.
3. Checks the measurements against pass criteria.
4. Logs the results to a database and web dashboard for analysis.

I wrote and optimised the script and pass criteria with the software team, tuning the process over many runs for
speed and reliability.

## How the failure rate fell

The QC data pointed to two root causes: a **firmware fault** and a **motor defect** that wasn't being caught.
Fixing both took the failure rate from **11% to under 1%**.

## Custom PCBs for production

I also designed custom PCBs in KiCad, made by PCBWay, to remove or simplify tedious manual production steps.
For example, a flexible PCB replaced a complicated hand-soldered wire assembly inside one of the devices with a
single simple part.

<div class="gallery">
  <figure>
    <img src="{{ '/assets/img/qc-system/flex-before.jpg' | relative_url }}" alt="Device with a hand-soldered wire assembly">
    <figcaption>Before: hand-soldered wire assembly.</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/img/qc-system/flex-after.jpg' | relative_url }}" alt="Same device with a flexible PCB in place of the wiring">
    <figcaption>After: one flexible PCB. Main board obscured.</figcaption>
  </figure>
</div>

## Result

- Used on **4,000+ units**, and still in use.
- Failure rate cut from **11% to under 1%**.
