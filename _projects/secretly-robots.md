---
title: A humanoid that fetches on request
context: UCL Agentverse 2026 hackathon, robotics track
period: November 2026
order: 2
summary: In a two-day hackathon, our team of five built voice-commanded fetching software for a Unitree G1 humanoid in MuJoCo. An older person on the sofa asks for a drink, and the robot finds it, opens drawers, works round a locked door and brings it to their tray, with everything running on the robot.
result: Top 3 of 25+ teams. A simulated humanoid that hears a request, finds the item and brings it, fully offline.
cover: /assets/img/secretly-robots/cover.jpg
cover_alt: Simulated Unitree G1 humanoid delivering a water bottle to a seated person's tray in a MuJoCo house
metrics:
  - value: "Top 3"
    label: of 25+ teams, robotics track
  - value: "25"
    label: test scenarios, all run through with the G1
  - value: "~0.3 s"
    label: speech-to-text on the robot's CPU
  - value: "Offline"
    label: hearing, dialogue and planning all run locally
tools: [MuJoCo, Unitree G1, NVIDIA GR00T, Python, Whisper, Gemma 4 (Ollama), Gemini TTS, OpenCV ArUco, pytest]
---

## The problem

For an older person living alone with limited mobility, a drink two rooms away means waiting for a carer or risking a
fall. One in three people over 65 falls each year, and England has around 96,000 care vacancies on any given day.
Older adults also say they want robots for fetching, not personal care. We built the software for that: a robot a carer
teaches once, which then fetches things on request.

<figure>
  <video src="{{ '/assets/img/secretly-robots/demo.mp4' | relative_url }}" poster="{{ '/assets/img/secretly-robots/poster.jpg' | relative_url }}" controls playsinline preload="metadata"></video>
  <figcaption>Submission video: the person asks, the G1 finds the door locked, reroutes, fetches the bottle and delivers it. Then the carer teaches the drawer once.</figcaption>
</figure>

## What we built

A care layer that plugs into a robot through one interface: hear, understand, plan, navigate, open, find, grasp,
deliver. We ran it on a Unitree G1 in MuJoCo, balanced and walked by NVIDIA's GR00T policies.

- **Asks before acting on hints.** "Bring me water" starts a fetch. "I'm parched" gets *"Would you like some water?"*
  first. Yes fetches; no, or 10 s of silence, cancels. It refuses medication.
- **Searches like a person would.** Each item has a probability for every place it might be. The robot checks the
  likeliest first and rules places out as it goes.
- **Adapts, and says when it's stuck.** A moved bottle or a shut door means a new plan. It asks for help after two
  failures and never reports a delivery it hasn't confirmed.
- **Private by design.** Hearing, dialogue and planning all run on the robot with the Wi-Fi off. Gemini can plan when
  online, but a rule-based guard approves every action either way.

## My part

There were five of us: four mechanical engineers and a computer scientist. I built two pieces end
to end.

**The house.** On day one I built the MuJoCo world everyone else worked in: a randomised 8 × 6 m four-room flat with
push doors (some locked), chests of drawers, ArUco markers, room and head cameras, and a pytest suite checking every
layout. I also wrote the path planner on its occupancy grid (BFS with line-of-sight shortening and squared-up doorway
crossings), which the G1 navigation was built on.

**The voice pipeline and demo.** On day two I built everything between the person speaking and the robot moving:

- **Hearing.** The G1's head camera acts as a microphone, with volume falling off with distance, room noise and voice
  activity detection. It also works through the laptop mic.
- **Speech to text.** Whisper base.en on the CPU, about 0.3 s per phrase, with a live window showing each transcript,
  its timing and the command it produced.
- **Understanding.** Rules first, which are instant, then a local Gemma 4 model for phrasing the rules don't know (0.2–0.45 s).
  Every model answer is schema-checked, so the robot never acts on free text.
- **Dialogue.** A command state machine (confirming, understood, declined) with the robot's own voice lines.
- **The demo.** I tied it all to the G1 in fetch mode with 25 fixed scenarios (5 item placements × 5 floor setups,
  from tidy to locked door plus clutter), adaptive search and locked-door discovery. The robot doesn't know which door is
  locked. It finds out when it gets there, says *"That door's locked, I'll go round"* and replans.

<div class="gallery row">
  <figure style="flex: 1.778">
    <img src="{{ '/assets/img/secretly-robots/locked-door.jpg' | relative_url }}" alt="G1 at a locked door marked with a red bar, with its LiDAR map and planned route beside it">
    <figcaption>Locked door found and marked (red bar). The route reroutes through the bedroom and study.</figcaption>
  </figure>
  <figure style="flex: 1.778">
    <img src="{{ '/assets/img/secretly-robots/teach-once.jpg' | relative_url }}" alt="Room camera tracking ArUco markers on a chest of drawers as the carer opens a drawer">
    <figcaption>Teach once: the carer opens a drawer while a room camera tracks the markers.</figcaption>
  </figure>
</div>

## Result

- **Top 3 of over 25 teams** in the robotics track.
- A full fetch on video, unscripted: request, locked door, reroute, grasp, delivery to the tray.
- **One demonstration teaches a drawer or door.** The motion is fitted as a hinge or a slide (4.3 mm fit error), not
  replayed.
- **Collision-checked arm.** Contacts over 1 cm dropped from 21.6% of moves to none.

<div class="gallery row">
  <figure style="flex: 1.5">
    <img src="{{ '/assets/img/secretly-robots/presenting.jpg' | relative_url }}" alt="Jack presenting the robot's live map to the judges">
    <figcaption>Presenting the live demo to the judges.</figcaption>
  </figure>
  <figure style="flex: 0.668">
    <img src="{{ '/assets/img/secretly-robots/at-the-event.jpg' | relative_url }}" alt="Jack seated at a laptop during the hackathon">
    <figcaption>At the event.</figcaption>
  </figure>
</div>

## Limits

Simulation only. ArUco markers stand in for a learned object detector, and it fetches light items only (a bottle or
a cup). It is a prototype, not a medical device.

## What I learned

<!-- DRAFT: rewrite in your own words. -->
With five people and two days, the most useful thing I built first was the shared world: once the house existed, everyone
could work against it in parallel. Keeping the language model behind rules and a guard made the demo dependable. Gemma
handled the odd phrasing, but the robot never acted on anything that hadn't been checked.

[Code on GitHub](https://github.com/kwerui/secretly-robots)
