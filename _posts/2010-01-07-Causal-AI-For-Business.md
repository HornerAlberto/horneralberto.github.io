---
title: "Causal AI for Business: the next breakthrough"
excerpt_separator: "<!--more-->"
categories:
  - Blog
---

## Beyond association

Most of the widespread Machine Learning algorithms are based on purely statistical methods. They are based
on the dependence between available data and a target variable (or set of variables). For instance, a drivers
app algorithm collects data from other users’ trajectories and outputs the probably fastest path for you to
drive through. In those cases, purely statistical algorithms are perhaps the best approach you can have.

Now, think about a second example: a company that wants to evaluate whether a marketing campaign was
successful or not. They may find an association between the marketing campaign and an increase in sales; they
may also have achieved the purported goals on their sales and revenue, which are the reason why they launched that marketing
campaign. Therefore, they dare to conclude that the marketing campaign was successful. Should they run that campaign again next year? In these cases, Causal AI is surely a better approach.

The main difference between the former and the later example is that the former is looking for optimization,
while the later is looking for a decision rule. Drivers do not have control over the streets. They’ll pick
always the quickest path. On the other hand, business leaders do have control over marketing campaigns. Then,
before deciding to relaunch the same campaign, it would be nice to know that the increase in sales they’ve observed was,
in fact, due to the campaign. They can intervene in the situation in order to achieve their goals. And that’s the point with causal AI: it takes a step beyond association and deals with interventional and counterfactual data.

The main idea in causal reasoning is condensed in the ladder of causation, an analogy that tells that you can
ascend into a more structural knowledge than the associative one. There are three kinds of causal knowledge,
which can be mapped to three kinds of questions. The first kind is associative knowledge: was the increase in sales associated
with our marketing campaign? The second kind is interventional knowledge: what if we relaunch the campaign? Will it yield the same results? The third kind is counterfactual: what would have happened if we hadn’t launched that campaign? Would sales have increased anyway? The second and third levels can only be reached using causal reasoning (or simulating it), and that is the kind of information that managers really want to have.


![LadderOfCausation](/assets/images/the-ladder-of-causation.png)

*The Ladder of Causation. A drawing by Maayan Harel.*


## It’s a business thing

Causal AI has its own history as a scientific project. Judea Pearl must be noted as the scientist who laid out the sound foundations of causal inference; his book Causality: Models, Reasoning and Inference is now a canonical book. But what about causal AI as a business project?

Currently, the leading project for developing causal AI applications is pywhy, a python library that emerged from the joined efforts of Microsoft and Amazon research. We may focus on that project to determine the current state of causal AI for business. A good approach to take is that of Hurwitz and Thompson.

Judith S. Hurwitz and John K. Thompson recently published a book titled Causal Artificial Intelligence: The Next Step in Effective Business AI. They assess innovative software as a process that takes, at least, three iterations: “The first iteration proves that the idea will work. The second attempt refines the approach and implementation, and the third round of work standardizes, hardens, and builds software that is reliable, robust, and scalable.” They depict these three steps as the beginning of a continuous improvement process. Most important of all, they say that “the causal AI software market is in the process of moving past the three-cycle model”. In other words, we know that causal AI tools work well, but they are also at their very beginning inside the business world, in such a way that they may be a competitive advantage for innovators.

In their book, Hurwitz and Thompson also warn that Causal AI tools have a long way to walk. “The software that is the basis of causal AI market needs to evolve, it is too hard to use, it has functional gaps, and it is not robust enough for reliable enterprise-class use today.” If you are a business leader, these are good news. It means that you still have time to get prepared for the next industrial breakthrough of AI.


## Take a look into the causal levels

Let’s dive deeper into the previous example. Ideally, a good marketing campaign produces an increase in sales. But how could I know if the increase in sales that I have observed was produced by the campaign? Was it perhaps just coincidence and other factors were responsible for that increase? A causal analysis can tell the answer and provide guidelines to keep those increasing results. It is essentially actionable.

You may wonder why a mere plot of sales and revenue before and after the marketing campaign won’t work. Usually, business decisions are not taken in isolation. Around the same lapse of time, the pricing team may have changed their strategy, and the engineers may have come up with a more ergonomic design. It is possible to discover that the last two caused the increase in sales, and not the first one. A causal diagram of the situation looks as follows:

![Example Graph](assets/images/the-ladder-of-causation.png)

That would mean that the marketing campaign needs a change and that, at least for this hypothetical company, it will be better to focus efforts on design and pricing. While performing the analysis, your team may discover insightful relations among variables, like the role of customer satisfaction as a mediator between the quality of the product’s design and the number of sales (look at the diagram). Furthermore, your causal model will enable you to answer questions like ‘what is the best way to allocate our budget to maximize sales?’ Obviously, assuming that budget allocation has a causal effect on design improvement and pricing optimization. Achieving those results is feasible with the current state of causal AI.


## The meaning of this breakthrough

Four years ago, Regina Barzilay, MIT professor whose research has focused on early cancer diagnosis, was asked how far we are from understanding the human body’s biology or some of its diseases, from the perspective of computer science. “One of the reasons that we succeeded in the areas that we as a computer scientists succeeded,” she said, “is that we are not trying to understand in someways. If you think about e-commerce: Amazon doesn´t really understands you, and that’s why it recommends you certain book or certain products, correct? \[…\] If you look on what they do with the recommendation system, they are not claiming that they´re understanding something. They’re just managing to, from patterns of human behavior, recommend you a product.”

Nowadays, then, it may sound surprising that Amazon is part of the pywhy project. The next step in AI is about achieving a better understanding. Think about a movie recommendation algorithm; two users may have watched the same set of movies. A traditional algorithm would recommend them the same set of movies. A causal algorithm, instead, might detect that the reason one user chose those movies was the soundtrack, photography, and all other aesthetic details, while the other user was captivated mainly by the plots, therefore the causal algorithm will recommend different and more adequate set of movies to each user.

Amazon and Microsoft know that causal AI is profitable. But there are more reasons to implement causal AI, like ethical compliance and side-effects prevention. For instance, there is interesting work on algorithmic fairness and accountability for the sake of preventing gender and race bias. Also AI will be much more useful to fight climate crisis if it is enhanced with causal reasoning. It is a field of research and development where we can strive to align technological growth with human goals and make money on the road.