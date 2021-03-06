---
layout: post
title:  "Announcing clustRcompaR v.0.1.0"
date:   2017-01-07 10:16:00 -0500
categories: tools 
---

Alex Lishinski and I worked on an `R` package over the last year or so. We are excited that it's now available on [CRAN](https://cran.r-project.org/web/packages/clustRcompaR/index.html). 

You can install the package using `install.packages('clustRcompaR')` (only needed first time) and load it (more on its two functions below) using `library(clustRcompaR)`.

Here's a description:

> Provides an interface to perform cluster analysis on a corpus of text. Interfaces to Quanteda to assemble text corpuses easily. Deviationalizes text vectors prior to clustering using technique described by Sherin (Sherin, B. [2013]. A computational study of commonsense science: An exploration in the automated analysis of clinical interview data. Journal of the Learning Sciences, 22(4), 600-638. Chicago. http://dx.doi.org/10.1080/10508406.2013.836654). Uses cosine similarity as distance metric for two stage clustering process, involving Ward's algorithm hierarchical agglomerative clustering, and k-means clustering. Selects optimal number of clusters to maximize "variance explained" by clusters,, adjusted by the number of clusters. Provides plotted output of clustering results as well as printed output. Assesses "model fit" of clustering solution to a set of preexisting groups in dataset.

I learned about document clustering and this approach by Christina Krist, who introduced me to to the paper cited (and referenced) in the description. It is straightforward but powerful in light of other approaches like [topic modeling](https://cran.r-project.org/web/packages/topicmodels/vignettes/topicmodels.pdf).

Here's more background:

[Document clustering](https://en.wikipedia.org/wiki/Document_clustering) is a common technique to discover topics in a corpus of texts. This package uses functions from the [`quanteda`](https://github.com/kbenoit/quanteda) `R` package as the basis for two functions, `cluster()` and `compare(), to make document clustering and comparing topics identified through document clustering across factors straightforward.

* First, use `cluster()` on a `data.frame` with the first column a `vector` of character strings, and any other columns are `vectors` of `factors` (such as groups representing different time points and classes taught by different teachers).
 
* Next, use `compare()` with the output from the `cluster()` function along with a `string` for the factor to compare the frequency of clusters to.

If you happen to use it and would like to suggest improvements, have any issues, or make changes, all of the contents are [available on GitHub](https://github.com/alishinski/clustRcompaR).
