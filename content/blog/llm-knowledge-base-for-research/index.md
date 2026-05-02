---
title: Shapiro Lab LLM Knowledge Base
summary: Raw information to structured wiki to grounded research questions answered over your own corpus.
date: 2026-04-23

image:
  caption: 'Knowledge graph view from the Shapiro Lab LLM knowledge base.'

authors:
  - admin

tags:
  - LLMs
  - Knowledge Base
  - Research Workflow
  - Obsidian
  - OpenAI API
---

I recently got inspired by [Karpathy's post on LLM Knowledge Bases](https://x.com/karpathy/status/2039805659525644595), and decided to build my own **Shapiro Lab LLM Knowledge Base (KB)** 😅

💡 The idea for this is simple:  
Raw information → structured wiki → continuously refined and queried with LLMs

{{< video src="shapiro-lab-kb-demo.mp4" controls="yes" >}}

🧠 What the system does:

- Ingests papers, supplementary, notes or potentially any other material, like lab notebooks, drafts, bioarxivs, etc. from a raw directory
- Converts them into structured Markdown notes (papers, concepts, methods)
- Builds a connected graph inside Obsidian (with backlinks + maps)
- Lets you ask research questions and get grounded answers based on your own corpus (this is the really cool feature!)
- Runs "linting" passes to detect inconsistencies, missing links, and new concept opportunities

⚙️ Under the hood:

- Python scripts for ingestion + maintenance
- OpenAI API for summarization, synthesis, and QA
- Obsidian as the interface / visualization layer
- A lightweight RAG-style retrieval system over local notes

📊 The result:

Instead of a pile of PDFs, you get a growing knowledge graph that surfaces connections, recurring design patterns, and gaps across papers or other pieces of information. You can directly ask questions that will generate new answers through the LLM. For example, I can ask:

👉 "How long should I express GVs in mammalian cells before ultrasound imaging?"

...and get a synthesized answer that abstracts across multiple papers (not just summaries), identifying things like:

- 24/48h prior as a short answer
- other suggestions for in vitro or in vivo experiments

I also experimented with local LLMs (Ollama) for this pipeline. They can work for smaller setups, but for now cloud models (via the OpenAI API or similar) provided more reliable reasoning and synthesis for this kind of research workflow.

Now, why is this better than just asking ChatGPT? -> A **knowledge base approach** pairs an LLM with an external, searchable collection of documents, facts, or data that is continuously growing and not necessarily public (drafts, internal documents, etc.). The system first retrieves the most relevant pieces from this knowledge base and then feeds them as context to the LLM for generating a response. In contrast, querying an **LLM directly** relies solely on the model's internal "parametric" knowledge—everything it learned and compressed during training.

Had so much fun implementing this!!
