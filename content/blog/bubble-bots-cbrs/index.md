---
title: Bubble Bots, Cavitation, and a Great Collaboration
summary: Acoustic characterization of chemotactic microbubble robots, their cavitation behavior, and a simple Keller-Miksis model.
date: 2026-02-02

image:
  caption: 'Time evolution of cavitation signals for PBS, CBRs and commercial microbubbles under insonation'

authors:
  - admin

tags:
  - Ultrasound
  - Microrobots
  - Cavitation
---

Glad to see this one out! It was a lot of fun working with Songsong Tang to characterize the acoustic response of chemotactic microbubble robots (CBRs), an ultrasound-activated platform with exciting potential for targeted therapy.

## Two complementary microrobot designs

This work from Prof. Wei Gao's lab introduced two complementary robot types. Magnetically controlled microbubble robots (MBRs) combine enzyme-powered propulsion with ultrasound imaging and magnetic guidance. CBRs instead use catalase functionalization to respond to endogenous hydrogen peroxide gradients, allowing them to migrate toward tumor microenvironments without external field guidance.

Both designs contain a gas-filled component that provides ultrasound contrast and can also be activated by focused ultrasound. That second function was where my contribution came in.

## Why cavitation matters

When a gas bubble is driven strongly enough by an acoustic field, its oscillations can become nonlinear and culminate in inertial cavitation. The rapid expansion and collapse generate localized mechanical effects that can help disrupt the robot shell and enhance penetration of a therapeutic payload.

To study this response, I assembled a passive cavitation detection (PCD) setup. A PCD listens for the broadband acoustic emissions associated with inertial cavitation while the sample is being insonated, giving us a way to track when cavitation begins and how long it persists.

![Experimental setup for the passive cavitation detection experiments.](setup.png)

## My contribution

The time-frequency measurements compared CBRs with degassed phosphate-buffered saline and commercial microbubbles. The resulting cavitation maps showed that the gas carried by the CBRs could sustain inertial cavitation signals for several seconds under insonation.

We complemented the measurements with a Keller-Miksis bubble-dynamics model. This relatively compact model captures the nonlinear radial motion of a spherical bubble in a compressible liquid and helped us estimate the pressure threshold at which bubbles of the relevant size would transition into inertial cavitation.

![Keller-Miksis simulations used to estimate the cavitation threshold.](keller-miksis.png)

## What we found

Together, the PCD measurements and simulations provided a mechanistic link between the acoustic exposure and the cavitation behavior of the robots. In the full study, focused ultrasound triggered shell collapse and inertial cavitation, producing mechanical effects that enhanced therapeutic payload penetration.

The broader platform is especially interesting because propulsion, imaging, guidance, targeting, and ultrasound activation are integrated into the same biodegradable microrobot design. There is still a substantial path from an experimental platform to clinical use, but this combination offers a compelling direction for image-guided and spatially controlled therapy.

Working with Songsong was a real pleasure and helped forge a great friendship. You can [read the paper in *Nature Nanotechnology*](https://www.nature.com/articles/s41565-025-02109-6) or see [Caltech's overview of the bubble-bot platform](https://www.caltech.edu/about/news/bubble-bots-simple-biocompatible-microrobots-autonomously-target-tumors).

![Songsong Tang and Ernesto Criado-Hidalgo.](songsong-ech.jpg)
