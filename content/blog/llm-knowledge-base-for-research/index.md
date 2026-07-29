---
title: Building an LLM Knowledge Base for Scientific Research
summary: Turning a growing collection of papers and notes into a structured, searchable knowledge system for grounded research questions.
date: 2026-04-23

image:
  caption: 'Knowledge graph view from the Shapiro Lab LLM knowledge base.'

authors:
  - admin

tags:
  - Artificial Intelligence
  - Knowledge Base
  - Research Workflow
---

I recently got inspired by [Karpathy's post on LLM knowledge bases](https://x.com/karpathy/status/2039805659525644595) and decided to build my own **Shapiro Lab LLM Knowledge Base (KB)** 😅

The idea is simple:

**Raw information → structured wiki → continuously refined and queried with LLMs**

{{< video src="shapiro-lab-kb-demo.mp4" poster="featured.jpg" controls="yes" title="Silent demonstration of the Shapiro Lab LLM knowledge-base workflow" >}}

*Silent screen recording showing the structured notes and connected knowledge graph used in the workflow described below.*

## What the system does

The system begins with a raw directory rather than a carefully curated database. From there, a set of ingestion and maintenance scripts turns heterogeneous research material into a connected collection of Markdown notes.

- Ingests papers, supplementary information, notes, lab notebooks, drafts, bioRxiv preprints, and other research material
- Converts them into structured Markdown notes (papers, concepts, methods)
- Builds a connected graph inside Obsidian (with backlinks + maps)
- Lets you ask research questions and get grounded answers based on your own corpus
- Runs "linting" passes to detect inconsistencies, missing links, and new concept opportunities

## Under the hood

Python scripts handle ingestion and maintenance, while the OpenAI API supports summarization, synthesis, and question answering. Obsidian serves as the interface and visualization layer, making it easy to inspect individual notes, follow backlinks, and explore the knowledge graph.

For question answering, a lightweight retrieval-augmented generation workflow searches the local notes, selects the most relevant passages, and provides them to the model as context. That separation is important: the source material remains inspectable, while the model is used to connect and synthesize evidence rather than replace it.

## From PDFs to grounded answers

Instead of a pile of PDFs, the result is a growing knowledge graph that can surface connections, recurring design patterns, and gaps across papers and notes. It also supports questions that require information from several sources rather than a summary of a single document.

For example, I can ask:

👉 "How long should I express GVs in mammalian cells before ultrasound imaging?"

The system can then synthesize a practical answer across multiple papers, such as:

- A short recommendation of 24–48 hours before imaging
- Additional considerations for in vitro and in vivo experiments

The useful part is not only the answer. Because the retrieval step exposes the supporting notes, I can inspect where a recommendation came from, compare experimental conditions, and decide whether the evidence applies to the experiment I am planning.

## What I learned

I also experimented with local models through Ollama. They can work well for smaller setups and have clear privacy advantages, but cloud models currently gave me more reliable reasoning and synthesis for this workflow. Model choice was only one part of the problem, though. Retrieval quality, consistent note structure, source attribution, and human verification all mattered just as much.

This project also made it clear that a knowledge base is never truly "finished." New papers need to be ingested, concepts need to be consolidated, and contradictory or weakly supported statements need to be surfaced rather than silently blended together. The linting passes are therefore not just housekeeping; they are part of maintaining the scientific usefulness of the system.

These lessons connected directly with what I later explored during Caltech's [AI for Research Bootcamp](/blog/ai-for-research-bootcamp-2026/), especially the tradeoffs between long context, vector retrieval, knowledge graphs, and agentic research workflows.

## Why not just ask ChatGPT?

A **knowledge base approach** pairs an LLM with an external, searchable collection of documents, facts, and data that can keep growing and can include non-public material such as drafts or internal notes. The system retrieves the most relevant pieces first and gives them to the model as context for its response.

By contrast, querying an **LLM directly** relies mainly on the model's internal parametric knowledge: information compressed during training, without guaranteed access to the specific documents, experimental details, or private material that matter for the question at hand.

The knowledge base does not eliminate the need to read papers or verify an answer. What it does is make a large research corpus easier to navigate and turn scattered information into a more useful starting point for scientific reasoning. I had a lot of fun building it, and I am excited to keep refining it.
