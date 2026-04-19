---
title: "Personalized Decision Making"
date: 2026-04-19T00:00:00-00:00
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

![p-harm-p-benefit](/assets/images/20260419-PersonalizedDecisionMaking.png)

*Originally published in* [*Causal Python weekly*](https://causalpython.io/).
*Sign up and get up-to-date coverage of Causal AI for free.*



**What Matters to You, Individually**

A growing field of study within causal inference is personalized decision-making.

While population-based decision-making concerns a subpopulation resembling a given individual, this area of study includes your individual beliefs and priorities as part of the analysis, that is, what matters particularly to you.

Personalized decision-making focuses on Individual Treatment Effects (ITEs), which are measured by the difference between control and treatment outcomes for a given individual.


Two important caveats for ITEs are:

1. In general, they are not point-identifiable.

2. From the estimation standpoint, ITE will be the same for all individuals that share the same measured attributes.


Even so, once we consider causal effects at the individual level, we open the door to include distinct beliefs and utility functions for every individual.

For high-stakes scenarios like medical applications, this approach turns out to be considerably advantageous compared to subpopulation approaches such as Conditional Average Treatment Effect (CATE) optimization.


**A crucial moment for ITEs**

Personalized decision-making has been motivated by medical applications.

Healthcare is estimated to be globally a $14 trillion market, as Nate Gross, Head of Health at OpenAI, said in [a recent podcast by The Economist](https://www.economist.com/podcasts/2026/04/02/can-ai-fix-health-care).

In that podcast, he focuses on the potential of GenAI for Health on information availability, patient awareness, and process automation. As far as I see, there are no theoretical guarantees on individual alignment for those applications.

With personalized decision-making, we are talking about something entirely different.

It means suspending the assumption that the physician knows what is personally important to the patient and enables an approach that includes all individual circumstances.


**The probability of harm**

Two events that turn out to be of particular interest are harm and benefit.

For different individuals pertaining to the same subpopulation, the same drug might save one of them and doom the other.

The probability of harm is nothing but the probability for a given individual to get an undesired outcome under treatment that would not have been observed without the treatment.

Formalizing the probabilities of these events allows us to further investigate how to leverage the effectiveness of a drug and avoid its undesired effects.

In [a recent paper](https://ftp.cs.ucla.edu/pub/stat_ser/r513.pdf), Scott Mueller and Judea Pearl present an example where the effectiveness of a decision strategy is raised from 28% to 62% due to this personalized approach.


**State of the art**

Conceptually, probabilities of harm and benefit, along with personalized decision making, are tightly related to the probabilities of necessity and sufficiency.

The following are three non-exhaustive important references in the field:

1. Judea Pearl’s book Causality (Chapter 9) presents theoretical bounds for individual-level probabilities.

2. In 2000, Jin Tian and Judea Pearl published [a paper on how to define bounds for probabilities of necessity and sufficiency](https://ftp.cs.ucla.edu/pub/stat_ser/r271-A.pdf) by combining experimental with non-experimental data.

3. In addition to many published papers ([2022](https://ftp.cs.ucla.edu/pub/stat_ser/r505.pdf), [2023](https://ftp.cs.ucla.edu/pub/stat_ser/r513.pdf), [2025](https://academic.oup.com/aje/article/194/6/1749/7909739)), Scott Mueller (UCLA) wrote a PhD dissertation on [“Personalized and situation-specific Decision Making”](https://scott.am/dissertation.pdf), this is, as far as I know, the most comprehensive resource on the topic.

*Written by Alberto D. Horner*

