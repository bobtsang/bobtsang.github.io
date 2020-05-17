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
  - Data staging area
- Date warehouse tier
  - Data marts
  - Metadata repository
- OLAP tier
- Front-end tier: client tools
  - Visualisation
  - Statistical modelling
  - Data mining

### Reference
1. [Designing Data-Intensive Application](https://www.notion.so/bobzeng/Read-Data-Intensive-System-498ff1dc017f4260b5530d10ea89b615)
2. [Apache Kylin](http://kylin.apache.org/docs/gettingstarted/concepts.html)
3. [Druid](https://druid.apache.org/druid.html)
4. [Data Cube: A Relational Aggregation Operator Generalizing
Group-By, Cross-Tab, and Sub-Totals,1997](https://arxiv.org/pdf/cs/0701155.pdf)