---
layout: post
title:  "Data and Knowledge Discovery"
date:   2021-02-13 22:00:00 +0800
---

## Introduction

Why `metadata hub` <sup>5</sup>
> .. what they're really referring to is the ability for a random data analyst to keep up with the rest of a very large data-producing and data-consuming orgranisation

## Components

- Search interface
- UI which is explorable
- An API service that communicates with internal data services
- Ability to update metadata by human

## Tools

- [`Dataporl`](https://www.slideshare.net/neo4j/graphconnect-europe-2017-democratizing-data-at-airbnb) by Airbnb
    - key stack: `neo4j`
- [`Metacat`](https://netflixtechblog.com/metacat-making-big-data-discoverable-and-meaningful-at-netflix-56fb36a53520) by Netflix
![alt text](https://miro.medium.com/max/700/1*Nz8bc62eRDxegVkzJr_HrQ.png "Metacat")

- `DataHub` by Linkedin
- `Databook` by Uber
- `Amundsen` by Lyft

- `Lexikon` by Spotify
- `Data Catalog` by GCP


## Topics 

### Data Lineage

> By parsing through the SQL code from query logs in Snowflake, it’s possible to automatically create column-level lineage, assign a popularity score to every data asset, and even deduce the potential owners and experts for each asset.

## Reference

1. [Admunsen: meta data driven application](https://github.com/amundsen-io/amundsen)
2. [Knowledge Repo](https://github.com/airbnb/knowledge-repo)
3. [DataHub: A Generalized Metadata Search & Discovery Tool](https://github.com/linkedin/datahub)
4. Edge#62: Data Discovery and Management Architectures at LinkedIn, Uber, Lyft, Airbnb and Netflix, TheSequence, 2021
5. [A Dive Into Metadata Hubs, Cedric Chin, 2020](https://www.holistics.io/blog/a-dive-into-metadata-hubs/)
6. [Data Catalog 3.0: Modern Meta Data for Modern Data Stack](https://towardsdatascience.com/data-catalog-3-0-modern-metadata-for-the-modern-data-stack-ec621f593dcf)