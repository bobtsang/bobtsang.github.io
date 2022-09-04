---
layout: post
title:  "Database System"
date:   2022-09-04 22:59:07 +0800
---
#### Database system overview

Database system would mainly compos 4 parts

1. transport layer accepting requests
2. query processor optimising the queries
3. an execution engine
4. storage engine

#### Comparing Database

- Schema and record sizes
- Number of clients
- Types of queries and access pattern
- Rates of the read and write queries
- Expected changes in any of these variables

#### Database Management System (DBMS)

![dbms]({{site.baseurl}}/resources/dbms.png)

> A database system usually separates data files and index files: data files store data records, while index files store record metadata and use it to locate records in data files.


#### Naming Convention

##### Tables

1. Singular Names
Table names should be singular because

- Indicating one record per row, level of details; It's like `class` in programming language
- do not need to worry about plural transformation in English: person --> people

2. Prefixes

- Should avoid if not necessary; typing more characteres if having it
- Helpful when you need to group related tables together

#### Terminology

##### ACID

- Atomicity
  An operation either succeeds completely or fails, it does not leave partial data.
- Consistency
  Once an application performs an operation the results of that operation are visible to it in every subsequent operation
- Isolation
  An incomplete operation by one user does not cause unexpected side effects for other users
- Durability
  Once an operation is complete it will be preserved even in the face of machine or system failure

#### Reference

[1]Database Internals,Alex Petrov, 2019 <br>
[2][Naming convention](http://en.dwhwiki.info/templates/process/naming_conventions), Data Warehouse Wiki <br>
[3] Transaction Processing Benchmark,[TPC BENCHMARK DS](http://tpc.org/tpc_documents_current_versions/pdf/tpc-ds_v2.13.0.pdf) <br>
[4] [MVCC: Multiversion Concurrency Control, Wikipedia](https://www.wikiwand.com/en/Multiversion_concurrency_control) <br>
[5] [Database System Concepts, 7th ed., 2019 <br>
[6] [CMU Database System 15-445/645 Course Schedules](https://15445.courses.cs.cmu.edu/fall2021/schedule.html)
