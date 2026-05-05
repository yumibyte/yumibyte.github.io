---
layout: project
slug: smesh
title: SMesh — wildfire mesh sensing (Stanford Radio Club)
permalink: /projects/smesh/
---

As SMesh team lead for Stanford Radio Club (Spring 2025 onward), I help deploy and validate low-cost, off-grid mesh networks for wildfire sensing using LoRa. We have tested our sensors at a handful of local controlled burns.

This has been pretty awesome to work on because sensors that are used commercially mainly:

1. Drain a bunch of power (think: they are plugged into wall outlets)
2. Use WiFi (and don't work otherwise)
3. Are super expensive

So we're essentially trying to tackle all three of these problems to make a smoke sensor that burn bosses can carry out to the field and easily deploy (without needing special installment, like most smoke sensors).

On the firmware side I built embedded drivers for real-time clock (RTC) logging, LoRa radio, and wind sensors (anemometer and vane) so nodes stay time-synchronized and stay reliable on constrained power budgets.

<div class="project-inline-video project-inline-video--smesh">
  <video autoplay muted loop playsinline controls>
    <source src="{{ '/images/wind-sensor.mp4' | relative_url }}" type="video/mp4" />
  </video>
</div>

I also contribute towards the electrical for the project and have helped with the wiring/so forth for our wind sensors. Above is a fully assembled wind sensor that I personally built. Excuse the wires we are actively making our first PCB based on this design ;) The idea is to get these sensors in the hands of researchers/burn bosses.

We have deployed at multiple controlled burn sites so far and I'm looking forward to more :-)
