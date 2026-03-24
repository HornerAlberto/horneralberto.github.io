---
title: "Counterfactual Fairness: take as much as you can"
date: 2026-03-22T00:00:00-00:00
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

![counterfactual-fariness-model](/assets/images/20260321-CounterfactualFairness-StandardFairnessModel.png)

*Originally published in* [*Causal Python weekly*](https://causalpython.io/).
*Sign up and get up-to-date coverage of Causal AI for free.*

**Counterfactual Fairness**
In fairness research we often talk about so-called sensitive attributes.

Two popular examples are gender and race.

We typically wish to prevent these attributes from playing a role in settings such as credit lending or recidivism prediction.

Would the bank have approved the credit had person X been male rather than female?

Counterfactual Fairness (CF) is achieved when the prediction for an individual is the same as that in a counterfactual world with a different value for a given sensitive attribute.



**The challenge**

But here's the challenge:

How to prevent a given sensitive attribute from influencing our predictions?

If we remove it from the dataset, the model could be implicitly inferring it based on other attributes.

Another option could be to set that variable to a different value, but that wouldn’t be a valid counterfactual, since other attributes are also affected by the sensitive ones.

Furthermore, there is a trade-off: CF usually comes at the expense of accuracy.

For the CFO of a bank, lowering accuracy by 2% means losing 2% of revenue.

If a bank gives up too much accuracy, it could go bankrupt and end up incapable of lending credit to anyone.



**A brand-new Counterfactual Fairness estimation model**

In a brand-new paper, Yuchen Ma, Valentyn Melnychuk and colleagues (MCML at LMU), present A Consistent End-to-End Estimation for Counterfactual Fairness.

The authors train a Generative Adversarial Network (GAN) called the Generative Counterfactual Fairness Network (GCFN), which ensures counterfactual fairness with theoretical guarantees in a tailored fashion.

Their approach follows the Standard Fairness Model, which assumes a causal graph with the structure presented in *Figure 1* above.

The focus lies on mediators because those variables capture the entire influence of the sensitive attribute and its descendants on the target. Thus, this method removes information from the sensitive attribute while keeping remaining useful information to maintain high performance.



**The trade-off parameter**

There is a lemma presented in the paper on how a Counterfactual Mediator Regularization effectively forces the predictor to be more counterfactually fair.

Moreover, the authors introduce a weight parameter λ that defines how much regularization affects the overall model.

This way, it is possible to balance the trade-off between counterfactual fairness and performance.



**Enabling decisions**

The following plot shows how accuracy and counterfactual fairness change for one of the analyzed datasets:

![counterfactual-fariness-weight](/assets/images/20260321-CounterfactualFairness.png)


Let’s say that our CFO considers it unacceptable to give up more than 0.0075 of accuracy. Then, it is possible to choose a fairness weight (say, λ=0.6) that maximizes CF under the given constraints:

![counterfactual-fariness-sweet-spot](/assets/images/20260321-CounterfactualFairnessSweetSpot.png)


**Alberto's verdict**

Definitely, a significant step towards Responsible AI.

Written by Alberto D. Horner

[Explore the paper](https://arxiv.org/pdf/2310.17687)


[Explore the code](https://github.com/yccm/consistent-estimation-gcfn)