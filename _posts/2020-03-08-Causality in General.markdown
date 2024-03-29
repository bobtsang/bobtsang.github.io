---
layout: post
title:  "Causality in General"
date:   2020-12-27 19:46:07 +0800
---
When A and B are dependent, there are three possibilities of their relationship

1. A causes B
2. B causes A
3. Something else causes A and B


What is [causal graph](https://www.wikiwand.com/en/Causal_graph)?

> a causal diagram is a Bayesian network in whic every arrow signifies a direct causal relation, or at least the possibility of one, in the direction of that arrow. --- Judea

#### Terminology

##### Confounding and Confounders

> A confounder is a variable that influences both the dependent and independent variable, causing a spurious association.

![Confounder]({{site.baseurl}}/resources/confounder.png)


How to identify confoudners?

To control confounder, a simple and widely-used approach is `stratification`, which is bucketting based on values of the confounders.

##### Structure Learning

##### Causal Discovery

##### SEM: Structural Equation Modelling

It's an integration of the following <sup>10</sup>

- Measurement theory
- Factor (latent variable) analysis
- Path analysis
- Regression
- Simultaneous equations

#### Reference

[1] [User Causal Graph!](https://towardsdatascience.com/use-causal-graphs-4e3af630cf64) <br>
[2] [Awesome Causality](https://github.com/napsternxg/awesome-causality) <br>
[3] [Awesome Causality Algorithm](https://github.com/rguo12/awesome-causality-algorithms) <br>
[4] [Awesome Causality Data](https://github.com/rguo12/awesome-causality-data) <br>
[5] [Causal Inference in Computer Science](https://www.wikiwand.com/en/Causal_inference#:~:text=Causal%20inference%20is%20the%20process,when%20the%20cause%20is%20changed.)<br>
[6] [What is causal inference and why should data scientists know? by Ludvig Hult](https://www.youtube.com/watch?v=dFp2Ou52-po&ab_channel=PyConSweden) <br>
[7] [A Critical View of the Structural Causal Model](https://arxiv.org/pdf/2002.10007.pdf) <br>
[8] [Differentiable Causal Discovery Under Unmeasured Confounding](https://arxiv.org/pdf/2010.06978.pdf) <br>
[9] [Introduction to Structural Equation Modelling](http://statmath.wu-wien.ac.at/courses/StatsWithR/Topic-5.pdf) <br>
[10] [Video: What is structural equation modelling](https://www.youtube.com/watch?v=Flqbo8J3li4&ab_channel=Geek%27sLesson) <br>
[11] [From how to why: An overview of causal inference in machine learning](https://www.notion.so/bobzeng/Overview-of-causal-inference-machine-learning-Ericsson-27f2619637b3411e9edd1155d7ba399b) <br>
[12] [CausalML:A Python Package for Uplift Modeling and Causal Inference with ML](https://github.com/uber/causalml)
[13] Causality:Statistical Perspectives and Applications, Carlo Berzuini, Philip Dawid, Luisa Bernardinell, 2012 <br>
[14] Elements of Causal Inference, Jonas Peters, Dominik Janzing, and Bernhard Scho ̈lkopf, 2017 <br>
[15] [Paper notes by Vitaly Kurin](https://www.notion.so/bobzeng/Paper-Notes-by-Vitaly-Kurin-4a844b30f73b4247ab74b0436a01b8ce) <br>
[16] [Discussion:'The Scientific Model of Causality', Michael E. Sobel](https://www.notion.so/bobzeng/DISCUSSION-THE-SCIENTIFIC-MODEL-OF-CAUSALITY-3e9cf563a8ff4beba3b00800a36ba312)<br>
[17] [Causal Inference: Mixed Tape](https://mixtape.scunning.com/index.html)<br>
[18] [Introduction to Causal Inference: from Machine Learning Perspective](https://www.notion.so/bobzeng/Introduction-to-Causal-Inference-from-Machine-Learning-Perspective-3e7ad2192a144882b33221173c6fe4fb)<br>
[19] [How to Use Causal Inference In Day-to-Day Analytical Work](https://towardsdatascience.com/how-to-use-causal-inference-in-day-to-day-analytical-work-part-1-of-2-b5efbdbf8ab0), Rama Ramakrishnan, 2019
[20] [Controlling Confounding Bias](http://bayes.cs.ucla.edu/BOOK-2K/ch3-3.pdf)