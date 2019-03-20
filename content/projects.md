---
title: "Projects"
date: "2019-01-02"
---

### Analysis of genomic data from single cells

Single-cell RNA-Sequencing (scRNA-seq) data has become the most widely used high-throughput method for transcription profiling of individual cells. This technology has created an unprecedented opportunity to investigate important biological questions that can only be answered at the single-cell level. However, this technology also brings new statistical, computational and methodological challenges. 

#### Methods to address technical variablity

In contrast to bulk RNA-seq experiments, the majority of reported expression levels in scRNA-seq data are zeros, which could be either biologically-driven, genes not expressing RNA at the time of measurement, or technically-driven, genes expressing RNA, but not at a sufficient level to be detected by sequencing technology. In addition, systematic errors, including batch effects, have been widely reported as a major challenge in high-throughput technologies, however, surprisingly, these issues have received minimal attention in published studies based on scRNA-seq technology. To investigate this, I examined data from fifteen published scRNA-seq studies and demonstrated that systematic errors can explain a substantial percentage of observed cell-to-cell expression variability, which in turn can lead to false discoveries, for example, when using unsupervised learning methods (1). More recently, we developed a fast, scalable statistical framework for feature selection and dimensionality reduction using generalized principal component analysis (GLM-PCA) for scRNA-seq data, which permits the identification of low-dimensional representations of cells measured with unique molecular identifiers (UMI) count data using a multinomial model (2).

