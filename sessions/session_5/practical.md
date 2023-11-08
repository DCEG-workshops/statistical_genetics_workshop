---
layout: page
permalink: sessions/session_5/practical
menubar_toc: true
---

<script link="{{ site.baseurl }}/assets/js/vanilla-back-to-top.min.js"></script>
<script>addBackToTop()</script
<script src="{{ site.baseurl }}/assets/js/copyCodeSnippet.js" defer></script>
<script src="{{ site.baseurl }}/assets/js/copyCodeBlock.js" defer></script>

## Practical session 

This workshop will explore rare variant analysis using the [STAAR pipeline](https://github.com/xihaoli/STAARpipeline). 

## Practical Overview:

- Rare variant association analysis of WGS data
- WGS data preparation and annotation
- PC / Sparse Genetic Relatedness Matrix (GRM) generation
- Functionally-informed rare variant association analysis
- Conditional analysis
- Annotating rare variant analysis results

## Practical Goals:
- To prepare 1000G WGS data in a Genomic Data Structure (GDS) format
- To functionally annotate 1000G WGS data into an annotated GDS (aGDS) format
- To generate ancestral principal components and sparse GRM (using FastSparseGRM)
- To perform a functionally-informed rare variant analysis using linear mixed model
- To perform conditional analysis for a significant rare variant set (mask) of interest
- To annotate a significant rare variant set (mask) of interest

## Data Used
- 1000G High Coverage WGS: https://pubmed.ncbi.nlm.nih.gov/36055201/
- 1000G Phase 3: https://www.nature.com/articles/nature15393
- 1000G Original: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3498066/

## Programs Used
- GDS: https://academic.oup.com/bioinformatics/article/33/15/2251/3072873
- aGDS: https://academic.oup.com/nar/article/51/D1/D1300/6814464
- FastSparseGRM: https://github.com/rounakdey/FastSparseGRM
- STAARpipeline: https://www.nature.com/articles/s41592-022-01640-x  

### Workshop Material
Due to the time and resource limit of the workshop, we are not going to do a live demo of the preprocessing steps. Please refer to the [README.md file](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/05_RareVariants/README.md) for the precoessing steps and the [1000G_scripts_part1 folder](https://github.com/DCEG-workshops/statgen_workshop_tutorial/tree/main/src/05_RareVariants/1000G/1000G_scripts_part1) for the preprocessing steps. 

In this workshop, we will be focusing on the R scripts in [1000G_scripts_part2](
https://github.com/DCEG-workshops/statgen_workshop_tutorial/tree/main/src/05_RareVariants/1000G/1000G_scripts_part2)

### Let's get started 
Please go ahead and open the [05_RareVariants.ipynb](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/05_RareVariants.ipynb) Google colab notebook. 
