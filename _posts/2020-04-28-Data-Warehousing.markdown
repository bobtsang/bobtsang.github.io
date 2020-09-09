---
layout: post
title:  "Data Warehousing"
date:   2020-04-28 22:59:07 +0800
---
### Data Warehouse Concepts

- Multi-dimensional data cube
![tree is not for this.use things properly]({{site.baseurl}}/resources/data-cube.png)
  - **Dimensions** are perspective used to analyze the data.
  - **Dimensional level** means granularity.
  - **Facts** are associated with numberical measures.

### Data Warehouse Architecture

- Backend tier
  - ETL process
    - Extraction:API/ODBC/JDBC
    - Transformation
      - Cleaning
      - integration: schema and data
    - Loading
      - Refreshing
  - Data staging area
- Date warehouse tier
  - Data marts
  - Metadata repository
    - Business metadata
      - meaning (or semantics) of the data
      - organizational rules
      - constraints related to the data
    - Technical metadata
      - how is it structured or organised
      - ETL process: data lineage, cleaning rules

- OLAP tier
  - XMLA: XML for analysis
  - MDX: MultiDimensional eXpressions
- Front-end tier: client tools
  - Visualisation
  - Statistical modelling
  - Data mining

### Hierarchy Design

- Balanced Hierarchies

> has only one path at the schema level, where all levels are mandatory.

- Unbalanced Hierarchies
- Generalised Hierarchies

### Reference

1. [Designing Data-Intensive Application](https://www.notion.so/bobzeng/Read-Data-Intensive-System-498ff1dc017f4260b5530d10ea89b615)
2. [Apache Kylin](http://kylin.apache.org/docs/gettingstarted/concepts.html)
3. [Druid](https://druid.apache.org/druid.html)
4. [Data Cube: A Relational Aggregation Operator Generalizing
Group-By, Cross-Tab, and Sub-Totals,1997](https://arxiv.org/pdf/cs/0701155.pdf)
5. Data Warehouse System: Design and Implementation, 2014, Alejandro Vaisman etc.
6. [Semantic data model](https://www.wikiwand.com/en/Semantic_data_model)
7. [Hadoop vs MPP](https://0x0fff.com/hadoop-vs-mpp/)
