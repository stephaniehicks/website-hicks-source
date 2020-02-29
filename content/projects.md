---
title: "Projects"
date: "2019-01-02"
---

### Analysis of genomic data from single cells

Single-cell RNA-Sequencing (scRNA-seq) data has become the most widely used high-throughput method for transcription profiling of individual cells. This technology has created an unprecedented opportunity to investigate important biological questions that can only be answered at the single-cell level. However, this technology also brings new statistical, computational and methodological challenges (1, 2). 

1. Amezquita RA, Lun ATL, Carey VJ, Carpp LN, Geistlinger L, Marini F, Rue-Albrecht K, Risso D, Soneson C, Waldron L, Pages H, Smith M, Huber W, Morgan M, Gottardo R, **Hicks SC**. (2019). [Orchestrating Single-Cell Analysis with Bioconductor](https://doi.org/10.1038/s41592-019-0654-x). _Nature Methods_.

2. Lähnemann D, Koester J, Szczurek E, McCarthy D, **Hicks S**, Robinson MD, Vallejos C, Beerenwinkel N, et al. (2020). [Eleven Grand Challenges in Single-Cell Data Science](https://doi.org/10.1186/s13059-020-1926-6). _Genome Biology_. 


#### Spatial transcriptomics 

**[Join us](../join/index.html)** with an open postdoctoral position!

The goal of this project is to develop statistical methods and open-source software for the analysis of spatial transcriptomics data. This is highly relevant to public health because these methodologies will provide insights into topographical and pathological changes in gene expression for example in the aging human brain or in patients affected by psychiatric diseases. The funding for this project is from the [Chan Zuckerberg Initiative](https://chanzuckerberg.com). 

1. Maynard KR, Collado-Torres L, Weber LM, Uytingco C, Barry BK, Williams SR, II JLC,  Tran MN, Besich Z, Tippani M, Chew J, Yin Y, Kleinman JE, Hyde TM, Rao N, **Hicks SC**, Martinowich K, Jaffe AE (2020). [Transcriptome-scale spatial gene expression in the human dorsolateral prefrontal cortex](https://doi.org/10.1101/2020.02.28.969931). _bioRxiv_. 


#### Methods to address technical variablity

In contrast to bulk RNA-seq experiments, the majority of reported expression levels in scRNA-seq data are zeros, which could be either biologically-driven, genes not expressing RNA at the time of measurement, or technically-driven, genes expressing RNA, but not at a sufficient level to be detected by sequencing technology. In addition, systematic errors, including batch effects, have been widely reported as a major challenge in high-throughput technologies, however, surprisingly, these issues have received minimal attention in published studies based on scRNA-seq technology. To investigate this, I examined data from fifteen published scRNA-seq studies and demonstrated that systematic errors can explain a substantial percentage of observed cell-to-cell expression variability, which in turn can lead to false discoveries, for example, when using unsupervised learning methods (1). To address this, we developed a fast, scalable statistical framework for feature selection and dimensionality reduction using generalized principal component analysis (GLM-PCA) for scRNA-seq data, which permits the identification of low-dimensional representations of cells measured with unique molecular identifiers (UMI) count data using a multinomial model (2). More recently we performed a benchmark comparison of 18 scRNA-seq imputation methods across multiple experimental protocols and datasets (3). 

1.	**Hicks SC**, Townes FW, Teng M, Irizarry RA (2018). [Missing data and technical variability in single-cell RNA-sequencing experiments](https://academic.oup.com/biostatistics/article/19/4/562/4599254). _Biostatistics_. 
2.	Townes FW, **Hicks SC**, Aryee MJ, Irizarry RA (2019). [Feature Selection and Dimension Reduction for Single Cell RNA-Seq based on a Multinomial Model](https://doi.org/10.1186/s13059-019-1861-6). _Genome Biology_. 
3. Hou W, Ji J, Ji H, **Hicks SC** (2020). [A Systematic Evaluation of Single-cell RNA-sequencing Imputation Methods](https://www.biorxiv.org/content/10.1101/2020.01.29.925974v1). _bioRxiv_.


#### Fast, scalable, memory-efficient methods to analyze single-cell data

The _k_-means algorithm is a classic algorithm used in the analysis of scRNA-seq data. However, with increasing sizes of single-cell data, new methods are needed that are fast, scalable and memory-efficient. To address this, we are implementing the mini-batch optimization for _k_-means clustering proposed in [Sculley (2010)](https://www.eecs.tufts.edu/~dsculley/papers/fastkmeans.pdf) for large single cell sequencing data (1). The mini batch _k_-means algorithm can be run with data stored in memory or on disk (e.g. HDF5 file format).

1. [mbkmeans](http://bioconductor.org/packages/mbkmeans). Mini-batch k-means clustering for large single-cell datasets.

#### High-grade serous ovarian cancer subtypes with single-cell profiling

The goal of this project is to identify the biological basis of subtypes of high-grade serous ovarian cancers (HGSOC) using bulk and single-cell gene expression data. This is highly relevant to public health because HGSOC is a particularly deadly cancer that is often only identified at late stage and treatment options are limited. The long-term impact of this project will be a key step towards developing targeted treatments for HGSOCs. 

#### Practical and reproducible workflows for single-cell and single-nucleus analysis of childhood cancer data

The goal of this project, funded by [Alex's Lemonade Stand Foundation](https://www.alexslemonade.org), is to design and build practical, reproducible, statistically-rigorous workflows for the analysis of single-cell and and single-nucleus childhood cancer data. Most importantly, this will alllow researchers studying childhood cancers use the same or similar workflows to analyze their own data, which will help scientists in the field compare and contrast across studies. For more information, see the [highlight](https://www.alexslemonade.org/project/practical-reproducible-and-statistically-rigorous-workflows-single-nucleus-analysis) on the Alex's Lemonade Stand Foundation website. 


#### Development and neurogenesis of the enteric nervous system with single-cell profiling

The goal of this project is to study the steady-state and transcriptomic changes from stimuli and perturbations of neurons and surrounding cells in enteric nervous system (ENS) in the gastrointestinal tract (gut) using bulk and single-cell gene expression data. For example, one project investigates the remodeling and cellular changes in the gastrointestinal tract from inflammation. The ENS contains the largest collection of neurons in the body outside of the brain that regulate diverse gastrointestinal and  metabolic functions and is commonly referred to as our "second brain". A better understanding of the gut is highly relevant to public health because alterations and inflammation in the gut have been linked to diseases such as Parkinson's, colitis, irritable bowel syndrome, anxiety and mood disorders, with limited treatment options. The long-term impact of this project will be a key step towards developing targeted treatments for curbing inflammation and associated pathological changes in the gut.

--- 

### Data Science Education

An increase in demand for statistics and data science education has led to changes in curriculum, specifically an increase in computing. While this has led to more applied courses, students still struggle with effectively deriving knowledge from data and solving real-world problems. In 1999, Deborah Nolan and Terry Speed argued the solution was to teach courses through in-depth case studies derived from interesting scientific questions with nontrivial solutions that leave room for different analyses of the data. This innovative framework teaches the student to make important connections between the scientific question, data and statistical concepts that only come from hands-on experience analyzing data (1, 2). To address this, I am building the [Open Case Studies](https://opencasestudies.github.io) (OCS) community resource of case studies that educators can use in the classroom to teach students how to effectively derive knowledge from data. 

In addition, I am actively thinking about how to define the field from first principles, namely the elements and principles of data analysis, based on the activities of people who analyze data with a language and taxonomy for describing a data analysis in a manner spanning disciplines (3). This leads to two insights: it suggests a formal mechanism to evaluate data analyses (4) based on objective characteristics, and it provides a framework to teach students how to build data analyses. 

1. **Hicks SC**, Irizarry RA (2018). [A Guide to Teaching Data Science](https://www.tandfonline.com/doi/abs/10.1080/00031305.2017.1356747?journalCode=utas20). _The American Statistician_. 
2. **Hicks SC** (2017). [Greater Data Science Ahead](https://www.tandfonline.com/doi/abs/10.1080/10618600.2017.1385472). _Journal of Computational Graphical Statistics_. 
3. **Hicks SC**, Peng RD. (2019). [Elements and Principles for Characterizing Variation between Data Analyses](https://arxiv.org/abs/1903.07639). _arXiv_.
4. **Hicks SC**, Peng RD. (2019). [Evaluating the Success of a Data Analysis](https://arxiv.org/abs/1904.11907). _arXiv_.

--- 

### Statistical methods to control for false discoveries

In high-throughput studies, hundreds to millions of hypotheses are typically tested. Statistical methods that control the false discovery rate (FDR) have emerged as popular and powerful tools for error rate control. While classic FDR methods use only _p_-values as input, more modern FDR methods have been shown to increase power by incorporating complementary information as "informative covariates" to prioritize, weight, and group hypotheses. To address this, we investigated the accuracy, applicability, and ease of use of two classic and six modern FDR-controlling methods by performing a systematic benchmark comparison using simulation studies as well as six case studies in computational biology (1). 

1. Korthauer K, Kimes PK, Duvallet C, Reyes A, Subramanian A, Teng M, Shukla C, Alm EJ, **Hicks SC** (2019). [A practical guide to methods controlling false discoveries in computational biology](https://doi.org/10.1186/s13059-019-1716-1). _Genome Biology_. 


--- 

### Statistical methods for preprocessing and normalization of high-throughput data

Normalization is an essential step for the analysis of genomics high-throughput data. Quantile normalization is one of the most widely used multi-sample normalization tools for applications including genotyping arrays, RNA-Sequencing (RNA-Seq), DNA methylation, ChIP-Sequencing (ChIP-Seq) and brain imaging. However, quantile normalization relies on assumptions about the data-generation process that are not appropriate in some contexts. I developed a data-driven method to test these assumptions and guide the choice of an appropriate normalization method (1). The [freely available software](https://bioconductor.org/packages/release/bioc/html/quantro.html) has been downloaded over 7500 times (distinct IPs) from Bioconductor since 2014 and has helped researchers test the assumptions of global normalization methods in the analysis of their own data. To address the scenario when the assumptions of quantile normalization are not appropriate, I have developed a generalization of quantile normalization, referred to as smooth quantile normalization, which allows for global differences between biological groups (2). More recently, I collaborated with researchers from the University of Maryland to correct for compositional biases found in sparse metagenomic sequencing data (3) and developed a methods to estimate the cell composition in whole blood DNA methylation samples independent of platform-technology (4). 

1.	**Hicks SC**, Irizarry RA (2015). [quantro: a data-driven approach to guide the choice of an appropriate normalization method](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-015-0679-0). _Genome Biology_.
2.	**Hicks SC**, Okrah K, Paulson JN, Quackenbush J, Irizarry RA, Bravo HC (2018). [Smooth quantile normalization](https://academic.oup.com/biostatistics/article-abstract/19/2/185/3949169). _Biostatistics_.
3.	Kumar MS, Slud EV, Okrah K, **Hicks SC**, Hannenhalli S, Corrada Bravo H (2018). [Analysis and correction of compositional bias in sparse sequencing count data](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-5160-5). _BMC Genomics_. 
4. 	**Hicks SC**, Irizarry RA (2019). [methylCC: technology-independent estimation of cell type composition using differentially methylated regions](https://doi.org/10.1186/s13059-019-1827-8). _Genome Biology_.
5. Wang Y, **Hicks SC**, Hansen KD (2020). [Co-expression analysis is biased by a mean-correlation relationship](https://www.biorxiv.org/content/10.1101/2020.02.13.944777v1). _bioRxiv_