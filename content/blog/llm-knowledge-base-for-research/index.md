---
title: Building an LLM Knowledge Base for Research
summary: Turning a pile of papers and notes into a structured, queryable knowledge graph for lab research.
date: 2026-04-30

image:
  caption: 'Short demo of the Shapiro Lab knowledge base in Obsidian.'

authors:
  - admin

tags:
  - LLMs
  - Knowledge Base
  - Research Workflow
  - Obsidian
  - OpenAI API
---

I recently got inspired by Karpathy's post on LLM knowledge bases and decided to build my own **Shapiro Lab LLM Knowledge Base**.

The core idea is simple:

> raw information -> structured wiki -> continuously refined and queried with LLMs

Instead of treating papers, notes, drafts, and supplementary files as disconnected documents, I wanted a system that could turn them into a growing knowledge graph that is actually useful for research.

{{< video src="shapiro-lab-kb-demo.mp4" controls="yes" >}}

{{< toc mobile_only=true is_open=true >}}

## What the system does

The pipeline is designed to work from a raw directory of research material and progressively organize it into something more usable.

- It ingests papers, supplementary material, notes, and in principle any related lab material such as notebooks, drafts, or bioRxiv manuscripts.
- It converts them into structured Markdown notes for papers, concepts, and methods.
- It builds a connected graph inside Obsidian using backlinks, references, and local maps.
- It lets me ask research questions and get grounded answers based on my own corpus.
- It runs maintenance and linting passes to detect inconsistencies, missing links, and opportunities for new concept pages.

## Under the hood

The implementation is intentionally lightweight.

- **Python** scripts handle ingestion, note generation, and maintenance passes.
- The **OpenAI API** handles summarization, synthesis, and question answering.
- **Obsidian** works as the interface and visualization layer.
- A lightweight **RAG-style retrieval layer** grounds answers in the local notes rather than relying only on model memory.

## Why this is useful

The most interesting part is not just generating summaries, but generating *new answers* from your own body of work.

For example, I can ask:

> How long should I express GVs in mammalian cells before ultrasound imaging?

and get a synthesized answer that abstracts across multiple sources, not just one-paper summaries. In this case, the system can surface patterns like:

- **24 to 48 hours** as a short practical answer
- alternative suggestions depending on whether the context is **in vitro** or **in vivo**

That kind of cross-document synthesis is what makes the system feel different from a static notes folder.

## Why not just ask ChatGPT?

A **knowledge-base approach** pairs an LLM with an external, searchable collection of documents, facts, and notes that can keep growing over time. The system first retrieves the most relevant pieces of that corpus and then feeds them as context into the model.

In contrast, querying an LLM directly relies only on the model's internal, compressed training knowledge. That can be useful, but it is not the same as reasoning over your own evolving set of papers, drafts, and internal documents.

For research, that difference matters a lot.

## Local models versus cloud models

I also experimented with local LLMs through **Ollama** for this pipeline. They can work for smaller setups, and I like the idea of having a more self-contained system.

For now, though, cloud models accessed through the OpenAI API or similar services gave me more reliable reasoning and synthesis for this kind of workflow.

## Final thought

The result is something much more useful than a pile of PDFs: a growing knowledge graph that surfaces recurring design patterns, hidden connections, and gaps across papers and notes.

I had a lot of fun building it, and I think this kind of workflow has real potential for research groups that want to make their internal knowledge more searchable, connected, and reusable.
