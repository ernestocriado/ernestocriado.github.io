---
title: From Neural Data to Bayesian Models at DataSAI
summary: An immersive two-week Caltech summer school on practical data science, AI, and statistical modeling for neuroscience.
date: 2025-06-30

image:
  caption: '2025 DataSAI for Neuroscience Summer School group shot at Caltech.'

authors:
  - admin

tags:
  - Neuroscience
  - Data Science
  - Caltech
---

I spent the last part of June at the 2025 Data Science and AI for Neuroscience Summer School at Caltech. It was an immersive two-week program for people in neuroscience who want to get more comfortable with the computational side of the field, and it struck a really nice balance between practical workflows and the theory behind them.

## What made it useful

The curriculum built up in a very intentional way. We started with Python-based data wrangling and visualization, then moved into neuroscience data formats and organization, and eventually into probability, sampling, Bayesian inference, MCMC, model assessment, and optimization. The technical sessions also touched on split-apply-combine workflows, file formats such as MAT, TDT, HDF5, and NWB, and the kinds of tools that make large neuroscience datasets much easier to work with.

## A few themes that stuck with me

- keeping data structures clean enough that analysis stays reproducible
- using visualization to catch issues before they turn into modeling mistakes
- thinking about model selection and posterior checks as part of the workflow
- using hierarchical models, PCA, HMMs, and GLMs when the question calls for them
- treating inference as a pipeline rather than a one-off calculation

One especially helpful companion resource was [Distribution Explorer](https://distribution-explorer.github.io/), which is a great way to build intuition about probability distributions, sampling behavior, and how assumptions shape model geometry.

![Aggression raster and posterior corner plot from the technical sessions.](technical-composite.png)

The composite above captures two useful views of the problems we worked through. One aligns behavioral labels, including sex and attack events, with neural population activity over time. The other is a corner plot, which makes the marginal distributions and pairwise relationships between inferred parameters visible. Together, they are a nice reminder that good analysis needs both temporal context and a clear picture of uncertainty.

## Why it mattered

What I appreciated most was that the school never treated data science as an abstract add-on. The emphasis stayed on real neuroscience use cases, where the goal is to move from noisy measurements to interpretable results without losing the structure of the problem along the way. The shared pace also made it easy to talk through ideas with other participants and instructors, which was just as valuable as the technical content itself.

More information is available on the [official DataSAI summer school page](https://neuroscience.caltech.edu/programs/datasai-for-neuroscience-summer-schools/2025-data-science-and-ai-for-neuroscience-summer-school), and the [technical course materials](https://caltech-datasai.github.io/) remain online as a useful reference.

I left with a stronger appreciation for how much more expressive neuroscience analysis becomes when data handling, visualization, and statistical modeling are treated as one continuous workflow.
