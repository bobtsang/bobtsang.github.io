---
layout: post
title:  "Causality in Time Series"
date:   2020-03-06 22:00:00 +0800
---
This is for summarizing theories and implementation of modelling causality in time series data.

### Causal relationship in time series

Mainly two schools of thoughts

- Classical time series modelling

- Dynamic system and information theory 

#### Types of causality

- Granger causality
- Instantaneous causality
- Multi-step causality

  - bivariate system: 1-step ahead forecasts 
  - multi-variate system: X <sub>i</sub> is h-step causal for another variable Y<sub>i</sub>

- Sims causality

  - Granger causality will lead to Sims causality but the other way around may not be true

- Structural causality
 
  - recursive dynamic structure in data generation process
  - predecessors <b>structurally</b> determine successors

- Intervention causality

  - related to [impulse response](https://www.wikiwand.com/en/Impulse_response) in econmetrics 

#### Causality Inference in time series data

- Non-directional lagged interactions
  - Lagged version of X causes Y
    - high degree of correspondence
    - correspondence measure
      - pearson correlation
        - it's equivalent to looking at the [cross-correlation](https://www.wikiwand.com/en/Cross-correlation) function. this can lead to significant problems when interpretating.
      - mutual information

- Parametric VAR-based tests for Granger causality
  - Stationarity,differencing
  - restricted model: assuming Y only depends linearly only on its past values
  - unrestricted model: Y depends past values of both X and Y. [Granger Test](https://www.statisticshowto.datasciencecentral.com/granger-causality/), another example of [bivariate Granger Causality test](https://support.sas.com/rnd/app/ets/examples/granger/index.htm)
  - [statsmodels function](https://www.statsmodels.org/stable/generated/statsmodels.tsa.stattools.grangercausalitytests.html#statsmodels.tsa.stattools.grangercausalitytests)

#### Causality Inference In Information Theory

- Coarse-grained tras-information rate (CTIR)
- Transfer entropy measures 
- Mutual Information from Mixed Embedding (MIME)

#### Causality Inference In Graphical Modelling

- causal Markov condition: SGS, PC and FCI
  main structure for these algorithm
  1. initialization
  2. skeleton construction: testing for conditional independence 
  3. edge elimination
- PCMCI: [repo](https://github.com/jakobrunge/tigramite)
- Copula-Granger

#### When to Use What

1. When to use Granger

   - Separability

   Data needs to be separated into several mutually-exclusive time series. If this condition could not be met, then modern approaches like PCMCI would be more appropriate.
   
   > information about causing effects is not contained in the time series for the caused effects

2. Parametric vs Non-Parametric


#### Reference

1. [Learning notes](https://www.notion.so/bobzeng/Time-Series-de89af1b5fa04d8690ab90b39c62548c)
2. [Causality: Statistical Perspectives and Applications](https://onlinelibrary.wiley.com/doi/book/10.1002/9781119945710), Carlo Berzuini etc., 2012
3.Inference and Causality in Economic Time Series Models, John Geweke
