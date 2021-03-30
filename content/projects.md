---
title: "Projects"
date: "2019-01-02"
---

# Analysis of genomic data from single cells

Single-cell RNA-Sequencing (scRNA-seq) data has become the most widely used high-throughput method for transcription profiling of individual cells. This technology has created an unprecedented opportunity to investigate important biological questions that can only be answered at the single-cell level. However, this technology also brings new statistical and computational challenges (1, 2). 

1. Amezquita RA, Lun ATL, Carey VJ, Carpp LN, Geistlinger L, Marini F, Rue-Albrecht K, Risso D, Soneson C, Waldron L, Pages H, Smith M, Huber W, Morgan M, Gottardo R, **Hicks SC**. (2020). [Orchestrating Single-Cell Analysis with Bioconductor](https://doi.org/10.1038/s41592-019-0654-x). _Nature Methods_.

2. Lähnemann D, Koester J, Szczurek E, McCarthy D, **Hicks S**, Robinson MD, Vallejos C, Beerenwinkel N, et al. (2020). [Eleven grand challenges in single-cell data science](https://doi.org/10.1186/s13059-020-1926-6). _Genome Biology_. 


#### Methods to identify and remove systematic errors and biases in single-cell data

I was one of the first to demonstrate that systematic errors can explain a substantial percentage of observed cell-to-cell expression variability scRNA-seq, which in turn can lead to false discoveries, for example, when using unsupervised learning methods (1). To address this, we developed a fast, scalable statistical framework for feature selection and dimensionality reduction using generalized principal component analysis (GLM-PCA) for scRNA-seq data, which permits the identification of low-dimensional representations of cells measured with unique molecular identifiers (UMI) count data using a multinomial model (2). These count-based models can be generalized using the Tweedie family of distributions, which we used to develop a stastical method to identify differentially expressed genes (3). More recently, we developed a probabilistic model to identify low-quality cells in scRNA-seq data (4).

1.	**Hicks SC**, Townes FW, Teng M, Irizarry RA (2018). [Missing data and technical variability in single-cell RNA-sequencing experiments](https://academic.oup.com/biostatistics/article/19/4/562/4599254). _Biostatistics_. 
2.	Townes FW, **Hicks SC**, Aryee MJ, Irizarry RA (2019). [Feature Selection and Dimension Reduction for Single Cell RNA-Seq based on a Multinomial Model](https://doi.org/10.1186/s13059-019-1861-6). _Genome Biology_. 
4. **Hippen AA**, Falco MM, **Weber LM**, Erkan EP, Zhang K, Dohert JA, Vähärautio A, Greene CS, **Hicks SC**. (2021). [miQC: An adaptive probabilistic framework for quality control of single-cell RNA-sequencing data](https://doi.org/10.1101/2021.03.03.433798). _bioRxiv_.


#### Methods for fast, memory-efficient distance metrics and unsupervised clustering for single-cell data

Computational methods and open-source software to store, access, and analyze single-cell data are essential. Most importantly, they need to be fast, scalable, and memory efficient. For example, the _k_-means algorithm is a classic algorithm used in the analysis of scRNA-seq data. However, with increasing sizes of single-cell data, new methods are needed that are fast, scalable and memory-efficient. To address this, we implemented the mini-batch optimization for _k_-means clustering proposed in [Sculley (2010)](https://www.eecs.tufts.edu/~dsculley/papers/fastkmeans.pdf) for large single cell sequencing data (1), including fast and memory-efficient k-means++ center finding with distance measures designed for count data and probability distributions (2). The mini-batch _k_-means algorithm can be run with data stored in memory or on disk (e.g. HDF5 file format). We have also implemented scalable data infrastructure to store and access single-cell data that can be explored with hierarchical structures (e.g. cell types) (3). 

1. **Hicks SC**, Liu R, Ni Y, Purdom E, Risso D. (2020). [mbkmeans: fast clustering for single cell data using mini-batch _k_-means](https://doi.org/10.1371/journal.pcbi.1008625). _PLOS Computational Biology_.
2. Baker DN, Dyjack N, Braverman V, **Hicks SC**, Langmead B. (2021). [minicore: Fast scRNA-seq clustering with various distance measures](https://doi.org/10.1101/2021.03.24.436859). _bioRxiv_.
3. Huang R, Soneson C, Ernst FGM, Rue-Albrecht KC, Guangchuang Y, **Hicks SC**, Robinson MD. (2020). [TreeSummarizedExperiment: a S4 class for data with hierarchical structure](https://doi.org/10.12688/f1000research.26669.1). _F1000Research_.


#### Methods to identify differences between groups in single-cell data

These count-based models, such as Poisson or negative binomial, can be generalized using the Tweedie family of distributions, which we used to develop a stastical method to identify differentially expressed genes (1). 

1. Mallick H, Chatterjee Su., Chowdhury S, Chatterjee Sa., Rahnavard A, **Hicks SC**. (2021). [Differential expression of single-cell RNA-seq data using Tweedie models](https://doi.org/10.1101/2021.03.28.437378).  _bioRxiv_.


#### High-grade serous ovarian cancer subtypes with single-cell profiling

The goal of this project is to identify the biological basis of subtypes of high-grade serous ovarian cancers (HGSOC) using bulk and single-cell gene expression data. This is highly relevant to public health because HGSOC is a particularly deadly cancer that is often only identified at late stage and treatment options are limited. The long-term impact of this project will be a key step towards developing targeted treatments for HGSOCs. Most recently, we demonstrated that genetic demultiplexing from single-cell cancer samples can be used for better experimental design and increase cost savings (1). 

1. **Weber LM**, Hippen AA, Hickey PF, Berrett KC, Gertz J, Doherty JA, Greene CS, **Hicks SC**. (2020). [Genetic demultiplexing of pooled single-cell RNA-sequencing samples in cancer facilitates effective experimental design](https://doi.org/10.1101/2020.11.06.371963). _bioRxiv_.


#### Single-nucleus profiling 

Single-nucleus RNA-sequencing (snRNA-seq) has become the preferred experimental technology, compared to scRNA-seq, to profile gene expression in frozen cells or cells that are hard to dissociate, such as brain tissue. Previous studies have shown that snRNA-seq offers substantial advantages over scRNA-seq, including reduced dissociation bias and the ability to capture rare cell types in these tissues (1). 

1. Tran MN, Maynard KR, Spangler A, Collado-Torres L, Sadashivaiah V, Tippani M, Barry BK, Hancock DB, **Hicks SC**, Kleinman JE, Hyde TM, Martinowich K, Jaffe A. (2020). [Single-nucleus transcriptome analysis reveals cell type-specific molecular signatures across reward circuitry in the human brain](https://doi.org/10.1101/2020.10.07.329839). _bioRxiv_.


--- 

# Developing and benchmarking open-source software for genomics data 

In addition to developing statistical methods, I am heavily invested in implementing methods in open-source software for the analysis of genomics data leading to improved reproducibility and understanding of biological data. Bioconductor is an open-source, open-development software project in the R programming language for the analysis and comprehension of high-throughput genomics and molecular biology data. As one of the leaders of the Bioconductor project, I have not only contributed software for the analysis of scRNA-seq data, but also I have led a team of investigators to address a growing need of how to approach single-cell genomic data in a comprehensible way published in _Nature Methods_ (1), which included creating a freely available, [**42-chapter online book**](http://bioconductor.org/books/release/OSCA/) of single-cell methods and tools for prospective users and was highlighted in a _Nature Biotechnology_ [**editorial**](https://www.nature.com/articles/s41587-020-0449-8) in 2020. 

1. Amezquita RA, Lun ATL, Carey VJ, Carpp LN, Geistlinger L, Marini F, Rue-Albrecht K, Risso D, Soneson C, Waldron L, Pages H, Smith M, Huber W, Morgan M, Gottardo R, **Hicks SC**. (2020). [Orchestrating Single-Cell Analysis with Bioconductor](https://doi.org/10.1038/s41592-019-0654-x). _Nature Methods_.

In addition, I evaluate open-source software packages for their accuracy, usability and reproducibility. For example, in high-throughput studies, hundreds to millions of hypotheses are typically tested. Statistical methods that control the false discovery rate (FDR) have emerged as popular and powerful tools for error rate control. While classic FDR methods use only _p_-values as input, more modern FDR methods have been shown to increase power by incorporating complementary information as "informative covariates" to prioritize, weight, and group hypotheses. To address this, we investigated the accuracy, applicability, and ease of use of two classic and six modern FDR-controlling methods by performing a systematic benchmark comparison using simulation studies as well as six case studies in computational biology (2). 

2. Korthauer K, Kimes PK, Duvallet C, Reyes A, Subramanian A, Teng M, Shukla C, Alm EJ, **Hicks SC** (2019). [A practical guide to methods controlling false discoveries in computational biology](https://doi.org/10.1186/s13059-019-1716-1). _Genome Biology_. 

Most recently, we performed a benchmark comparison of 18 scRNA-seq imputation methods across multiple experimental protocols and datasets (3).

3. **Hou W**, Ji J, Ji H, **Hicks SC** (2020). [A systematic evaluation of single-cell RNA-sequencing imputation methods](https://doi.org/10.1186/s13059-020-02132-x). _Genome Biology_.


--- 

# Analysis of high-throughput biological data

### Statistical methods for normalizing and removing biases in high-throughput data

Normalization is an essential step for the analysis of genomics high-throughput data. Quantile normalization is one of the most widely used multi-sample normalization tools for applications including genotyping arrays, RNA-Sequencing (RNA-Seq), DNA methylation, ChIP-Sequencing (ChIP-Seq) and brain imaging. However, quantile normalization relies on assumptions about the data-generation process that are not appropriate in some contexts. To address this, I developed two statistical methods and open-source software for normalizing high-throughput data (1, 2). More recently, I have developed methods and software for correct for and remove compositional biases found in high-throughput DNA methylation data (3) and metagenomic data (4), and co-expression analysis of correlated genes (5). 

1.	**Hicks SC**, Irizarry RA (2015). [quantro: a data-driven approach to guide the choice of an appropriate normalization method](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-015-0679-0). _Genome Biology_.
2.	**Hicks SC**, Okrah K, Paulson JN, Quackenbush J, Irizarry RA, Bravo HC (2018). [Smooth quantile normalization](https://academic.oup.com/biostatistics/article-abstract/19/2/185/3949169). _Biostatistics_.
3. 	**Hicks SC**, Irizarry RA (2019). [methylCC: technology-independent estimation of cell type composition using differentially methylated regions](https://doi.org/10.1186/s13059-019-1827-8). _Genome Biology_.
4.	Kumar MS, Slud EV, Okrah K, **Hicks SC**, Hannenhalli S, Corrada Bravo H (2018). [Analysis and correction of compositional bias in sparse sequencing count data](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-5160-5). _BMC Genomics_. 
5. Wang Y, **Hicks SC**, Hansen KD (2020). [Co-expression analysis is biased by a mean-correlation relationship](https://www.biorxiv.org/content/10.1101/2020.02.13.944777v1). _bioRxiv_.


--- 

# Analysis of genomic data with spatial resolution

Spatially resolved transcriptomics (ST), the [Nature Methods 2020 Method of the Year](https://doi.org/10.1038/s41592-020-01042-x), is poised to transform our understanding of how the spatial organization and communication of cells in complex tissues. These technologies have created an unprecedented opportunity to investigate important biological questions that can only be answered in a spatial context. However, these technologies also brings new statistical, computational and methodological challenges (1). 

1. Righelli D, **Weber LM**, Crowell HL, Pardo B, Collado-Torres L, Ghazanfar S, Lun ATL, **Hicks SC**, Risso D (2021). [SpatialExperiment: infrastructure for spatially resolved transcriptomics data in R using Bioconductor](https://doi.org/10.1101/2021.01.27.428431). _bioRxiv_. 


#### Neuroscience

We were first to apply the 10x Visium spatial transcriptomics technology to human tissue. This is highly relevant to public health because these technologies will provide insights into topographical and pathological changes in gene expression for example in the aging human brain or in patients affected by psychiatric diseases (1). 

1. Maynard KR, Collado-Torres L, **Weber LM**, Uytingco C, Barry BK, Williams SR, II JLC,  Tran MN, Besich Z, Tippani M, Chew J, Yin Y, Kleinman JE, Hyde TM, Rao N, **Hicks SC**, Martinowich K, Jaffe AE (2021). [Transcriptome-scale spatial gene expression in the human dorsolateral prefrontal cortex](https://doi.org/10.1038/s41593-020-00787-0). _Nature Neuroscience_. 

---

# Data Science Education

An increase in demand for statistics and data science education has led to changes in curriculum, specifically an increase in computing. While this has led to more applied courses, students still struggle with effectively deriving knowledge from data and solving real-world problems. In 1999, Deborah Nolan and Terry Speed argued the solution was to teach courses through in-depth case studies derived from interesting scientific questions with nontrivial solutions that leave room for different analyses of the data. This innovative framework teaches the student to make important connections between the scientific question, data and statistical concepts that only come from hands-on experience analyzing data (1, 2). 

#### Open Case Studies 

To address this, I am building the [Open Case Studies](https://www.opencasestudies.org) (OCS) (1) community resource of case studies that educators can use in the classroom to teach students how to effectively derive knowledge from data. This project was selected as a High-Impact Project in 2019-2020 by the Bloomberg American Health Initiative and Bloomberg Philanthropies (2). A list of available cases studies are listed in the [teaching](../teaching/index.html) section. 

1. https://www.opencasestudies.org
2. https://americanhealth.jhu.edu/open-case-studies

<p align="center"><iframe width="560" height="315" src="https://www.youtube.com/embed/DgzBSOY5Yc8" frameborder="0" allowfullscreen></iframe></p>



#### Theory of Data Analysis

The data science revolution has led to an increased interest in the practice of data analysis. While much has been written about _statistical thinking_, a complementary form of thinking that appears in the practice of data analysis is _design thinking_ -- the problem-solving process to understand the people for whom a product is being designed. There can be significant or subtle differences in how a data analyst (or producer of a data analysis) constructs, creates, or designs a data analysis, including differences in the choice of methods, tooling, and workflow. These choices can affect the data analysis products themselves and the experience of the consumer of the data analysis. Therefore, the role of a producer can be thought of as designing the data analysis with a set of design principles (3,4). Our work leads to several insights: it suggests a formal mechanism to describe and evaluate (5) data analyses based on the design principles for data analysis, and it provides a framework to teach students how to build data analyses using formal design principles with an emphasis on reproducible data analyses (6). 

1. **Hicks SC**, Irizarry RA (2018). [A Guide to Teaching Data Science](https://www.tandfonline.com/doi/abs/10.1080/00031305.2017.1356747?journalCode=utas20). _The American Statistician_. 
2. **Hicks SC** (2017). [Greater Data Science Ahead](https://www.tandfonline.com/doi/abs/10.1080/10618600.2017.1385472). _Journal of Computational Graphical Statistics_. 
3. D'Agostino McGowan L, Peng RD, **Hicks SC**. (2021). [Design Principles for Data Analysis](https://arxiv.org/abs/2103.05689). _arXiv_.
4. **Hicks SC**, Peng RD. (2019). [Elements and Principles for Characterizing Variation between Data Analyses](https://arxiv.org/abs/1903.07639). _arXiv_.
5. **Hicks SC**, Peng RD. (2019). [Evaluating the Success of a Data Analysis](https://arxiv.org/abs/1904.11907). _arXiv_.
6.  Peng RD, **Hicks SC**. (2021). [Reproducible Research: A Retrospective](https://doi.org/10.1146/annurev-publhealth-012420-105110). _Annual Review of Public Health_.

