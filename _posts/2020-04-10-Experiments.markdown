---
layout: post
title:  "Experimentation"
date:   2021-01-31 22:00:00 +0800
---
### Introduction

> An experiment is a test or a series of tests.

### History

> Agricultural applications dominated designed experiments for, probably most of the 20s and 30s. It wasn't until World War II that we began to see an expansion of designed experiments into industrial work. And this was largely because of experimental work that went on during the war for developing weapons systems and medical treatments for injuries.

### Principles of Design of Experimentations

- Randomization
    - Running the trials in an experiment in random order
- Replication
    - Independent `repeat run` of each factor combination
    - Sample size
- Blocking

### Guideliness

1. Recognition of and statemetn of problem
2. Selection of the response variable
3. Choice of factors, levels and range
   a. Design factors vs. nuisance factors

4. Choice of experimental design
5. Performing the experiment
6. Statistical analysis of data
7. Conclusions and recommendations

### Factorial Design

> In a factorial experiment, all possible combinations of factor levels are tested

- Fractional Factorial Design

### Goals of experiments

- Reduce time to desgin and develop new products and process
- Improve performance of existing processes


> At the core of the Lean Methodology is the scientific method: Creating hypotheses, running experiments, gathering data, extracting insight and validation or modification of the hypothesis.

Necessary Ingrediants for running user controlled experiments

1. There are experimental units that can be assigned to different variants with no interference.
2. There are enough experimental units.
3. Key metrics, ideally an [OEC](https://learning.oreilly.com/library/view/understanding-experimentation-platforms/9781492038139/ch03.html), are agreed upon and can be practically evaluated.
4. Changes are easy to make.

## The Hypothesis Testing Framework

- Sampling from a normal distribution
- Statistical hypothesis

### Estimation of Parameters

- For example: mean, variance
- Comparative experiment
 - Mean
 - Variance

### Terminologies

- critical value (statistics)
- `reference distribution`
- P-value approach
- Pooled t-test (or Equal Variance t-test), Two-Sample t-Test<sup>10</sup>
    - t<sub>0</sub> serves as signal-to-noise ratio
    - Checking assumptions: normal probability plotting

> In some simple comparative experiments, we can greatly improve the precision by making comparison within matched pairs of experimental material

- Paired t-test
- Power = 1 - $\beta$, in which $\beta$ is the probability of type 2 error (failing to reject default hypothesis)


### Analysis of Variance (ANOVA)

> The name 'analysis of variance' stems from a partitioning of the total variability in the response variable into components that are consistent with a model for the experiment.

Why `ANOVA`

- single factor for more than 2 levels
- more than single factor

`Total variability` = SS<sub>Treatments</sub> + SS<sub>E</sub>
![tree is not for this.use things properly]({{site.baseurl}}/resources/single_factor_anova.png)

Reference distribution is `F` distribution.
We will reject the default H<sub>0</sub> if F<sub>0</sub> > F<sub>a,a-1,a(n-1)</sub>

#### Assumptions

- Normality
- Constant variance
- Independence


#### Model adequacy checking for ANOVA

- Normal probaiblity plot of residuals
- Residual against order or time: should be randomly scattered
- Residual against predicted values/ fitted values: should be randomly scattered


#### Post-ANOVA comparison of means

Which specific means are the particular mean to be different? It's the `multiple comparisons problem`.

- Design-expert output
- Graphical comparison of means
  - sliding the normal distribution curve to see whether the group means would fall into the shape
- The regression model

### Sample Size Determination

Considerations

- What type of experiments
- How it will be conducted
- Desired sensitivity
- Desired `power`

### The Random Effects Model

aka. variance components model, in this type of model, mean is usually not tested but the variance.

Note that `normality assumption` is not needed and it's possible that the estimate of variance can be negative, which is against the nature of variance

### The Blocking Principle

- Blocking and nuisance factors
  - `nuisance factor` may have effect on the response, but it's of no interest to the experimenter
    - If the `nuisance factor` is known and controllable, we can use `analysis of covariance` to remove the effect
    - If the `nuisance factor` is unknown and uncontrollable ("lurking" variable), we hope that randomization balances out its impact across the experiments
  - In general, a `block` is a specific level of nuisance factor, and it represents a `restriction on randomization`. All runs within a block are `randomized`

- RCBD: the randomised complete block design
  - Assumptions
    - Additive model, which means no interactions
  - Statistical model for RCBD: an extension of ANOVA
  - SS<sub>T</sub> = SS<sub>Treatments</sub> + SS<sub>Blocks</sub> + SS<sub>E</sub>
  - If we do not do RCBD, then the variance of error term will be inflated
  - Random Blocks and/or Treatments
  - The Latin Square Design
    - simultaneously control two sources of nuiance variability
    - Assumption: three factors (treatments, nuisance factors) do not interaction

## Reference

[1] Trustworthy Online Controlled Experiments, 2020  <br>
[2] [Awesome User Testing](https://github.com/augbog/awesome-user-testing) <br>
[3] [Beyesian Machine Learning in Python: A/B Testing](https://www.udemy.com/course/bayesian-machine-learning-in-python-ab-testing/) <br>
[4] Statistics for Experimenters: Design, Innovation, and Discovery, 2nd Edition <br>
[5] Bandit Algorithms, Tor Lattimore, Csaba Szepesvári,2020 <br>
[6] Understanding Experimentation Platform, Adil Aijaz, 2018 <br>
[7] [It's all about testing: the Netflix Experiment Platform](https://netflixtechblog.com/its-all-a-bout-testing-the-netflix-experimentation-platform-4e1ca458c15) <br>
[8] [Design of Experiments, Coursera Specialisation](https://www.coursera.org/learn/introduction-experimental-design-basics/lecture/8IrTw/history-of-dox) <br>
[9] [How Ronald A. Fisher’s work feeds into statistical engineering, Lynne B. Hare, 2019](https://www.notion.so/bobzeng/Statistics-Spotlight-The-Foundation-of-Statistical-Engineering-5958806bcaf64ca680e1aab90f8b2ccb) <br>
[10] [The two-sample t Test,JMP tech doc](https://www.jmp.com/en_hk/statistics-knowledge-portal/t-test/two-sample-t-test.html) <br>
[11] [Wiki:AB Testing](https://www.wikiwand.com/en/A/B_testing) <br>
[12] Design and Analysis of Experiments, Douglas C. Montgomery, 2017 <br>
[13] [What's the difference between a randomized block design and two factor design, Cross Validated, StackExchange](https://stats.stackexchange.com/questions/236573/whats-the-difference-between-a-randomized-block-design-and-two-factor-design/312736#:~:text=With%20the%20randomized%2Dblock%20design,levels%20of%20the%20blocking%20variable.&text=In%20a%20two%2Dway%20factorial,cells%20of%20the%20factorial%20design.)
