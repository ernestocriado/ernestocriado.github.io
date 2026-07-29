---
title: Modeling Tumor Heating Under Therapeutic Ultrasound
summary: An axisymmetric bioheat model combining measured acoustic fields, feedback control, and thermal imaging to study tumor heating under ultrasound.
date: 2025-12-01

image:
  caption: 'Axisymmetric bioheat FEM model and temperature evolution under therapeutic ultrasound.'

authors:
  - admin

tags:
  - Ultrasound
  - Computational Modeling
  - Cell Therapy
---

This was a short but really fun collaboration!

My labmate Ann Liu asked if I could help model how a subcutaneous tumor heats up under a therapeutic ultrasound transducer. The broader project used ultrasound-induced hyperthermia to activate engineered macrophages carrying a heat-responsive genetic switch, so understanding the temperature throughout the tumor was essential.

## The modeling question

During the experiments, an infrared camera measured the temperature at the skin surface while the ultrasound power was adjusted to maintain a target temperature. That feedback made the surface temperature observable, but the temperatures deeper inside the tumor could not be measured as directly.

The central question was therefore practical: **How accurately does the infrared surface measurement represent the temperature distribution across the tumor volume?**

## Building the model

We constructed an axisymmetric finite-element bioheat model using the acoustic field measured with a hydrophone. This let the simulated heat source retain the spatial structure of the experimental ultrasound beam rather than assuming uniform energy deposition.

We then coupled the model to a proportional-integral-derivative (PID) controller. The controller used the simulated surface temperature as feedback and adjusted the applied ultrasound power, mirroring how the infrared measurement informed power changes during the experiment.

The model included the tumor core, surrounding shell, coupling gel, skin-facing surface, and the direction of ultrasound propagation. It allowed us to follow both the rapid initial heating and the slower redistribution of heat over the full treatment period.

## What the simulations showed

The temperature distribution initially reflected the nonuniform acoustic field, but those spatial differences dissipated in less than a minute as heat spread through the tissue. After approximately five minutes, the simulated temperatures at the top and bottom of the tumor, as well as the maximum temperature within it, differed by only about 1 °C.

In other words, the tumor warmed and quickly approached a relatively homogeneous temperature distribution, without persistent internal hotspots. The surface temperature used by the controller also acted as a conservative proxy for the intratumoral temperature.

## Why it matters

For thermally controlled cell therapies, both undertreatment and overheating are important concerns. Too little heating may not activate enough engineered cells, while excessive or highly localized heating could damage tissue. The model gave us a way to connect an accessible surface measurement with the temperature experienced by cells throughout the tumor.

This was a compact modeling contribution, but it supported a much broader result: a brief, spatially targeted ultrasound-heating treatment could switch engineered macrophages into a stable active state, with localized gene expression persisting after treatment.

If you are curious about how ultrasound-activated heat-shock promoters can control engineered macrophages, read the full paper: [A. Liu *et al.*, "Thermally Controlled State Switches for Engineered Macrophages," *ACS Synthetic Biology* **14**, 4304–4313 (2025)](https://pubs.acs.org/doi/full/10.1021/acssynbio.5c00395).

This is a really exciting direction for ultrasound-controlled cell therapies.
