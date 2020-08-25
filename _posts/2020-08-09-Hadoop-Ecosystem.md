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

## Reference

[1] [Apache Hadoop Documentation](https://hadoop.apache.org/) <br>
[2] [Apache Ambari](https://ambari.apache.org/)
[3] [Apache Ranger](https://ranger.apache.org/)