---
layout: post
title:  "Data Engineering and Business Intelligence Engineering"
date:   2020-03-18 22:00:00 +0800
---


#### Data Warehouse

Aka, enterprise data warehouse (EDW)， current and historical data in one single place, which will provide single source of truth.

##### Upsteam sources

- Operational system
This is a term referred to a system that is used to process day-to-day transactions of an organisation in data warehousing.Similar terms are OLTP (online transaction processing sytems)

- ODS
Operational data store is used for operational reporting and as a source for the data warehouse. And generally speaking, it's used for operational decision making, in contrast of EDW, which is used for tactical and strategic decision support. Taking data from multiple sources of operational systems, ODS loosely integrates them together with no feeding back to operational systems.

- EDH (Enterprise Data Hub)

##### ETL

    - Staging: Intermediate storage area to increase the efficiency of ETL process
    - Data integration
    - Data dictionary

    > centralized repository of information about data such as meaning, relationships to other data, origin, usage, and format
        

#### Reference

1. [Data Engineering Cookbook](https://github.com/andkret/Cookbook)
2. [Awesome Data Engineering](https://github.com/igorbarinov/awesome-data-engineering)
3. [Awesome BI Engineering](https://github.com/thenaturalist/awesome-business-intelligence)
4. [Data Warehouse](https://www.wikiwand.com/en/Data_warehouse)
5. [Designing Data Intensive Application](https://dataintensive.net/)
6. [OLAP](https://www.wikiwand.com/en/Online_analytical_processing)
7. [Dimensional Modelling](https://www.wikiwand.com/en/Dimensional_modeling)