---
layout: post
title:  "Business Intelligence Engineering"
date:   2020-03-18 22:00:00 +0800
---

#### Major topics for Business Intelligence

##### Single source of truth

- Engineering: data is updated accurately on time

  - Update Pattern: realtime, batch; full dump, incremental
  - Query Optimisation: depends on platform

- Documentation

##### Analytics


#### Data Warehouse

Aka, enterprise data warehouse (EDW)， current and historical data in one single place, which will provide single source of truth.


- Operational system
This is a term referred to a system that is used to process day-to-day transactions of an organisation in data warehousing.Similar terms are OLTP (online transaction processing sytems)

- ODS
Operational data store is used for operational reporting and as a source for the data warehouse. And generally speaking, it's used for operational decision making, in contrast of EDW, which is used for tactical and strategic decision support. Taking data from multiple sources of operational systems, ODS loosely integrates them together with no feeding back to operational systems.

- EDH (Enterprise Data Hub)

![tree is not for this.use things properly]({{site.baseurl}}/resources/different-layers-in-data-warehouse-architecture.png)

##### ETL

- Staging: Intermediate storage area to increase the efficiency of ETL process
- Data integration
- Data dictionary

> centralized repository of information about data such as meaning, relationships to other data, origin, usage, and format

#### Business Intelligence Concepts

##### CDC: Change Data Capture

##### SCD: Slowly Changing Dimension

There are 6 types of methodologies to deal with SCD.

0. retain original
1. overwrite
2. add new row
3. add new attribute
4. add history table
5. type 4 + type 1
6. combined type

#### Reference

1. [Data Engineering Cookbook](https://github.com/andkret/Cookbook)
2. [Awesome Data Engineering](https://github.com/igorbarinov/awesome-data-engineering)
3. [Awesome BI Engineering](https://github.com/thenaturalist/awesome-business-intelligence)
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
