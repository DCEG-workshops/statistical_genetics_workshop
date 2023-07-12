---
layout: page
permalink: sessions/session_1/practical
menubar_toc: true
---
<script src="{{ site.baseurl }}/assets/js/vanilla-back-to-top.min.js"></script>
<script>addBackToTop()</script>

<script src="{{ site.baseurl }}/assets/js/copyCodeSnippet.js" defer></script>
<script src="{{ site.baseurl }}/assets/js/copyCodeBlock.js" defer></script>

Description of the practical section 

---

This workshop was designed to provide a quick introduction to GWAS QC using plink. Here, we will walk you through the process of using plink to conduct various QC steps for GWAS.

---

## Objectives

- To introduce participants the importance of Quality Control in the analysis pipeline.
- To provide participants with the basic practical skills needed to perform QC of GWAS data using plink.

## Prerequisites

Before starting this workshop, we recommend that you have:

- A basic understanding of genetics, genome-wide association studies (GWAS), and the role of quality control (QC) in GWAS.
- Familiarity with command-line tools, as we will use the command-line tool plink for the QC steps.


## Workshop Overview

We'll begin with introducing the usage of Jupyter notebook and a brief overview of the PLINK software and its key features.   We'll then dive into the hands-on component of the workshop, where you'll learn how to perform several essential QC procedures, the steps are as follows. The jupyter notebook for this workshop is also provided in [here](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/01_plink_QC.ipynb).

The data that we used in this workshop are the small variants from chromosome 21 from the 1000 genomes project. The pre-processing of the data is recorded in [this jupyter notebook](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/00_setup_data.ipynb)

### Step 1: Check sample and SNP missingness
### Step 2: Check Sex discrepancy
### Step 3: Filter by Minor allele frequency (MAF)
### Step 4: Filter markers that deviate from Hardy-Weinberg Equilibuium
### Step 4: Filter samples based on heterzygocity
### Step 5: Identify (and optionally filter) on estimated relatedness
### Step 6: Population stratification and batch effects

## References

For further reading, we recommend:

1. PLINK 1.9: [Website](https://www.cog-genomics.org/plink/1.9/)
2. Purcell S, Neale B, Todd-Brown K, et al. PLINK: A Tool Set for Whole-Genome Association and Population-Based Linkage Analyses. Am J Hum Genet. 2007;81(3):559-575. [Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1950838/)
3. Anderson CA, Pettersson FH, Clarke GM, Cardon LR, Morris AP, Zondervan KT. Data quality control in genetic case-control association studies. Nat Protoc. 2010;5(9):1564-1573. [Link](https://pubmed.ncbi.nlm.nih.gov/21085122/)
