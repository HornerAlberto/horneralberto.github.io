---
title: "Causal Discovery: Making LLMs Better with Causal Ordering"
date: 2025-04-27T00:00:00-00:00
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

![causal-order-diagram](/assets/images/20260427CausalOrder1.png)

*Originally published in* [*Causal Python weekly*](https://causalpython.io/).
*Sign up and get up-to-date coverage of Causal AI for free.*


Over the past few years, large language models (LLMs) have been increasingly gaining attention in the causal community as potential helpers in causal discovery, even though they’re not perfect experts.

A recent paper presented at the ICLR by Aniket Vashishtha, Amit Sharma and a cross-disciplinary team (Microsoft Research, UIUC, CISPA, MIT, and IIT Hyderabad), argues that causal order is a more effective approach for leveraging expert knowledge than forcing it to convey a completely defined causal graph.

As they point out, an optimal (perfect) expert prompted with only two variables at a time could incorrectly predict the underlying causal graph but will always predict the causal order correctly.

The authors also propose a new strategy to prompt any expert (human or not, perfect or not).

Instead of asking about each pair of variables in isolation, include a third variable for context.

This triplet method improves performance across several metrics, including the number of cycles, Structural Matching Error (SME), and a novel measure based on topological divergence.

By balancing additional context with minimal added complexity, the triplet method reliably reduces error.

In fact, the probability of error when using triplets is always less than or equal to the probability of error with standard pairwise prompts.

The code is not currently available, but the authors promised to add it soon [here](https://pjvglb.clicks.mlsend.com/td/cl/eyJ2Ijoie1wiYVwiOjUxNjI1MSxcImxcIjoxNTI4NTQzMTI2Njc1ODAwNjIsXCJyXCI6MTUyODU0MzgwNzQ1MzI3ODY4fSIsInMiOiI1MjJkOTEyM2Y5M2Q5MzNjIn0).

![Explore the paper](https://pjvglb.clicks.mlsend.com/td/cl/eyJ2Ijoie1wiYVwiOjUxNjI1MSxcImxcIjoxNTI4NTQzMTI2NzgwNjU4MjUsXCJyXCI6MTUyODU0MzgwNzQ1MzI3ODY4fSIsInMiOiJkNjExZTAwYzY1ZGMxNjJhIn0)

*Written by Alberto D. Horner*