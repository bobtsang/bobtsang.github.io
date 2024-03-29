---
layout: post
title:  "Business Intelligence"
date:   2020-03-18 22:00:00 +0800
---

## Business Intelligence Overview

It has been a hot topic as data sceince being a growing discipline <sup>18</sup>.


## Major topics for Business Intelligence

### Single source of truth

- Engineering: data is updated accurately on time

  - Update Pattern: realtime, batch; full dump, incremental
  - Query Optimisation: depends on platform

- Documentation

### Analytics


### Data Warehouse

Aka, enterprise data warehouse (EDW)， current and historical data in one single place, which will provide single source of truth.


- Operational system
This is a term referred to a system that is used to process day-to-day transactions of an organisation in data warehousing.Similar terms are OLTP (online transaction processing sytems)

- ODS
Operational data store is used for operational reporting and as a source for the data warehouse. And generally speaking, it's used for operational decision making, in contrast of EDW, which is used for tactical and strategic decision support. Taking data from multiple sources of operational systems, ODS loosely integrates them together with no feeding back to operational systems.

- EDH (Enterprise Data Hub)

![tree is not for this.use things properly]({{site.baseurl}}/resources/different-layers-in-data-warehouse-architecture.png)

### ETL

- Staging: Intermediate storage area to increase the efficiency of ETL process
- Data integration
- Data dictionary

> centralized repository of information about data such as meaning, relationships to other data, origin, usage, and format

## Business Intelligence Concepts

### CDC: Change Data Capture

### SCD: Slowly Changing Dimension

There are 6 types of methodologies to deal with SCD.

0. retain original
1. overwrite
2. add new row
3. add new attribute
4. add history table
5. type 4 + type 1
6. combined type

### OLAP vs.OLTP vs. HTAP

Traditionally speaking, `OLTP` is more likely to be a row-based storage engine, supporting high concurrency and strong consistency. Each request modifies no more than few rows of data.
And `OLAP` is likely to be a columnar databases, in which we can process batch historical information.


## Business Intelligence Platform

In this section, I would like to compare the BI platforms I have used. In general, BI platform should be considered as the components in serving layer in Lambda or Kappa architecture.

### Tableau

#### Data Source

#### Data Catalog and Governance

### Looker

#### LookML

#### Explore

#### Online Support

## Reference

1. [Data Engineering Cookbook](https://github.com/andkret/Cookbook)
2. [Awesome Data Engineering](https://github.com/igorbarinov/awesome-data-engineering)
3. [Awesome Business Intelligence](https://github.com/thenaturalist/awesome-business-intelligence)
4. [Data Warehouse](https://www.wikiwand.com/en/Data_warehouse)
5. [Designing Data Intensive Application](https://dataintensive.net/)
6. [OLAP](https://www.wikiwand.com/en/Online_analytical_processing)
7. [Dimensional Modelling](https://www.wikiwand.com/en/Dimensional_modeling)
8. [Beyond Data Warehousing:What’s Next in Business Intelligence?,2004](https://dl.acm.org/doi/pdf/10.1145/1031763.1031765)
9. [How to Track State with Type 2 Dimensional Models](https://engineering.shopify.com/blogs/engineering/track-state-type-2-dimensional-models)
10. [Star Schema the Complete Reference, 2010, Christopher Adamson](https://learning.oreilly.com/library/view/star-schema-the/9780071744324/ch00fm6.html)
11. [The Data Warehouse Toolkit, Margy Ross, Ralph Kimball, 2013](https://learning.oreilly.com/library/view/the-data-warehouse/9781118530801/9781118530801c00.xhtml)
12. [Airflow Concept](https://airflow.readthedocs.io/en/stable/concepts.html)
13. [dbt:data build tool](https://docs.getdbt.com/docs/introduction)
14. [What is ETLT](https://www.xplenty.com/blog/what-is-etlt/)
15. Business intelligence guidebook: from data integration to analytics, Rick Sherman, 2015
16. [How We Build an HTAP Database That Simplifies Your Data Platform, Shawn Ma](https://pingcap.com/blog/how-we-build-an-htap-database-that-simplifies-your-data-platform)
17. [TiDB:A distributed SQL Database](https://github.com/pingcap/tidb)
18. [Business Intelligence vs. Data Science, 2021, Matt Przybyla](https://www.notion.so/bobzeng/Data-Science-vs-Business-Intelligence-Differences-Towards-Data-Science-2019647dee41400b8bd2948025f6e7d9)
19. [Crow's Foot Notation](https://www.vertabelo.com/blog/crow-s-foot-notation/)
20. [My Looker Notes](https://www.notion.so/bobzeng/Looker-a9e8c954e60043f293df1dd7cf186858)
21. [Looker: Looker vs. Tableau](https://looker.com/compare/looker-vs-tableau)