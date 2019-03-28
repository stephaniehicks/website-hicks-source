---
title: Updates in the world of single-cell RNA-sequencing data analysis
author: Stephanie Hicks
date: '2019-03-20'
slug: updates-in-the-world-of-single-cell-rna-sequencing-data-analysis
categories:
  - single-cell
tags:
  - single-cell
---

In the last few weeks, there have been quite a few great pre-prints posted
on bioRxiv related to the analysis of a popular type of genomics data, 
called single-cell RNA-sequencing (scRNA-seq). The idea with this data 
is that you can measure genome-wide features (such as genes or transcripts) 
in individual cells, in contrast to more traditional bulk RNA-sequencing 
experiments where for each feature, you get an average of gene expression 
across all the cells in the sample. One key insight that has been widely
talked about in the world of scRNA-seq data analysis is the over inflation 
of the number of zeros, or sparsity, of the data compared to bulk RNA-sequencing
measurements. Therefore, for several years now, lots of work has been focused on
developing zero-inflation aware methods. Many early contributions were based on 
what are commonly referred to as plate-based protocols as opposed to 
the more recently developed droplet-based protocols that have what are called 
unique molecular identifiers (UMIs) -- little barcodes attached to the ends of 
the mRNA that remove certain biases related to PCR amplification. Here, 
I wanted to write up a quick blogpost summarizing one of the key takeaways 
that have come out from some recent pre-prints. 

## Droplet-based scRNA-seq data with UMI counts are not zero inflated

There were hints of this in 2017 [[Vieth et al. (2017)](https://www.ncbi.nlm.nih.gov/pubmed/29036287) and a 
[blogpost by Valentine Svensson in 2017](https://web.archive.org/web/20171119115058/http://www.nxn.se/valent/2017/11/16/droplet-scrna-seq-is-not-zero-inflated)], but several recent pre-prints have come 
out supporting this idea. [Townes et al. (2019)](https://doi.org/10.1101/574574) 
showed UMI count data derived from negative control scRNA-seq datasets 
(i.e. identical RNA was added to droplets and sequenced aka we do 
not expect any biological variation) are well-described by multinomial
distributions, which can be approximated by Poisson and negative 
binomial distributions. A few days later 
[Hafemeister and Satija (2019)](https://doi.org/10.1101/576827) 
independently published similar results, with a different error
distribution. The next day, 
[Svensson et al. (2019)](https://doi.org/10.1101/582064)
took the analysis from his 
[2017 blogpost](https://web.archive.org/web/20171119115058/http://www.nxn.se/valent/2017/11/16/droplet-scrna-seq-is-not-zero-inflated) and converted it into a pre-print. 
Here, he took five negative control droplet scRNA-seq datasets 
(again, identical RNA was added to droplets and sequenced aka we 
do not expect any biological variation), and showed how the 
data -- well 4 out of 5 datasets -- dropseq was a bit wonky) fit nicely 
to a negative binomial distribution. This matches what previous 
authors have found [Vieth et al. (2017)](https://www.ncbi.nlm.nih.gov/pubmed/29036287). 
Svensson argues this suggests an over-abundance of zeros in biological 
data is likely real biological variation, as opposed to 
technical variation, which also been suggested by 
[Andrews and Hemberg (2018)](https://www.ncbi.nlm.nih.gov/pubmed/30590489)
as a way to identify genes that contain biologically meaningful information. 

Both Townes and Svensson hypothesize that the zero-inflation in non-UMI 
data is related to the outliers in PCR duplicated counts, which is corrected 
by the use of UMIs. Svensson does not perform a similar assessment of 
plate-based scRNA-seq datasets because no comparable negative control 
data exists or plate-based methods. However, Svensson goes on to hypothesize 
that plate-based methods might introduce an additional layer out count noise
leading to over dispersion and manifesting as additional zeros. 

What does this mean for the field going forward? This means that the choice of 
methods used for the analysis of scRNA-seq data will likely vary depending
on the type of protocol used to generate that data. I guess this is not 
*so suprising*, but methods do matter and the assumptions behind those 
methods are important to think about. However, ultimately I'm just excited
to see such great work from multiple groups all converge on a similar idea.
Hope this helps to move the field forward. 

