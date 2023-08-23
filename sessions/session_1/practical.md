---
layout: page
permalink: sessions/session_1/practical
menubar_toc: true
---
<script src="{{ site.baseurl }}/assets/js/vanilla-back-to-top.min.js"></script>
<script>addBackToTop()</script>

<script src="{{ site.baseurl }}/assets/js/copyCodeSnippet.js" defer></script>
<script src="{{ site.baseurl }}/assets/js/copyCodeBlock.js" defer></script>


---

This workshop offers an introduction to utilizing Jupyter notebooks through [Google Colaboratory](https://colab.google/). Additionally, it serves as a quick guide to GWAS QC with PLINK. We'll guide you step by step in using PLINK and R to carry out various QC procedures for Genome-Wide Assoication Studies(GWAS).

---

## Objectives

- To introduce the Google Colaboratory platform.
- To introduce participants the importance of Quality Control in the analysis pipeline.
- To provide participants with the basic practical skills needed to perform QC of GWAS data using plink.

## Prerequisites

Before starting this workshop, we recommend that you have:

- A Google Account 
- A basic understanding of genetics, genome-wide association studies (GWAS), and the role of quality control (QC) in GWAS.
- Familiarity with command-line tools, as we will use the command-line tool plink for the QC steps.


## Workshop Overview

We'll begin with introducing the usage of Google Colab and a brief overview of the PLINK software and its key features.   We'll then dive into the hands-on component of the workshop, where you'll learn how to perform several essential QC procedures.

The data that we used in this workshop is from 

### Run standard QC steps using Colab
Please go ahead and open the [QC Notebook](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/01_qc.ipynb) in Google Colab


### Get access to the data in Shared Google Drive
For this workshop, we'll be storing the data on Google Drive. Please consult the [notebook](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/01_qc.ipynb) for guidance on accessing the data. Alternatively, you can also execute this notebook in a Jupyter environment, remember to download the data to a location accessible by the Jupyter server and modify the data path variables accordingly.

### QC Steps
Please refer to the notebook for more details. In short, we would like to: 
- Check sample and SNP missingness
- Identify markers that deviate from Hardy-Weinberg Equilibuium
- Check heterzygosity on the samples
- Check estimated IBD and relatedness on the samples
- Population stratification and batch effects 

### Assign ancestry to samples using GrafPop
Please go ahead and open the [Ancestry Notebook](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/02_ancestry.ipynb) in Google Colab 


## References

For further reading, we recommend:

1. PLINK 1.9: [Website](https://www.cog-genomics.org/plink/1.9/)
2. Purcell S, Neale B, Todd-Brown K, et al. PLINK: A Tool Set for Whole-Genome Association and Population-Based Linkage Analyses. Am J Hum Genet. 2007;81(3):559-575. [Link](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC1950838/)
3. Anderson CA, Pettersson FH, Clarke GM, Cardon LR, Morris AP, Zondervan KT. Data quality control in genetic case-control association studies. Nat Protoc. 2010;5(9):1564-1573. [Link](https://pubmed.ncbi.nlm.nih.gov/21085122/)
