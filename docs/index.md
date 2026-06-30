---
title: Boris Dev — Knowledge Engineer in Messy Domains
description: Essays on intermediate representations, evaluation, and the IR-compile pattern across clinical evidence, legal billing, narrative gaming, manufacturing analytics, and human geography.
---

## About me

I dissect high-stakes AI judgments into the underlying structures experts use—often implicitly—and encode them so the reasoning becomes transparent and reproducible: domain ontology as code.

### Knowledge-dissection projects

- **Tau-Bench Belief State** — What did the user actually want, what did the agent believe, and what did the task rules require? I model these hidden states as a typed problem specification before evaluating the solution. [github.com/borisdev/tau-belief-state-bench](https://github.com/borisdev/tau-belief-state-bench)
- **NoBSmed** — What makes a medication or supplement recommendation questionable given the evidence, missing evidence, and relevance to the patient?
- **HealthBench audit** — What makes a "doctor-approved" answer or grading rubric unreliable? I found fabricated citations and 29 possible patient-harm issues in OpenAI's medical-AI benchmark family. [github.com/borisdev/nobsmed-healthbench-audit](https://github.com/borisdev/nobsmed-healthbench-audit)
- **Wolf Games** — What makes an AI-generated murder-mystery storyboard coherent across interpolated scenes?
- **PhD thesis** — What makes an inequality metric capture nuanced gaps among social groups in the same city? I modeled those relationships as weighted edges.
- **SimpleLegal** — What makes "Called the State Senator" lawyer-level work rather than an administrative task? The classification depended on the relevance of the output, not the wording of the task.

### Selected technical impact

- Built an AI agent-evaluation framework for Sindri.ai using Temporal.
- Helped relaunch a stalled legal-billing AI feature by eliciting lawyer expertise and redesigning the rubric for 11 billing flags.
- Built story-scene prediction for a gaming startup led by a Law & Order producer.
- Contributed an experimental causal-graph agent to LangChain: [langchain-ai/langchain#6255](https://github.com/langchain-ai/langchain/pull/6255)
- Built backend systems for factory analytics, people analytics, and Tableau geospatial services.
- Embedded subjective concerns into statistical analysis of income inequality in my social-science PhD: [escholarship.org/content/qt8br7d5df](https://escholarship.org/content/qt8br7d5df/qt8br7d5df.pdf)

### Non-tech fun points

- Climbed Cotopaxi (about 19,300 ft).
- Survived bodyboarding Mexpipe.
- Taught geospatial data to students in Medellín, Colombia.
- Taught kids snowboarding.
- Managed an international restaurant team.
- Counseled severely emotionally disturbed children.

## Elsewhere

- [Nobsmed blog](https://nobsmed.com/blog) — work-in-progress notes on clinical-evidence retrieval and personalized trial matching:
    - [The Evidence-to-Person Fit Problem](https://nobsmed.com/blog/evidence-to-person-fit)
    - [The Medical AI Landscape](https://nobsmed.com/blog/medical-ai-landscape)
    - [Medical AI Developer Tooling](https://nobsmed.com/blog/medical-ai-developer-tooling)
- [evidence-to-person-eval](https://github.com/borisdev/evidence-to-person-eval) — open benchmark for whether Medical AI applies clinical-study findings to heterogeneous people without overgeneralizing

## Writing

Essays on the patterns I've seen recur. Some are primarily a way to organize my own learning; I'm not an expert in everything I write about — especially the compiler-design piece.

| # | Title | Topic |
|---|-------|-------|
| 1 | [Beyond RAG: How Chomsky's I-Language and Compiler Design Converge on Knowledge Graphs](domain-grammar-compiler.md) | LLVM-style IR, Chomsky's I-language, BFO ontology, grammar-first design |
| 2 | [What Is Knowledge Engineering, Really?](knowledge-engineering.md) | A working definition built around elicitation, evaluation, and 0→1 modeling in messy domains |
| 3 | [Fine-Tuning LLMs Will Restructure Your Data Science Team](fine-tuning-restructures-data-science.md) | How fine-tuning replaces annotation pipelines and the NN-optimization role; the new "fine-tuning analyst" |
| 4 | [Why Domain-Specific Language AI Features Fail](domain-specific-language-ai.md) | The customer-discovery process for niche language AI, and why a Lean Startup approach is required |
| 5 | [Language AI Evaluation 101: Know Your User](language-ai-evaluation-101.md) | Why simplistic Ground Truth produces misleading accuracy metrics; cognitive empathy as the iteration loop |
| 6 | [Hyper-Local Community Funding: A DAO Alternative to CDFIs](hyperlocal-community-funding.md) | Local digital tokens and DAOs as a delivery mechanism for under-served-neighborhood capital |
| 7 | [Inequality with a Spatial View](spatial-view-is-a-graph.md) | A note from my 2014 dissertation: the same income data can read as inequality going down or up depending on whether you keep the spatial structure. A spatial view is a graph |
| 8 | [CV: Knowledge Engineering in Messy Domains](boris_dev_resume.md) | The IR-compile pattern across clinical trials, legal billing, maritime construction, narrative gaming, and geographic inequality |
