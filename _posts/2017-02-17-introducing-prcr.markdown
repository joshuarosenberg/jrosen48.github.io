---
layout: post
title:  "Introducing the prcr package for person-centered analysis in R"
date:   2017-02-17 16:59:00 -0500
categories: R 
---

I'm excited to introduce `prcr` (v. 0.1.0), an R package for person-centered analysis. 

The package is available on CRAN via `install.packages("prcr")`. 

A vignette introducing the package is [here](https://cran.r-project.org/web/packages/prcr/vignettes/introduction_to_prcr.html), though the main function is `create_profiles(df, n_clusters)`, with `df` a `data.frame` of the variables to be clustered and `n_clusters` the specified number of profiles to identify. 

There's more information in the vignette on how to access the output from `create_profiles()`, though the generic functions `summary()`, `plot()`, and `print()` are useful to start.

Please [contact me](mailto:jrosen@msu.edu) or create an issue (or folk the project) on the [GitHub page](https://github.com/jrosen48/prcr) for prcr.