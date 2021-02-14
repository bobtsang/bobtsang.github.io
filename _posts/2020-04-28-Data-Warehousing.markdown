---
layout: post
title:  "Data Warehousing"
date:   2020-04-28 22:59:07 +0800
---
## Goals of Data Warehousing and BI

> Business users want to separate and combine analytic data in endless combinations

- Make information easily accessible <sup>11</sup>
  - Must be intuitive
  - Must be obvious to business users, not merely developer
  - Should mimic business users' thought processes and vocabulary
  - > Simple and fast
- Present information consistently
  - Must be credible: cleaned, quality assured and released only when it is fit for user consumption
  - Common labels and definitions for contents are used across data sources
- Adapt to change
- Must present information in a timely way
- Foundation for improved decision making

## Data Warehouse Concepts

- Multi-dimensional data cube
![tree is not for this.use things properly]({{site.baseurl}}/resources/data-cube.png)
  - **Dimensions** are perspective used to analyze the data.
  - **Dimensional level** means granularity.
  > In many ways, the data warehouse is only as good as the dimension attributes
  - **Facts** are associated with numberical measures.

## Data Warehouse Methodologies

- Kimball
- Inmon
- Data Vault

## Data Warehouse Architecture

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

![BI architecture]({{site.baseurl}}/resources/kimball_bi_architecture.png)

### Hierarchy Design

- Balanced Hierarchies

> has only one path at the schema level, where all levels are mandatory.

- Unbalanced Hierarchies
- Generalised Hierarchies

### Basic Fact Table Techniques

> At the lowest grain, a fact table row corresponds to a measurement event and vice versa

- Additive
- Semi-additive facts
  - Balance
- Non-additive facts

### Basic Dimension Table Techniques

#### Dimension Table Structure

> Every dimension table has a single primary key column

Dimension tables are usually wide, flat denormalised tables with many low-cardinality text attributes.

#### Dimension Surrogate Keys

Highlight points

- Primary key cannot be the operational system's natural key.
- Natural keys for a dimension may be created by more than one source system.


#### Enterprise Data Warehouse Bus Architecture

> Delivering integration via standardised conformed dimensions
> Architectural framework which can help decomposing the program to managable agile implementations

#### Enterprise Data Warehouse Bus Matrix

> Rows are processes and columns are dimensions

#### Dealing with Slowly Changing Dimension (SCD) Attributes

1. Type 0: Retain original; typical for data dimension
2. Type 1: Overwrite
3. Type 2: Add new row
     A minimum of three additional columns should be added <br>
      a. row effective datetime <br>
      b. row expiration date <br>
      c. current row indicator <br>
4. Type 3: Add new attribute: 'alternative reality'
5. Type 4: Add mini-dimension

   > And Business Customers can ask for these type of Slicing Attributes more frequently, so this is obvious that we should not put these slicing attributes in Aggregate table, rather we should create another dimension with only slicing attributes and store foreign key into its Original Dimension and Aggregate Table. This will give more flexibility to Data Model we can cope up with frequent ask for different slicing Attributes in the report.

   > If we check cardinality of any column in table, whatever the columns with very low cardinality are present in that table, will be considered for Mini Dimension.

6. Type 5: Add mini-dimension and type 1 outrigger
7. Type 6: Add Type 1 attributes to type 2 dimension
8. Type 7: Dual type 1 and type 2 dimensions

### Semantics

- *By*: is almost always followed by a dimension.
- *For*: is equal to a filter.

### Layers

Layers to process data <sup>17</sup>

- ODS: Operational Data Store
- DWD: Data Warehouse Detail
- DWS: Data Warehouse Summary
- ADS: Application Data Store

## Reference

1. [Designing Data-Intensive Application](https://www.notion.so/bobzeng/Read-Data-Intensive-System-498ff1dc017f4260b5530d10ea89b615)
2. [Apache Kylin](http://kylin.apache.org/docs/gettingstarted/concepts.html)
3. [Druid](https://druid.apache.org/druid.html)
4. [Data Cube: A Relational Aggregation Operator Generalizing
Group-By, Cross-Tab, and Sub-Totals,1997](https://arxiv.org/pdf/cs/0701155.pdf)
5. Data Warehouse System: Design and Implementation, 2014, Alejandro Vaisman etc.
6. [Semantic data model](https://www.wikiwand.com/en/Semantic_data_model)
7. [Hadoop vs MPP](https://0x0fff.com/hadoop-vs-mpp/)
8. [Data Warehouse Wiki](https://www.wikiwand.com/en/Data_warehouse)
9. [Gura99: What is data warehouse](https://www.guru99.com/data-warehousing.html)
10. [一种通用的数据库分层方法](https://www.notion.so/bobzeng/6b0c642ec83b430ca73054335519d6a1)
11. The Data Warehouse Toolkit: The Definitive Guide, Kimball
12. [Implementating a Real-Time Data Warehouse with Flink](https://www.alibabacloud.com/blog/implementating-a-real-time-data-warehouse-with-flink_595681)
13. [Enterprise Bus Matrix](https://www.wikiwand.com/en/Enterprise_bus_matrix)
14. [Rapidly Changing Monster Dimension – Mini Dimension In Data Warehousing](https://bidatasolution.wordpress.com/2015/09/14/mini-dimension/)
15. Star Schema The Complete Reference, Christopher Adamson, 2010
16. Mastering Data Warehouse Aggregates:Solutions for Star Schema Performance, Christopher Adamson ,2006
17. 大数据之路，阿里巴巴，2017