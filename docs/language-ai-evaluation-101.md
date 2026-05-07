# Language AI Evaluation 101: Know Your User

*Originally published on [Medium](https://medium.com/@boris.dev/why-did-your-language-ai-feature-fail-66a280954287), Mar 20, 2023. Co-authors: Robert McKee and Shawn Larson.*

## Background

A language AI application can be a liability to your customer if it makes just a few terrible judgements on high-risk matters.

## The evaluation problem

"Most AI applications launch with bad predictions." Why? The cause is an overly simplistic evaluation test dataset that leads to exaggeratedly positive evaluation metrics. By "overly simplistic" we mean that the evaluation dataset, or Ground Truth, does not contain examples that robustly represent high-stakes, nuanced customer semantic judgements. Why is this Ground Truth so challenging to build? Because it requires both customer feedback and data science.

## Illustration

Imagine a Mom whose children text her hundreds of questions every day. Your job is to build her a language AI app that reduces her toil. You start by building a Ground Truth dataset of example correct responses. This Ground Truth is key to evaluating your future AI's prediction performance.

**Iteration 1's Ground Truth.** The problem with this initial set of examples is that all of them depend on rationales that are overly simplistic. After training the model on these examples, evaluation against a test set drawn from the same simplistic distribution yields a 100% accuracy metric. That metric is misleading.

To make a more rigorous evaluation, we need to discover more nuanced examples — questions whose correct response depends on context, priority, or risk that the simplistic rationales don't capture.

**Iteration 2's Ground Truth.** Adding nuanced examples depends on *cognitive empathy* — sitting with the customer and discovering the implicit principles she actually uses. When we re-evaluate the same model against this richer test set, the accuracy drops to 0%.

The lesson is twofold:

1. **Your quantitative evaluation will be misleading when your Ground Truth is overly simplistic.** Same model, two test sets, two opposite verdicts.
2. **Building Ground Truth is iterative, not a checkoff.** It is a continuous-improvement process driven by customer dialog, not a one-time annotation pass.

In summary: *without cognitive empathy for your customer, your language AI performance metrics are meaningless.*

## Connection to the IR-compile pattern

This is step 1 of [the pattern](boris_dev_resume.md#common-pattern) — decomposing human expertise into an IR — applied specifically to evaluation. The "nuanced rationales" you discover through cognitive empathy *are* the primitive concepts of the domain IR. Without that decomposition, the eval dataset is just surface-text matching, and the metric measures nothing real.

## References

1. *Human-in-the-Loop Machine Learning* by Robert Munro, O'Reilly Media, 2021.
2. *The One Practice That Is Separating The AI Successes From The Failures.* Forbes, Aug 14, 2022.
3. *Evaluation.* LangChain Blog, March 14, 2023.
