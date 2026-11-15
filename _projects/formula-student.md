---
title: Formula Student rear suspension
context: Imperial Formula Racing, Imperial College London
period: 2024 – 2025
order: 4
summary: Project manager and suspension designer for a new rear double wishbone suspension on Imperial's first combustion-engined Formula Student car, taken from geometry and CAD through outsourced CNC manufacture to instrumented testing.
result: CNC bolt-on mounts improved positional accuracy by 4.4%, with three camber presets, delivered £93 under budget.
cover: /assets/img/formula-student/assembly.jpg
cover_alt: Rear suspension assembly mounted on the new rear spaceframe, with components labelled
metrics:
  - value: "+12%"
    label: load path linearity
  - value: "+4.4%"
    label: positional accuracy vs CAD
  - value: "−10.1%"
    label: net mass (suspension + narrower chassis)
  - value: "£1,407"
    label: total cost, on a £1,500 budget
tools: [SolidWorks, ANSYS FEA, DFM for CNC, Outsourced manufacture, Test rig design, Strain gauges + Arduino DAQ, Project management]
---

## The problem

After more than a decade of electric cars, Imperial Formula Racing switched to a Kawasaki Ninja 400 combustion engine.
That meant a new rear spaceframe, drivetrain and rear suspension, all designed together. The old rear suspension had
two main weaknesses: its welded mounts drifted out of alignment during welding, giving bent, non-linear load paths, and
it left no room for the driveshaft boot required by the rules.

## My role

I was **project manager and suspension designer** in a four-person team, one of four subgroups (spaceframe, suspension,
drivetrain, rear wing) working on the rear half of the car. I ran the schedule and budget and coordinated hardpoints and
interfaces with the spaceframe and drivetrain teams.

## What I did

- **Set new geometry.** We designed symmetrical double wishbones that could be simulated reliably in 2D. Track width
  went from 1,200 to 1,150 mm to help the car clear cones, and the wishbones were made as long as the track width
  allowed. The pushrod and toe rod were placed to leave room for a standard driveshaft boot.
- **Replaced welded tabs with bolt-on CNC mounts.** The mounts are 16MnCr5 alloy steel with **three camber presets
  built in** (wet tyres, nominal slicks, extreme negative), plus shims for fine tuning. The final mounting holes are
  drilled at assembly, which adds a last alignment check.
- **Designed for the process.** Once I understood CNC better, I removed the webs between the tabs and used larger fillets
  instead. This kept the stiffness and cut machining cost.
- **Redesigned the lower wishbone apex** as a CNC-milled mild steel part, welded to the rods. It fits inside the existing
  upright, carries the pushrod and keeps the load path straight.
- **Brought sourcing costs down.** Geomiq quoted CNC at about half the price of the first quotes, so we outsourced every
  mount, not just the lower ones. We also found PTFE-lined rod ends for a fifth of the original quote. The money saved
  went on testing and on servicing the dampers.
- **Built our own test rig** when the spaceframe arrived late, so testing could go ahead without it.

<div class="gallery row">
  <figure style="flex: 1.409">
    <img src="{{ '/assets/img/formula-student/cad-render.jpg' | relative_url }}" alt="CAD render of the rear suspension on the spaceframe">
    <figcaption>Full assembly in CAD.</figcaption>
  </figure>
  <figure style="flex: 1.714">
    <img src="{{ '/assets/img/formula-student/apex-cad.jpg' | relative_url }}" alt="CAD of the CNC-milled lower wishbone apex">
    <figcaption>CNC-milled lower wishbone apex, which carries the pushrod mount.</figcaption>
  </figure>
</div>

## Testing

**Load test.** I instrumented all six rods with strain gauges, read through HX711 amplifiers and an Arduino. We loaded the
upright in 100 N steps over a pulley and compared the measured rod forces with our design load model.

- Rods in tension followed the model linearly, with the toe rod within **7.7%** of the predicted value.
- Compression channels read near zero. We traced this to the signal leaving the Arduino's 0–5 V input range, not to
  the structure.
- Suspension compliance stayed **under 2 mm/kN**. Most of it came from oversized water-jet holes in the rocker, so we
  recommended remaking the rocker with drilled holes.

**Geometry test.** We measured camber against 100 mm of wheel travel with a digital protractor and a laser level.

- Camber gain was linear for all three presets: **0.052, 0.074 and 0.086 °/mm**, with no more than 2.1% uncertainty.
  Two presets fall within the range recommended in the literature.
- The gap between presets was smaller than CAD predicted. This showed the limits of 2D kinematics, so we recommended 3D
  simulation and a 3D-printed jig to set the neutral position.

<div class="gallery row">
  <figure style="flex: 0.75">
    <img src="{{ '/assets/img/formula-student/load-test-rig.jpg' | relative_url }}" alt="Suspension on the test rig with rope and pulley loading and strain gauge wiring">
    <figcaption>Load test, with a strain gauge on each rod.</figcaption>
  </figure>
  <figure style="flex: 0.75">
    <img src="{{ '/assets/img/formula-student/lower-wishbone-jig.jpg' | relative_url }}" alt="Welded lower wishbone with CNC apex in its jig">
    <figcaption>Lower wishbone with the CNC apex, in its welding jig.</figcaption>
  </figure>
</div>

## Result

- A working rear-left suspension that **fits the new spaceframe and drivetrain** and meets its design specification
  for camber gain, strength and mass (3.18 kg, inside the 2–5 kg target).
- CNC mounts gave **12% better load path linearity** and **4.4% better positional accuracy** against CAD.
- The suspension itself is 30.9% heavier, but the longer wishbones allow a narrower chassis, for a **net mass
  reduction of 10.1%**.
- Delivered for **£1,407 on a £1,500 budget**, despite losing workshop welding access partway through the project.

## What I learned

<!-- DRAFT from the report's conclusions: rewrite in your own words. -->
Designing for the manufacturing process early saves both money and accuracy. Talking to the CNC supplier changed our
mounts more than any analysis did. Testing showed that our safety factors were too cautious, and that a test is only as
good as its data acquisition: next time I'd check the amplifier circuit on a scope before we glued a single gauge.
