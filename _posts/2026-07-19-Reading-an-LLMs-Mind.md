---
title: "Reading an LLM's Mind with Causal Effects"
date: 2026-07-05T00:00:00-00:00
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

![causal-j-space](/assets/images/20260719-CausalJSpace.png)

*Originally published in* [*Causal Python weekly*](https://causalpython.io/).
*Sign up and get up-to-date coverage of Causal AI for free.*

The internal **causal mechanisms** of Large Language Models (LLMs) are in the spotlight.

In a brand-new paper, Jack Lindsey, Wes Gurnee, Nicholas Sofroniew, and colleagues from *Anthropic Research* present **J-Lens, a novel interpretability technique**.

J-Lens surfaces concepts from internal LLM activity during inference. Those concepts could be analogous to **consciously accessible thoughts** in humans.

This interpretability technique allows us to know, roughly speaking, what the model is thinking. The model could even, as the authors show, be thinking about one thing while answering something different.

I found two elements in this paper that might be of particular interest to the causal community.

**How J-Lens Works**

The first is how J-Lens works. As the authors explain, *“the basic idea is to characterize an intermediate activation vector by its **first-order causal effect** on the model’s outputs, over a broad distribution of **potential contexts**.”* (Emphasis added.).

This method asks how an output would be affected by the presence of a concept within a given intermediate vector.

Our readers might remember a review we wrote earlier this year on a [Max Planck Institute paper](https://arxiv.org/abs/2602.04718) about how to produce intervenable features inside LLMs using Sparse Autoencoders (SAEs). (By the way, that paper was accepted this month at COLM.)

Instead of deliberately producing those features, Anthropic researchers found this representational space to be an emergent property of LLMs that is discoverable with J-Lens. They call this representational space **J-Space**.

But interestingly, some of the examples they present follow the same logic as the paper from the Max Planck Institute.

In one example, the authors ask the LLM to tell “the number of legs on the animal that spins webs”. The model answers ‘8’, and it is possible to find through the J-Lens the word ‘spider’. Now, if we replace the vector representing ‘spider’ in the J-Space with the vector representing ‘ant’, then the model’s answer changes to ‘6’.

**A New Training Technique**

The second interesting element in the paper from a causal standpoint is a new training technique based on counterfactual reasoning. They call it **Counterfactual Reflection Training**.

The training implemented in the models consists of doing one thing: if interrupted mid-task and asked to reflect, articulate a set of ethical principles.

The hypothesis is that training the model to articulate principles in **counterfactual reflective continuations** of a context will populate the J-Space in the original context with concepts related to those principles and thereby shape the model’s behavior.

Code is available [here](https://github.com/anthropics/jacobian-lens).

[Explore the paper](https://transformer-circuits.pub/2026/workspace/index.html)

*Written by Alberto D. Horner*