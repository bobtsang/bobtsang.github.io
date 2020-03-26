---
layout: post
title:  "Time Series"
date:   2020-03-06 22:00:00 +0800
---
### VAR

### Causal relationship in time series

Mainly two schools of thoughts

- Classical time series modelling

- Dynamic system and information theory 

#### Types of causality

- Granger causality
- Instantaneous causality
- Multi-step causality

  - bivariate system: 1-step ahead forecasts 
  - multi-variate system: X <sub> i</sub> is h-step causal for another variable Y<sub>i</sub>

- Sims causality

  - Granger causality will lead to Sims causality but the other way around may not be true

- Structural causality
 
  - recursive dynamic structure in data generation process
  - predecessors <b>structurally</b> determine successors

- Intervention causality

  - related to [impulse response](https://www.wikiwand.com/en/Impulse_response) in econmetrics 

### Reference

1. [Learning notes](https://www.notion.so/bobzeng/Time-Series-de89af1b5fa04d8690ab90b39c62548c)
2. [Causality: Statistical Perspectives and Applications](https://onlinelibrary.wiley.com/doi/book/10.1002/9781119945710), Carlo Berzuini etc., 2012
