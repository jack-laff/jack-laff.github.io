---
# NEEDS FOUNDER APPROVAL before you publish (failure rates, screenshots).
title: Automated quality control system
context: Adia Thermal
period: 2025 – 2026
order: 2
summary: Wrote the end-of-line QC software used on every smart device, and designed custom PCBs to remove tedious production steps.
result: 4,000+ units tested, failure rate cut from 11% to under 1%.
cover: /assets/img/placeholders/qc-system.svg
cover_alt: QC dashboard
metrics:
  - value: "4,000+"
    label: units tested
  - value: "11% → <1%"
    label: failure rate
tools: [Python, Raspberry Pi, PIC18, Database and web dashboard, KiCad, PCBWay]
---

## The problem

Adia's smart devices needed a consistent way to be inspected, calibrated and tested before shipping, with results that
could be tracked and analysed.

## How it works

Each device has a PIC18 microcontroller that communicates with a Raspberry Pi running my script. The script:

1. Guides the operator through a manual inspection.
2. Runs a calibration on the device.
3. Checks the measurements automatically against pass criteria I defined.
4. Sends the results through the backend to a database, where they can be viewed and analysed on a web dashboard.

I wrote all of the code, set the pass criteria and tuned the process over many runs to optimise for time and reliability.

<!-- Add one or two sentences on HOW the failure rate fell, e.g. which root causes the data revealed
     and what was changed in production or design as a result. Interviewers will ask about this. -->

## Custom PCBs for production

I also designed custom PCBs in KiCad, manufactured by PCBWay, to eliminate or simplify tedious manual production tasks.

<!-- IMAGES TO ADD (save in assets/img/qc-system/ and uncomment). Blur any customer or production data.
<img src="{{ '/assets/img/qc-system/dashboard.png' | relative_url }}" alt="QC dashboard">
*QC results dashboard (data blurred).*
<div class="gallery">
  <img src="{{ '/assets/img/qc-system/pcb-layout.png' | relative_url }}" alt="PCB layout in KiCad">
  <img src="{{ '/assets/img/qc-system/pcb-photo.jpg' | relative_url }}" alt="Assembled PCB">
</div>
-->

## Result

- Used on **4,000+ units** and still in use.
- Failure rate reduced from **11% to under 1%**.

## What I learned

<!-- Write 2–3 sentences in your own words. -->
