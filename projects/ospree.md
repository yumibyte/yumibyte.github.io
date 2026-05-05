---
layout: project
slug: ospree
title: Ocean profilers (Stanford S4 Lab)
permalink: /projects/ospree/
---

At the Stanford Smart Sensing Systems (S4) Lab (Winter 2026 onward), I work on embedded firmware for our ocean profilers, improving how sensing stacks run in the field. The project is focused on making a light weight, low-cost solution for measuring conductivity, temperature, and depth (CTD).

I built a demo system that highlights sensor capability over low-power LoRa so we can show what the platform does without a full deployment. This demo was accepted to ACM MobiSys 2026 (yahoo!), a leading conference in mobile and wireless systems.

The demo works as so: 
1) We slowly pump salt water via a peristaltic pump to the bottom of the tank
2) We heat the top up with a "lizard lamp."
So we've essentially created a fake ocean in this tube to demonstrate that we observe changes in pressure/temperature/salinity from our sensor.

Some fun things that I realized in this process:
- Lots of small things about wiring up protoboards cleanly
- Learned that some motor drivers (e.g. A4988T) are incredibly loud compared to others!! Using a LTC2226 makes the motors practically silent in our demo which is a huge win since they have modes such as StealthChop. I realize this is how things like 3D printers are much more silent and makes me wish I can go back to my "zen sand plotter" project on my page which wasn't so "zen" because the steppers were incredibly loud. This doesn't even require changing the actual motor we're using.
- It's fun to make essentially a large fishtank

<div class="project-inline-video">
  <video autoplay muted loop playsinline controls>
    <source src="{{ '/images/ospree-demo.mp4' | relative_url }}" type="video/mp4" />
  </video>
</div>

Besides this, I've been helping with writing the firmware for our new pressure testing board. Here's an example of us pressure testing the entire profiler since we'll need to drop to ~1000 meters in the ocean.

<figure class="project-body-figure">
  <img src="{{ '/images/ospree-pressure-test.jpg' | relative_url }}" alt="OSPREE Rev2 units in a shallow water pressure test" loading="lazy" />
  <figcaption>OSPREE Rev2 boards under test.</figcaption>
</figure>