1.	Hicks SC, Townes FW, Teng M, Irizarry RA (2018). [Missing data and technical variability in single-cell RNA-sequencing experiments](https://academic.oup.com/biostatistics/article/19/4/562/4599254). _Biostatistics_. 
2.	Townes FW, Hicks SC, Aryee MJ, Irizarry RA (2019). [Feature Selection and Dimension Reduction for Single Cell RNA-Seq based on a Multinomial Model](https://doi.org/10.1101/574574). _bioRxiv_. 


#### Fast, scalable, memory-efficient methods to analyze single-cell data

The _k_-means algorithm is a classic algorithm used in the analysis of scRNA-seq data. However, with increasing sizes of single-cell data, new methods are needed that are fast, scalable and memory-efficient. To address this, we are implementing the mini-batch optimization for _k_-means clustering proposed in [Sculley (2010)](https://www.eecs.tufts.edu/~dsculley/papers/fastkmeans.pdf) for large single cell sequencing data (1). The mini batch _k_-means algorithm can be run with data stored in memory or on disk (e.g. HDF5 file format).

1. [mbkmeans](https://github.com/drisso/mbkmeans).  Mini-batch k-means clustering for large single-cell datasets.


#### High-grade serous ovarian cancer subtypes with single-cell profiling

The goal of this project is to identify the biological basis of subtypes of high-grade serous ovarian cancers (HGSOC) using bulk and single-cell gene expression data. This is highly relevant to public health because HGSOC is a particularly deadly cancer that is often only identified at late stage and treatment options are limited. The long-term impact of this project will be a key step towards developing targeted treatments for HGSOCs. 

#### Practical and reproducible workflows for single-cell and single-nucleus analysis of childhood cancer data

The goal of this project, funded by [Alex's Lemonade Stand Foundation](https://www.alexslemonade.org), is to design and build practical, reproducible, statistically-rigorous workflows for the analysis of single-cell and and single-nucleus childhood cancer data. Most importantly, this will alllow researchers studying childhood cancers use the same or similar workflows to analyze their own data, which will help scientists in the field compare and contrast across studies.


#### Development and neurogenesis of the enteric nervous system with single-cell profiling

The goal of this project is to study the steady-state and transcriptomic changes from stimuli and perturbations of neurons and surrounding cells in enteric nervous system (ENS) in the gastrointestinal tract (gut) using bulk and single-cell gene expression data. For example, one project investigates the remodeling and cellular changes in the gastrointestinal tract from inflammation. The ENS contains the largest collection of neurons in the body outside of the brain that regulate diverse gastrointestinal and  metabolic functions and is commonly referred to as our "second brain". A better understanding of the gut is highly relevant to public health because alterations and inflammation in the gut have been linked to diseases such as Parkinson's, colitis, irritable bowel syndrome, anxiety and mood disorders, with limited treatment options. The long-term impact of this project will be a key step towards developing targeted treatments for curbing inflammation and associated pathological changes in the gut.

**If you are interested in this project**, there is an open postdoctoral scientist position (see the [Join us](../join/index.html) page for more information)!



--- 

### Data Science Education

An increase in demand for statistics and data science education has led to changes in curriculum, specifically an increase in computing. While this has led to more applied courses, students still struggle with effectively deriving knowledge from data and solving real-world problems. In 1999, Deborah Nolan and Terry Speed argued the solution was to teach courses through in-depth case studies derived from interesting scientific questions with nontrivial solutions that leave room for different analyses of the data. This innovative framework teaches the student to make important connections between the scientific question, data and statistical concepts that only come from hands-on experience analyzing data (1, 2). To address this, I am building the [openDataCases](https://github.com/opencasestudies) community resource of case studies that educators can use in the classroom to teach students how to effectively derive knowledge from data. 

In addition, I am actively thinking about how to define the field from first principles, namely the elements and principles of data analysis, based on the activities of people who analyze data with a language and taxonomy for describing a data analysis in a manner spanning disciplines (3). This leads to two insights: it suggests a formal mechanism to evaluate data analyses based on objective characteristics, and it provides a framework to teach students how to build data analyses. 

1. Hicks SC, Irizarry RA (2018). [A Guide to Teaching Data Science](https://www.tandfonline.com/doi/abs/10.1080/00031305.2017.1356747?journalCode=utas20). _The American Statistician_. 
2. Hicks SC (2017). [Greater Data Science Ahead](https://www.tandfonline.com/doi/abs/10.1080/10618600.2017.1385472). _Journal of Computational Graphical Statistics_. 
3. Hicks SC, Peng RD. (2019). [Elements and Principles of Data Analysis](https://arxiv.org/abs/1903.07639). _arXiv_.


--- 

### Statistical methods to control for false discoveries

In high-throughput studies, hundreds to millions of hypotheses are typically tested. Statistical methods that control the false discovery rate (FDR) have emerged as popular and powerful tools for error rate control. While classic FDR methods use only _p_-values as input, more modern FDR methods have been shown to increase power by incorporating complementary information as "informative covariates" to prioritize, weight, and group hypotheses. To address this, we investigated the accuracy, applicability, and ease of use of two classic and six modern FDR-controlling methods by performing a systematic benchmark comparison using simulation studies as well as six case studies in computational biology (1). 

1. Korthauer K, Kimes PK, Duvallet C, Reyes A, Subramanian A, Teng M, Shukla C, Alm EJ, Hicks SC (2018). [A practical guide to methods controlling false discoveries in computational biology](https://doi.org/10.1101/458786). _bioRxiv_. 


--- 

### Statistical methods for normalization of high-throughput data

Normalization is an essential step for the analysis of genomics high-throughput data. Quantile normalization is one of the most widely used multi-sample normalization tools for applications including genotyping arrays, RNA-Sequencing (RNA-Seq), DNA methylation, ChIP-Sequencing (ChIP-Seq) and brain imaging. However, quantile normalization relies on assumptions about the data-generation process that are not appropriate in some contexts. I developed a data-driven method to test these assumptions and guide the choice of an appropriate normalization method (1). The [freely available software](https://bioconductor.org/packages/release/bioc/html/quantro.html) has been downloaded over 7500 times (distinct IPs) from Bioconductor since 2014 and has helped researchers test the assumptions of global normalization methods in the analysis of their own data. To address the scenario when the assumptions of quantile normalization are not appropriate, I have developed a generalization of quantile normalization, referred to as smooth quantile normalization, which allows for global differences between biological groups (2). More recently, I collaborated with researchers from the University of Maryland to correct for compositional biases found in sparse metagenomic sequencing data (3). 

1.	Hicks SC, Irizarry RA (2015). [quantro: a data-driven approach to guide the choice of an appropriate normalization method](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-015-0679-0). _Genome Biology_.
2.	Hicks SC, Okrah K, Paulson JN, Quackenbush J, Irizarry RA, Bravo HC (2018). [Smooth quantile normalization](https://academic.oup.com/biostatistics/article-abstract/19/2/185/3949169?redirectedFrom=fulltext). _Biostatistics_. 
3.	Kumar MS, Slud EV, Okrah K, Hicks SC, Hannenhalli S, Corrada Bravo H (2018). [Analysis and correction of compositional bias in sparse sequencing count data](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-5160-5). _BMC Genomics_. 

