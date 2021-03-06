---
layout: post
title:  "prcr: An R Package for Person-Centered Analysis"
date:   2017-02-17 16:59:00 -0500
categories: R 
---

I'm excited to share that `prcr` (0.1.0), an R package for person-centered analysis, is now available on CRAN via `install.packages("prcr")`.

Person-centered analyses focus on clusters, or profiles, of observations, and their change over time or differences across factors. 

The package is designed to be "low threshold but high ceiling", in that you can do all of the analysis with one function, `create_profiles(df, n_clusters)`, where `df`is a `data.frame` of the variables to cluster, and `n_clusters` is the specified number of clusters. 

If you look at `?create_profiles()`, there are a lot of other options, from whether to center / scale the data (with `to_scale` and `to_center`), to the distance metric and linkage method. The function also outputs all of the information from the clustering, so you can extract the dendrogram from the hierarchical clustering, for example. 

A brief vignette / tutorial using built-in data is [here](https://cran.r-project.org/web/packages/prcr/vignettes/introduction_to_prcr.html).

Please feel free to [contact me](mailto:jrosen@msu.edu) or create an issue (or fork the project) on the [GitHub page](https://github.com/jrosen48/prcr) for prcr.