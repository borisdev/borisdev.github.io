# What makes launching a domain-specific language AI feature especially difficult?

*For CTOs and product managers wondering why their domain-specific language AI feature is underperforming.*

## What a language feature is supposed to do

The purpose of a language feature in a software product is to reduce expensive and extraneous cognitive load on your customer when she is repeatedly making judgements on a stream of business text. For example, a domain-specific language feature might be aimed at reducing your customer's toil when she needs to judge which of a daily stream of thousands of email complaints deserves the highest business priority.

A *domain-specific* language is one that contains specialized rules and terminology. A domain expert — a subject-matter expert — is required to train the model. To scale the expert, companies typically hire annotators, and this is where most projects begin to fail: the resulting training data is poor, and the AI's performance follows.

## Why these projects are hard

Success depends on experimentation and cognitive empathy, much like the customer discovery process for startups. It requires uncovering the prioritized principles — the primitive concepts — that your customer uses when translating what she is reading into a judgement that will impact her business or her life.

An analogy: a mom can't gather powerful learning examples to teach a baby to make judgements in an area until the mom herself has a set of prioritized principles. *Ignore losing the ball now; don't run across the busy street.* Likewise, you can't start to gather examples to train a machine to make judgements on behalf of your customer until you understand your customer's highest-priority principles. Otherwise, your AI predictions will be a nuisance to your customer at best, or a liability at worst.

## How to avoid the failure

You need a discovery process that keeps refining your understanding of the customer's principles in the domain. Two roles are enough to put a foundational discovery process in place before scaling up:

- **The subject-matter expert** (or the customer themselves)
- **The data scientist**, to crunch the expert's knowledge into a prototype

A simple checklist for CTOs, before they scale:

1. **Maintain an evolving, versioned document of your customer's language.** It serves two purposes: a model for the prototypes you'll build, and a Rosetta Stone that lets engineers, data scientists, sales, and product act cohesively.
2. **Build prototypes to get customer feedback quickly.** Treat your initial assumptions about the customer's mental model as wrong by default.
3. **Avoid large-scale human labeling in favor of fine-tuning a large language model with programmatic labeling.**

## Why the Lean Startup approach applies

Most AI projects fail, and a language AI project is especially difficult because of the ambiguity in understanding the customer. With a Lean Startup approach, you anticipate that your original assumptions about the customer's mental language model will be way off. If you are looking at a failed language AI feature, the most likely cause is a waterfall approach: you did not get enough customer feedback soon enough.

You can restart by first building a foundational discovery process around your customer's implicit language mental model — then earning the right to scale.
