---
layout: post
title:  "Feature Store"
date:   2020-02-12 22:00:00 +0800
---
My teammates and I have been thinking doing some kind of feature store which will address folloing chanllenges:

1. Time is wasted when data analysts do analytics from scratch again and again. As you may know, feature engineering and discovery are the most time-consuming part of data analytics/ data science. 

    - discover what has been done is not easy
    - applied acquired knowledge to what we face now is not easy (on organisation level)
    - ensure feature is still relevant is not easy  

2. Features are not normalised and standardised. Normalisation will benefit modelling. Standardization will benefit data quality since definitions are aligned.
    
    - need to be confident about where is the data from: data lineage/data management
    - normalised and scaled methodologies
![tree is not for this.use things properly]({{site.baseurl}}/resources/feature_store.PNG)

## Reference

1. [Feature store for machine learning](https://docs.featurestore.org/)
2. [Rethinking Feature Store](https://medium.com/@changshe/rethinking-feature-stores-74963c2596f0)
