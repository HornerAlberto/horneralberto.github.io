---
title: "Grow your agent wisely"
date: 2026-07-05T00:00:00-00:00
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

![causal-llm-development](/assets/images/20260705-CausalLLMDevelopmentNeon.png)

*Originally published in* [*Causal Python weekly*](https://causalpython.io/).
*Sign up and get up-to-date coverage of Causal AI for free.*

**The opportunity to leverage Causal Inference for LLM development**

To say that Causal Inference is underutilized in the biggest area of the AI industry is not a statement that could be passed inadvertently. And that is exactly the case.

In a brand-new KDD paper, an interdisciplinary group (*LMU Munich, Carnegie Mellon, Imperial College London*, and *University of Toronto*) presents where, how and why the opportunity to leverage causal methods can be found in the Large Language Models (LLMs) development and evaluation lifecycle.

Most decisions within the LLM lifecycle can be better framed as treatments.


![causal-llm-development](/assets/images/20260705-CausalLLMDevelopment.png)

**Where to apply it**

Imagine that, before fine-tuning your model, you could effectively calculate how much advantage and improvement your team and end users would get. You could be confident whether that decision deserves your effort or not.

In addition to that, most logged data that comes from LLM apps is biased.

Think about a router that sends more complex queries to higher reasoning LLMs. Based on outcomes, it could seem that the strongest LLM is performing worse than a distilled or lighter one.

Causal methods could help you debias your data, and even more. You can answer a variety of questions such as whether the data you have is enough to ground up a confident decision, something that causal inference traditionally calls *identifiability*.

You will find a clarifying note at the beginning of the paper: the intersection of causal reasoning and LLMs has been explored regarding how LLMs could be equipped with causal reasoning abilities.

What we have here is a novel approach: how could causal inference add value to LLM development projects and guide them in building, evaluating, and optimizing LLM systems more reliably.

**Enriching for a variety of roles**

From that perspective, this paper could be enriching for a variety of role: business owners, project managers, engineers, researchers and sales professionals.

A stakeholder can know how much value is being created with a feature improvement. Developers will discover a whole new horizon to improve their models and align them with the expected task at hand.

The paper explicitly flags research opportunities that allow researchers to focus on one problem and contribute to this area; from a research standpoint, this is just the beginning.

Sales professionals, on the other hand, will find a powerful tool to frame value propositions and ROI measurements that enable them to build trust and long-term value for their clients.

The authors present clear examples regarding pre-training, evaluation, retrieval, routing, and offline policy learning.

Changing chunking strategy, lowering temperature, using prompt engineering, and increasing some domain weights during pretraining are all treatments linked to outcomes such as model performance, user preference or retrieval relevance.

[Explore the paper](https://arxiv.org/abs/2605.25998)

*Written by Alberto D. Horner*