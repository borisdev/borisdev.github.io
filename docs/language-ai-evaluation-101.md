# Language AI Evaluation 101: Know Your User

*Originally published on [Medium](https://medium.com/@boris.dev/why-did-your-language-ai-feature-fail-66a280954287), Mar 20, 2023. Co-authors: Robert McKee and Shawn Larson.*

## Background

A language AI application can be a liability to your customer if it makes just a few terrible judgements on high-risk matters.

## The evaluation problem

"Most AI applications launch with bad predictions." Why? The cause is an overly simplistic evaluation test dataset that leads to exaggeratedly positive evaluation metrics. By "overly simplistic" we mean that the evaluation dataset, or Ground Truth, does not contain examples that robustly represent high-stakes, nuanced customer semantic judgements. Why is this Ground Truth so challenging to build? Because it requires both customer feedback and data science.

## Illustration

Imagine a Mom whose children text her hundreds of questions every day. Your job is to build her a language AI app that reduces her toil. You start by building a Ground Truth dataset of example correct responses. This Ground Truth is key to evaluating your future AI's prediction performance.

**Table 1: Iteration 1's Ground Truth**

| child's question | Mom's response | rationale |
|---|---|---|
| Should I clean my toys? | Yes | Prioritize cleaning up. |
| Should I run across the busy street? | No | Prioritize safety. |
| Should I go to school? | Yes | Prioritize schooling. |

The problem with this initial Ground Truth is that all its examples depend on rationales that are overly simplistic. After training the model on these examples, we evaluate its performance.

**Table 2: Evaluation result with Iteration 1's Ground Truth**

| child's question | AI's response | rationale |
|---|---|---|
| Should I clean my room? | Yes (correct answer) | Prioritize cleaning up. |
| Can I ride the motorcycle? | No (correct answer) | Prioritize safety. |
| Should I go to math class? | Yes (correct answer) | Prioritize schooling. |

Evaluation using Table 2's result leads to a 100% accuracy metric. Next, we illustrate why this metric is misleading.

To make a more rigorous evaluation, we need to discover more nuanced examples. Look at the bottom three examples in the next iteration of our Ground Truth in Table 3.

**Table 3: Iteration 2's Ground Truth**

| child's question | Mom's response | rationale |
|---|---|---|
| Should I clean my toys? | Yes | Prioritize cleaning up. |
| Should I run across the busy street? | No | Prioritize safety. |
| Should I go to school? | Yes | Prioritize schooling. |
| Should I clean my toys over catching the school bus? | No | Prioritize school over cleaning. |
| Should I do ski jump training at ski school? | Yes | It's safest to learn risky stuff at school. |
| Should I go to school with Covid-19? | No | Prioritize not harming over school. |

Notice how these examples map to more nuanced rationales than existed in the initial Ground Truth. Discovering them depends on *cognitive empathy*. The next table illustrates that using more complex questions demanding more nuanced rationales results in a more rigorous evaluation.

**Table 4: Evaluation result with Iteration 2's Ground Truth**

| child's question | AI's response | simplistic rationale |
|---|---|---|
| Should I clean my toys over catching the school bus? | Yes (wrong answer) | Prioritize cleaning up |
| Should I do ski jump training at ski school? | No (wrong answer) | Prioritize safety |
| Should I go to school with Covid-19? | Yes (wrong answer) | Prioritize schooling |

Evaluation using Table 4's result leads to a 0% accuracy metric — the opposite of the 100% from Table 2.

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
