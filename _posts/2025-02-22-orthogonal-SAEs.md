---
title: "How to produce Intervenable features inside LLMs"
date: 2026-02-22T00:00:00-00:00
excerpt_separator: "<!--more-->"
categories:
  - Blog
---
![Othogonal-SAEs-metrics](/assets/images/LLMsInterventionFigure20260222.png)


*Originally published in* [*Causal Python weekly*](https://causalpython.io/)
*Sign up and get up-to-date coverage of Causal AI for free.*

When it comes to knowing what is going on inside a Large Language Model (LLM), Sparse Autoencoders (SAEs) are popular mechanisms that can discover features in the model’s representation space. This makes models more interpretable.

In a brand-new paper, Moritz Miller, Florent Draye, and Bernhard Schölkopf from the Max Planck Institute for Intelligent Systems, take a step further. Inspired by the idea of Independent Causal Mechanisms (ICM), they fine-tuned a model to let the features be almost orthogonal.

Then, in addition to being human understandable, this enhances the model with additional properties without significantly compromising its accuracy:

1. For a given input, it is possible to identify how a feature is independently involved in producing the output.

2. It is possible to intervene in a feature and observe how the output changes in that respect while remaining invariant in every other aspect.

Additionally, the authors suggest that intervenable features might mitigate adversarial vulnerabilities, leading towards more robust and safer models, but this requires further investigation.

The figure above shows how intervention correctness increases as the SAE’s features are enforced to be more distinct, while the model’s accuracy remains essentially unchanged. The parameter λ is the penalty for non-orthogonality in the loss function.

In contrast to traditional causality, which studies interventions as distributional shifts in relation to an underlying data-generation-process, here the authors study intervenability on the modeling level.

The purpose is to uncover causal mechanisms inside the model’s representation space.

The results are limited to the MetaMathQA dataset (math problems), and one SAE variant (TopK). Therefore, the authors invite future research to focus on tasks different from mathematical reasoning, and other SAE variants like JumpReLU.

This is an important step towards a more human-aligned and safer AI, making LLM internals more transparent and controllable.

Code for the paper is available [here](https://github.com/mrtzmllr/sae-icm).

[Explore the Paper](https://arxiv.org/pdf/2602.04718)
