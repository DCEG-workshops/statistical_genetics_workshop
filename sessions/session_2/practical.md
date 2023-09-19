---
layout: page
permalink: sessions/session_2/practical
menubar_toc: true
---

<script link="{{ site.baseurl }}/assets/js/vanilla-back-to-top.min.js"></script>
<script>addBackToTop()</script
<script src="{{ site.baseurl }}/assets/js/copyCodeSnippet.js" defer></script>
<script src="{{ site.baseurl }}/assets/js/copyCodeBlock.js" defer></script>

## Practical session 2
#### Basic GWAS analyses

This workshop deploys a precoded Jupyter notebook through Google Colaboratory to perform Genome Wide Association Studies (GWAS) using Plink. We will also explore data visualization of the GWAS results using the R package qqman. Lastly, we will deploy Metasoft for a quick meta-analysis tutorial.  

### Objectives
- To perform a basic GWAS using linear and logistic regression.
- To display simple visualization of GWAS results and post GWAS QC.
- To provide additional considerations and for deploying GWAS in real studies.
- To provide a simple meta-analysis example and results.
- 
### Prerequisites
Before starting this workshop, we recommend that you have:

A Google Account
Completed Workshop #1 and been introduced to the usage of Google Colab, PLINK software, and data QC.
A basic understanding of genetics, genome-wide association studies (GWAS), and the role of quality control (QC) in GWAS.
Familiarity with command-line tools and basic R programming, as we will use the command-line tool plink and R for visualization.

### Workshop Overview
We’ll begin with introducing the available data and verifying connection to the google drive. Then we will proceed to deploy PLINK software and use it for linear and logistic regression. We will follow-up our GWAS results with QQplots and Manhattan plots.  We will perform some web exploration of publicly available tools to look at any interesting results from our GWAS.  Following the GWAS sections and exploration, we will pivot to perform a Meta-Analysis.

We use two data sources in this workshop:
1) GWAS: PennCATH study of coronary artery disease. It includes 1,401 individuals with 861,473 markers and has been made available publicly.
2) Meta-Analysis: Breast Cancer Association Consortium (BCAC) data from 3 different GWAS arrays that has summary statistics and meta-analysis results available publicly. 

### Let's Get Started
Please go ahead and open the 03_GWAS&MetaAnalysis Notebook in Google Colab
