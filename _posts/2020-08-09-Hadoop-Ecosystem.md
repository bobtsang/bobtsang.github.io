---
layout: post
title:  "Hadoop Ecosystem"
date:   2020-08-09 22:59:07 +0800
---
## Facilities

1. Hadoop Common
2. HDFS: Hadoop Distributed File System
3. Hadoop Yarn
4. Hadoop MapReduce
5. Hadoop Ozone

## HDFS

- HDFS stores metadata and application data separately.
- `NameNode`: metadata
- `DataNode`: application data; file contents are replicated across multiple `DataNode` for reliability

> The NameNode maintains the namespace tree and the mapping of file blocks to DataNodes (the physical location of file data).

## Apache Ambari

The Apache Ambari project is aimed at making Hadoop management simpler by developing software for provisioning, managing, and monitoring Apache Hadoop clusters. 


## Reference

[1] [Apache Hadoop Documentation](https://hadoop.apache.org/) <br>
[2] [Apache Ambari](https://ambari.apache.org/) <br>
[3] [Apache Ranger](https://ranger.apache.org/) <br>
[4] [Awesome Hadoop](https://github.com/youngwookim/awesome-hadoop) <br>
[5] [Hadoop vs. MPP](https://0x0fff.com/hadoop-vs-mpp/)