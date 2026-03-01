---
title: "Causal Foundation Models - A Benchmark"
date: 2026-01-11T00:00:00-00:00
excerpt_separator: "<!--more-->"
categories:
  - Blog
---
![PEHE-barplot](/assets/images/20260111PEHE-plot.png)
In-context learning is an emergent property of foundation models that raised a lot of excitement when it first became to known.

In simple terms, it allows a model to learn from the data and context available at inference time.

As it turns out, it can also be immensely useful in causal inference.

I decided to test out three major foundation models for causal inference using my personal Windows machine.

The three models are:

- [DoPFN](https://github.com/jr2021/Do-PFN) (Prior Labs and Max Planck Institute)

- [CausalFM](https://github.com/yccm/CausalFM) (LMU Munich and MCML)

- [CausalPFN](https://github.com/vdblm/CausalPFN/) (Toronto and Layer 6 AI)

All three algorithms are built upon TabPFN, a foundational model developed by Prior Labs and originally designed to address the abundance of small tabular datasets.

In this short article, I want to share with you my learnings, assuming that for some of our readers, using these algorithms in a local environment might be far easier and more appealing than managing to get access to an NVIDIA A100.

Here’s what I found.

From the accessibility standpoint, CausalPFN was the easiest one to get running.

A simple “uv add causalpfn” was sufficient to make the model ready for use.

On the other end of the spectrum was Do-PFN.

Despite many hours spent attempting to set it up, I was not able to make it run on my Windows machine.

After many failed attempts, I decided to replace Do-PFN with an S-Learner with TabPFN as the base model.

I focused on CATE estimation and used PEHE (Precision in Estimation of Heterogeneous Effect) to evaluate them.

I generated test datasets using the code available in the CausalFM repo (datasets 1-10) and on the Prior Labs website (dataset 11).

The results are plotted in the figure above (the lower the PEHE, the better the performance).

You can find the numerical values in the table below:

![PEHE-table](/assets/images/20260111-PEHE-table.png)

To play with the code yourself, check the [notebook](https://github.com/HornerAlberto/PFN-Causal-Inference-Benckmark/blob/main/benchmarknotebook.ipynb).