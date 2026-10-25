---
title: Adia Hub redesign
context: Adia Thermal
period: 2025 – 2026
order: 1
summary: Took a loss-making heat pump control product to a profitable, production-ready design as the company's sole hardware engineer.
result: Unit cost cut by 36%, from loss-making to profitable, with assembly time halved.
cover: /assets/img/adia-hub-redesign/cover.jpg
cover_alt: Render of the pilot Adia Hub (left) next to the redesign (right)
metrics:
  - value: "−36%"
    label: unit cost, loss-making to profitable
  - value: "−50%"
    label: assembly time
  - value: "−73%"
    label: unit cost of a further concept design
tools: [Fusion 360, 3D printing, DFM/DFA, Component testing, Supplier management]
---

## The problem

The Adia Hub is Adia Thermal's core product: a pipework assembly with a pump, sensors and a Raspberry Pi/PCBA
controller that talks to smart radiator valves and temperature sensors. The pilot version lost money on every unit,
was hard to assemble at scale, relied on a weak supply chain and was complicated to install.

<figure>
  <img src="{{ '/assets/img/adia-hub-redesign/internals.jpg' | relative_url }}" alt="Covers-off render of the pilot Hub's pipework next to the simpler redesign">
  <figcaption>Covers off: the pilot (left) and the redesign (right).</figcaption>
</figure>

## What I did

As the only hardware engineer in a 10-person team, I led the redesign end to end and reported directly to the founders.

- **Redesigned the product in Fusion 360**, validating each iteration with 3D printed prototypes.
- **Removed parts** that testing showed were unnecessary, and reselected the body materials and internal components.
- **Optimised the form factor** for faster assembly and simpler installation.
- **Ran a component testing programme:** specifications, supplier samples, acceptance criteria, test rigs, control code,
  data analysis and recommendations to the founders.
- **Built the supply chain** across China, India, Poland and the UK, from RFQs and design packages to production
  deadlines, including a visit to the pump supplier in China.

<div class="gallery row">
  <figure style="flex: 0.567">
    <img src="{{ '/assets/img/adia-hub-redesign/prototype.jpg' | relative_url }}" alt="3D printed Hub prototype mounted on a board">
    <figcaption>3D printed prototype.</figcaption>
  </figure>
  <figure style="flex: 1.238">
    <img src="{{ '/assets/img/adia-hub-redesign/covers.jpg' | relative_url }}" alt="Thermoformed production cover next to a two-part 3D printed cover">
    <figcaption>Thermoformed production cover (left) and the 3D printed prototype cover (right).</figcaption>
  </figure>
</div>

## Result

- Unit cost cut by **36%**, turning the product profitable, and **assembly time halved**.
- Production tooling complete.
- A further concept design cuts unit cost by **73%** against the original.
