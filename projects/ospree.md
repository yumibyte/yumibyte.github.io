---
layout: project
slug: ospree
title: Ocean profilers (Stanford S4 Lab)
permalink: /projects/ospree/
---

At the Stanford Smart Sensing Systems (S4) Lab (January 2026 onward), I work on embedded firmware for our ocean profilers, improving how sensing stacks run in the field. The project is focused on making a light weight, low-cost solution for measuring conductivity, temperature, and depth (CTD). The profiler drops to about 1 km deep, sampling conductivity, temperature, and salinity on the way.

I built a demo system that highlights sensor capability over low-power LoRa so we can show what the platform does without a full deployment. This demo won the Best Demo Award at ACM MobiSys 2026 (yahoo!), a leading conference in mobile and wireless systems.

The demo works like this:

1. We slowly pump salt water via a peristaltic pump to the bottom of the tank
2. We heat the top up with a "lizard lamp"
3. We reel the profiler slowly through the water column, taking measurements as we go
4. The profiler streams the data to my laptop over LoRa

So we've essentially created a fake ocean in this tube to demonstrate that we observe changes in pressure/temperature/salinity from our sensor. This is because the bottom of the tank will be saltier and the top will be warmer (as expected in the ocean).

For this I set up:

- Talking over LoRa from the profiler in the tank to my laptop
- Drivers to interface with the motors, the peristaltic pump, and the buttons
- A dashboard to display live data received

Some fun things that I realized in this process:
- Lots of small things about wiring up protoboards cleanly
- Learned that some motor drivers (e.g. A4988) are incredibly loud compared to others!! Using a TMC2226 makes the motors practically silent in our demo which is a huge win since they have modes such as StealthChop. I realize this is how things like 3D printers are much more silent and makes me wish I can go back to my "zen sand plotter" project on my page which wasn't so "zen" because the steppers were incredibly loud. This doesn't even require changing the actual motor we're using
- It's fun to make essentially a large fishtank

<div class="project-inline-video">
  <video autoplay muted loop playsinline controls>
    <source src="{{ '/images/ospree-demo.mp4' | relative_url }}" type="video/mp4" />
  </video>
</div>

## What I'm working on now

These days I write the embedded firmware and design the PCB for our radio module. We're also experimenting with designing our own low-cost pressure sensors.

Besides this, I've been helping with writing the firmware for our new pressure testing board. Here's an example of us pressure testing the entire profiler since we'll need to drop to ~1000 meters in the ocean.

<figure class="project-body-figure">
  <img src="{{ '/images/ospree-pressure-test.jpg' | relative_url }}" alt="OSPREE Rev2 units in a shallow water pressure test" loading="lazy" />
  <figcaption>OSPREE profilers under test.</figcaption>
</figure>
