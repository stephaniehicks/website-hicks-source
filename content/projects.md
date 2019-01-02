---
title: "Projects"
date: "2019-01-02"
---


### Data Science Education

An increase in demand for statistics and data science education has led to changes in curriculum, specifically an increase in computing. While this has led to more applied courses, students still struggle with effectively deriving knowledge from data and solving real-world problems. In 1999, Deborah Nolan and Terry Speed argued the solution was to teach courses through in-depth case studies derived from interesting scientific questions with nontrivial solutions that leave room for different analyses of the data. This innovative framework teaches the student to make important connections between the scientific question, data and statistical concepts that only come from hands-on experience analyzing data (1, 2). To address this, I am building the [openDataCases](https://github.com/opencasestudies) community resource of case studies that educators can use in the classroom to teach students how to effectively derive knowledge from data. 

I have also developed course material and videos for a series of data analysis for genomics courses at Harvard edX. I actively create and maintain software packages using the R programming language and is the co-founder of the R-Ladies Baltimore chapter for promoting gender diversity in the R community. 


1. Hicks SC, Irizarry RA (2018). [A Guide to Teaching Data Science](https://www.tandfonline.com/doi/abs/10.1080/00031305.2017.1356747?journalCode=utas20). _The American Statistician_. 
2. Hicks SC (2017). [Greater Data Science Ahead](https://www.tandfonline.com/doi/abs/10.1080/10618600.2017.1385472). _Journal of Computational Graphical Statistics_. 



### Statistical methods for high-throughput data

Normalization is an essential step for the analysis of genomics high-throughput data. Quantile normalization is one of the most widely used multi-sample normalization tools for applications including genotyping arrays, RNA-Sequencing (RNA-Seq), DNA methylation, ChIP-Sequencing (ChIP-Seq) and brain imaging. However, quantile normalization relies on assumptions about the data-generation process that are not appropriate in some contexts. I developed a data-driven method to test these assumptions and guide the choice of an appropriate normalization method (1). The freely available software (2) has been downloaded over 7500 times (distinct IPs) from Bioconductor since 2014 and has helped researchers test the assumptions of global normalization methods in the analysis of their own data. To address the scenario when the assumptions of quantile normalization are not appropriate, I have developed a generalization of quantile normalization, referred to as smooth quantile normalization, which allows for global differences between biological groups (3). More recently, I collaborated with researchers from the University of Maryland to correct for compositional biases found in sparse metagenomic sequencing data (4). 

1.	Hicks SC, Irizarry RA (2015). [quantro: a data-driven approach to guide the choice of an appropriate normalization method](https://genomebiology.biomedcentral.com/articles/10.1186/s13059-015-0679-0). _Genome Biology_.
2.	Hicks S, Irizarry R (2014). [quantro: A test for when to use quantile normalization](https://bioconductor.org/packages/release/bioc/html/quantro.html). 
3.	Hicks SC, Okrah K, Paulson JN, Quackenbush J, Irizarry RA, Bravo HC (2018). [Smooth quantile normalization](https://academic.oup.com/biostatistics/article-abstract/19/2/185/3949169?redirectedFrom=fulltext). _Biostatistics_. 
4.	Kumar MS, Slud EV, Okrah K, Hicks SC, Hannenhalli S, Corrada Bravo H (2018). [Analysis and correction of compositional bias in sparse sequencing count data](https://bmcgenomics.biomedcentral.com/articles/10.1186/s12864-018-5160-5). _BMC Genomics_. 


### Statistical methods for single-cell RNA-Sequencing

I work with single-cell RNA-Sequencing (scRNA-seq) data, which has become the most widely used high-throughput method for transcription profiling of individual cells. This technology has created an unprecedented opportunity to investigate important biological questions that can only be answered at the single-cell level. However, this technology also brings new statistical, computational and methodological challenges. In contrast to bulk RNA-seq experiments, the majority of reported expression levels in scRNA-seq data are zeros, which could be either biologically-driven, genes not expressing RNA at the time of measurement, or technically-driven, genes expressing RNA, but not at a sufficient level to be detected by sequencing technology. In addition, systematic errors, including batch effects, have been widely reported as a major challenge in high-throughput technologies, however, surprisingly, these issues have received minimal attention in published studies based on scRNA-seq technology. To investigate this, I examined data from fifteen published scRNA-seq studies and demonstrated that systematic errors can explain a substantial percentage of observed cell-to-cell expression variability, which in turn can lead to false discoveries, for example, when using unsupervised learning methods (1). More recently, we developed a dimensionality reduction method, Varying-censoring Aware Matrix Factorization (VAMF), which permits the identification of low-dimensional representations of cells in the presence of cell-specific censoring. This allows for the correction for batch effects if they are mediated through a varying censoring mechanism in either confounded or unconfounded study designs, which is not possible using standard batch correction methods (2).

1.	Hicks SC, Townes FW, Teng M, Irizarry RA (2018). [Missing data and technical variability in single-cell RNA-sequencing experiments](https://academic.oup.com/biostatistics/article/19/4/562/4599254). _Biostatistics_. 
2.	Townes FW, Hicks SC, Aryee MJ, Irizarry RA (2017). [Varying-Censoring Aware Matrix Factorization for Single Cell RNA-Sequencing](https://www.biorxiv.org/content/early/2017/07/21/166736). _bioRxiv_. 



