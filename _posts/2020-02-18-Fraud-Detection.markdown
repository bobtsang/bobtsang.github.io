---
layout: post
title:  "Fraud Detection"
date:   2020-02-18 22:00:00 +0800
---
Overview of general techniques used.

## Graph-based Learning

- Plain graph: the only information is the structure.
- Attributed graph: nodes and edges have features associated

### Structured Based

This method relies on investigating the structure to find patterns.

- feature-based
  - graph-centric features

    ```
    .. nodes,dyads, triads, egonets, communities, as well as global graph structure.. 
    ```

    - node-level features
      - in/out degress
      - centrality
      - closeness
    - dyad features
      - number of common neighbors
    - global features
      - number of connected components 

  - other additional features

- proximity-based
  
  calculate closeness based on graph based structure

### Community Based

```
..finding densely connected groups of close-by nodes..
```

Main problems addressed for this methodology:

- how to find the community of a given node
- how to quantify the level of the given node to be a bridge node

## Reference

[1] Graph based anomaly detection and description:a survey, Leman etc., 2014
