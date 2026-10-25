---
title: Automated quality control system
context: Adia Thermal
period: 2025 – 2026
order: 2
summary: Wrote and optimised the end-of-line QC software used to inspect, calibrate and test every smart device.
result: 4,000+ units tested, failure rate cut from 11% to under 1%.
cover: /assets/img/qc-system/cover.png
cover_alt: QC results dashboard (data blurred)
metrics:
  - value: "4,000+"
    label: units tested
  - value: "11% → <1%"
    label: failure rate
tools: [Python, Raspberry Pi, PIC18, Web dashboard]
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

The dashboard pictured above shows all-time totals across every production run, including the early runs before
the fixes below (device data blurred).

## How the failure rate fell

The QC data pointed to two root causes: a **firmware fault** and a **motor defect** that wasn't being caught.
Fixing both took the failure rate from **11% to under 1%**.

## Result

- Used on **4,000+ units**, and still in use.
- Failure rate cut from **11% to under 1%**.
