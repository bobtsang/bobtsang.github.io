---
layout: post
title:  "Learn Data Engineering"
date:   2020-03-18 22:00:00 +0800
---


## Data warehouse

Here is the [separate page](https://bobtsang.github.io/2020/04/28/Data-Warehousing.html) for this topic.

## Data Lake

## Data Lakehouse <sup>4</sup>
  - Metadata layers for data lakes
  - New query engine designs providing high-performance SQL execution on data lakes
  - Optimised access for data science and machine learning tools

## Data Mesh

> The data platform version of microservices

- Domain Driven Design and each domain handles their own data pipeline
- An universal layer with same syntax and data standards

Key topics of a data mesh including

```
Encryption for data at rest and in motion
Data product versioning
Data product schema
Data product discovery, catalog registration, and publishing
Data governance and standardization
Data production lineage
Data product monitoring, alerting, and logging
Data product quality metrics
```

## Batch Data Processing

## Streaming Data Processing

### Layering of Streaming Data

- ODS: raw data from production DB

### Case Study for Streaming Data

#### Business Intelligence

When calculating deduplicated metrics, e.g. distinct count, the following techniques should be considered <sup>2</sup>

1. Bloom Filter
   - The requirement for precision is not that high
2. Modelling based on historical data

## Reference

1. Streaming Architecture, 2016, Ted Dunning and Ellen Friedman
2. 大数据之路：阿里巴巴大数据实践，2017
3. Designing Data Intensive Application, 2017, Martin Kleppmann
4. [Data Lakehouse: Simplicity, Flexibility and Low Cost](https://databricks.com/glossary/data-lakehouse#:~:text=A%20data%20lakehouse%20is%20a,(ML)%20on%20all%20data.)
5. [Kappa Architecture](http://milinda.pathirage.org/kappa-architecture.com/)
6. [What is a Data Mesh](https://towardsdatascience.com/what-is-a-data-mesh-and-how-not-to-mesh-it-up-210710bb41e0)
7. [Data Mesh Applied](https://towardsdatascience.com/data-mesh-applied-21bed87876f2)
8. [Data Monolith to Mesh](https://martinfowler.com/articles/data-monolith-to-mesh.html)
9. [Data Mesh Principles and Architecture](https://martinfowler.com/articles/data-mesh-principles.html)