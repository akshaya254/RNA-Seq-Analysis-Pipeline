This repository contains the R Markdown script for analyzing the transcriptomic response to SARS-CoV-2 infection in human eye tissues. The primary objective is to identify differentially expressed genes in SARS-CoV-2 infected samples compared to mock samples, while accounting for tissue-specific differences.

ANALYSIS WORKFLOW -
The pipeline executed in rnaseq_analysis.Rmd follows these steps:   
1. Data Retrieval: Downloading GEO metadata and the raw count matrix.
2. Data Preprocessing: Cleaning the count matrix and creating sample metadata.
3. Differential Expression: Running DESeq2, using the design formula ~ tissue + infection.
4. Visualization: Generating PCA plots, sample-to-sample distance heatmaps, MA plots, and heatmaps for the top 50 differentially expressed genes.
5. Gene Mapping: Converting gene identifiers to gene symbols and Entrez IDs using org.Hs.eg.db.
6. Enrichment Analysis: Performing Gene Ontology (GO) and Reactome pathway enrichment analysis.
7. GSEA: Executing Gene Set Enrichment Analysis using MSigDB human Hallmark gene sets.
8. Quality Control: Summarizing raw read quality using FastQC and MultiQC.

DEPENDENCIES -
This analysis requires R and the following packages:   
- GEOquery
- DESeq2
- tidyverse & dplyr
- ggplot2 & pheatmap
- RColorBrewer
- AnnotationDbi & org.Hs.eg.db
- clusterProfiler, enrichplot, & ReactomePA
- msigdbr   
