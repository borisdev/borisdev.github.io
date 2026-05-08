---
description: A working definition of knowledge engineering, built around elicitation, evaluation, and 0-to-1 modeling in messy niche domains.
---

# What is knowledge engineering, really?

*A working definition, framed around three questions, with examples drawn from a decade of building software in messy niche domains.*

## The shortest definition

Knowledge engineering is the discipline of moving expert knowledge into computational systems in a way that is **reproducible and scalable**. It sits between domain experts who know things and the software that needs to act on what they know.

It is most visible right now in the AI world — RAG systems, fine-tuned LLMs, evaluation frameworks — but it predates LLMs and will outlast whatever model is fashionable next year. The interesting questions are mostly the same ones they have always been.

## Three questions that define the work

### 1. How do we elicit knowledge and performance feedback from domain experts and customers?

Experts rarely have their knowledge in a form that is ready to be encoded. The job is to draw it out, structure it, and create a feedback loop that makes the encoding better over time.

*Example.* Working with lawyers and paralegals on a legal-billing classification system, the rubric was refined by facilitating Slack discussions and running an active-learning pipeline that surfaced progressively harder examples for the experts to adjudicate. The output was not just a labeled dataset — it was a living rubric that the experts themselves trusted.

### 2. How do we embed nuanced, subjective concepts of quality into scalable, reproducible evaluation?

"Good" is the hardest thing to operationalize. Most evaluation breaks down because the metric drifts away from what the expert actually meant by good.

*Example.* An AI evaluation framework for email quality, where subjective judgements about tone, clarity, and appropriateness had to be turned into a graded scoring system that an automated pipeline could apply at scale without an expert in the loop for every example.

*Earlier example.* The same problem appears in academic research: a Ph.D. thesis on income inequality required embedding nuanced ideas of fairness into statistical analysis, where the choice of metric is itself the argument.

### 3. How do we do 0→1 engineering in messy niche domains?

Most of the interesting knowledge in the economy lives inside narrow domains where the rules are tacit and the data is bad. The work is figuring out the right entity types and the right primitives — what counts as an "invoice line item," a "scene card," a "treatment effect" — before any model or system can be built on top.

A partial list of niche domains where 0→1 modeling produced real software:

- legal billing flags for invalid invoice line items
- earnings call calendar events
- murder-mystery storyboard scene cards
- clinical study treatment effects
- AI behavioral expectations and email guidance for handling supplier errors in the maritime construction industry

Each of these required spending real time inside the domain — with paralegals, with analysts, with directors, with project managers — before the entity model made sense.

## Why this matters now

Two trends are making knowledge engineering more important, not less:

1. **LLMs collapsed the cost of generic NLP** but did not solve the problem of *whose* knowledge the model is supposed to encode. Fine-tuning, RAG, and evaluation are all knowledge engineering problems wearing new clothes.
2. **The bottleneck on AI feature quality** has moved from model architecture to the discovery and encoding of expert mental models. The teams that ship working AI features are the ones that take elicitation, evaluation, and 0→1 domain modeling seriously.

If you are building an AI product and the model is not the hard part anymore, the question worth asking is: who on your team owns the knowledge engineering?
