---
title: "Software and data packages"
date: "2019-01-02"
---

## Bioconductor 

#### Software packages

- [R/SpatialExperiment](https://www.bioconductor.org/packages/SpatialExperiment) <img src="https://bioconductor.org/shields/years-in-bioc/SpatialExperiment.svg">: R/Bioconductor package to define a S4 class for data with spatial coordinates by extending SingleCellExperiment to include spatial experiments such as seqFISH and 10x Visium spatial transcriptomics technologies. ([Righelli, Weber, Crowell et al., 2021. _bioRxiv_](https://doi.org/10.1101/2021.01.27.428431)). 
- [R/bluster](https://www.bioconductor.org/packages/bluster) <img src="https://bioconductor.org/shields/years-in-bioc/bluster.svg">: R/Bioconductor package to wrap common clustering algorithms in an easily extended S4 framework. Backends are implemented for hierarchical, k-means and graph-based clustering. Several utilities are also provided to compare and evaluate clustering results.
- [R/spQN](http://bioconductor.org/packages/spqn) <img src="https://bioconductor.org/shields/years-in-bioc/spqn.svg">: R/Bioconductor package to implement spatial quantile normalization (SpQN). This method was developed to remove a mean-correlation relationship in correlation matrices built from gene expression data. ([Wang et al., 2020. _bioRxiv_](https://doi.org/10.1101/2020.02.13.944777)).
- [R/scry](https://bioconductor.org/packages/scry) <img src="https://bioconductor.org/shields/years-in-bioc/scry.svg">: R/Bioconductor package to implement count-based feature selection and dimension reduction algorithms to facilitate unsupervised analysis of any high-dimensional data such as single-cell RNA-seq. This package builds around the [glmpca R CRAN package](https://cran.r-project.org/web/packages/glmpca/index.html). ([Townes et al., 2019. _Genome Biology_](https://doi.org/10.1186/s13059-019-1861-6)). 
- [R/methylCC](http://bioconductor.org/packages/methylCC) <img src="https://bioconductor.org/shields/years-in-bioc/methylCC.svg">: R/Bioconductor package to estimate the cell composition of whole blood in DNA methylation samples in microarray or sequencing platforms. ([Hicks and Irizarry, 2019. _Genome Biology_](https://doi.org/10.1186/s13059-019-1827-8)).
- [R/mbkmeans](http://bioconductor.org/packages/mbkmeans) <img src="https://bioconductor.org/shields/years-in-bioc/mbkmeans.svg">: R/Bioconductor package implementing the mini-batch optimization for _k_-means (**mbkmeans**)clustering proposed in [Sculley (2010)](https://www.eecs.tufts.edu/~dsculley/papers/fastkmeans.pdf) for large datasets, including single-cell RNA-sequencing data. The mini batch _k_-means algorithm can be run with data stored in-memory or on-disk (e.g. HDF5 file format). ([Hicks et al., 2021. _PLOS Computational Biology_](https://doi.org/10.1371/journal.pcbi.1008625)).
- [R/TreeSummarizedExperiment](https://www.bioconductor.org/packages/TreeSummarizedExperiment) <img src="https://bioconductor.org/shields/years-in-bioc/TreeSummarizedExperiment.svg">: R/Bioconductor package to define a S4 class for data with hierarchical structure by extending SingleCellExperiment to include hierarchical information on the rows or columns of the rectangular data. ([Huang et al., 2020. _F1000_](https://doi.org/10.12688/f1000research.26669.1)).
- [R/qsmooth](http://bioconductor.org/packages/qsmooth) <img src="https://bioconductor.org/shields/years-in-bioc/qsmooth.svg">: R package available that implements a generalization of quantile normalization, referred to as smooth quantile normalization (**qsmooth**), which is based on the assumption that the statistical distribution of each sample should be the same (or have the same distributional shape) within biological groups or conditions. ([Hicks et al., 2018. _Biostatistics_](https://doi.org/10.1093/biostatistics/kxx028)).
- [R/quantro](http://www.bioconductor.org/packages/release/bioc/html/quantro.html) <img src="https://bioconductor.org/shields/years-in-bioc/quantro.svg">: R package available on Bioconductor to test for global differences between groups of distributions to decide when to use quantile normalization. ([Hicks and Irizarry, 2015. _Genome Biology_](https://doi.org/10.1186/s13059-015-0679-0)).

#### Data packages

- [spatialLIBD](http://www.bioconductor.org/packages/spatialLIBD): Inspect interactively the spatial transcriptomics 10x Genomics Visium data analyzed by Lieber Institute for Brain Development researchers and collaborators. ([Maynard, Collado-Torres et al., 2021. _Nature Neuroscience_](https://doi.org/10.1038/s41593-020-00787-0)). 
- [benchmarkfdrData2019](http://bioconductor.org/packages/benchmarkfdrData2019): Benchmarking results for experimental and simulated data sets used in Korthauer and Kimes et al. (2019) to compare methods for controlling the false discovery rate. A shiny app to interactively explore the data is available on the [benchmark-shiny repository](https://github.com/kdkorthauer/benchmarkfdr-shiny) on GitHub. 
- [bodymapRat](http://bioconductor.org/packages/bodymapRat): R data package that contains an SummarizedExperiment from the [Yu et al. (2013)](https://www.ncbi.nlm.nih.gov/pubmed/24510058) paper that performed the rat BodyMap across 11 organs and 4 developmental stage. 
- [TENxPBMCData](http://bioconductor.org/packages/TENxPBMCData): R data package that contains a set of SingleCellExperiment objects with single-cell RNA-sequencing data from peripheral blood mononuclear cells generated by 10X Genomics. 

## CRAN 

#### Software packages

- [R/glmpca](https://cran.r-project.org/web/packages/glmpca/index.html): Implements a generalized version of principal components analysis (GLM-PCA) for dimension reduction of non-normally distributed data such as counts or binary matrices. ([Townes et al., 2019. _Genome Biology_](https://doi.org/10.1186/s13059-019-1861-6)).


## GitHub

#### Software packages

- [R/quantroSim](https://github.com/stephaniehicks/quantroSim): Supporting data simulation R-package for the *quantro* R-package to simulate gene expression and DNA methylation data.
- [R/explainr](https://github.com/hilaryparker/explainr): translates S3 objects into text using standard templates in a simple and convenient way. 
- [postMUT](https://github.com/stephaniehicks/postMUT): A tool implemented in Perl and R to predict the functionality of missense mutations.


#### Data packages

- [trapnell2014myoblasthuman](https://github.com/stephaniehicks/trapnell2014myoblasthuman): R data package that contains an ExpressionSet object from Trapnell et al. (2014) that performed a time-series experiment of bulk and single cell RNA-Seq at four time points in differentiated primary human myoblasts. 
- [patel2014gliohuman](https://github.com/willtownes/patel2014gliohuman): R data package that contains a SummarizedExpression object from Patel et al. (2014) with single cell and bulk RNA-Seq data on five human glioblastoma tumors. 
- [colonCancerWGBS](https://github.com/genomicsclass/colonCancerWGBS): Cov files produced from [Bismark](http://www.bioinformatics.babraham.ac.uk/projects/bismark/) after mapping six paired tumor-normal WGBS samples from Ziller et al. (2013) PMID: 23925113. Only chr22. 
- [myAffyData](https://github.com/stephaniehicks/mycAffyData): AffyBatch object from an experiment using P493-6 cells expressing low or high levels of c-Myc. Data from Loven et al. (2012) Cell 151: 476-482.
- [BackgroundExperimentYeast](https://github.com/stephaniehicks/BackgroundExperimentYeast): AffyBatch object from an experiment to measure NSB and optical noise in yeast.

