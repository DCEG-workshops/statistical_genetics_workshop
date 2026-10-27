---
layout: page
permalink: sessions/session_6
---

**Date:** October 28, 2026

**Instructor:** Haoyu Zhang

## Topics Covered

This session introduces polygenic risk scores (PRS), which combine GWAS effect estimates across genetic variants to summarize genetic predisposition to a trait. We will compare clumping and thresholding (C+T) with LDpred2, examining how the methods use linkage disequilibrium (LD), align effect alleles, and select model settings. We will also discuss the separation of tuning and validation samples, interpretation of predictive performance, and limitations when scores are transferred across populations.

The [practical tutorial]({{ '/sessions/session_6/practical' | relative_url }}) uses chromosome 22 GWAS summary statistics, a European 1000 Genomes LD reference, simulated target genotypes, and a quantitative outcome. Participants will use PLINK and R to select a C+T threshold and an LDpred2 model in 10,000 tuning samples, then compare the selected scores in 10,000 separate validation samples using R-squared. This teaching example illustrates score construction and evaluation; it does not estimate clinical performance or establish a general ranking of the two methods.

## Learning Objectives

By the end of the session, participants should be able to:

- Explain how GWAS effect estimates and effect-allele counts contribute to a PRS.
- Describe the roles of allele alignment, variant QC, and an appropriate LD reference.
- Construct C+T scores at multiple p-value thresholds and fit a small LDpred2 parameter grid.
- Select settings using tuning samples and evaluate the selected scores in separate validation samples.
- Recognize why validation R-squared does not establish calibration, clinical utility, or portability to another population.

## Reading Material

### Essential reading

1. Choi SW, Mak TS-H, O'Reilly PF. (2020). [Tutorial: a guide to performing polygenic risk score analyses](https://doi.org/10.1038/s41596-020-0353-1). *Nature Protocols*, 15, 2759–2772. A practical introduction to quality control, score construction, and interpretation. [Free full text](https://pmc.ncbi.nlm.nih.gov/articles/PMC7612115/).
2. Privé F, Arbel J, Vilhjálmsson BJ. (2020). [LDpred2: better, faster, stronger](https://doi.org/10.1093/bioinformatics/btaa1029). *Bioinformatics*, 36, 5424–5431. Read the abstract and Section 4.1 for the differences between LDpred2-inf, LDpred2-grid, and LDpred2-auto; this practical uses LDpred2-grid. [Free full text](https://pmc.ncbi.nlm.nih.gov/articles/PMC8016455/).
3. Privé F. [Polygenic scores and inference using LDpred2](https://privefl.github.io/bigsnpr/articles/LDpred2.html). Official `bigsnpr` tutorial. Focus on required inputs, allele matching, the LD reference, and LDpred2-grid; use this as a reference alongside the workshop notebook.

### Further reading

4. Wand H, Lambert SA, Tamburro C, et al. (2021). [Improving reporting standards for polygenic scores in risk prediction studies](https://doi.org/10.1038/s41586-021-03243-6). *Nature*, 591, 211–219. A framework for documenting study populations, score development, validation, performance, and limitations. [Free full text](https://pmc.ncbi.nlm.nih.gov/articles/PMC8609771/).
5. Martin AR, Kanai M, Kamatani Y, et al. (2019). [Clinical use of current polygenic risk scores may exacerbate health disparities](https://doi.org/10.1038/s41588-019-0379-x). *Nature Genetics*, 51, 584–591. Background for discussing why scores developed using European discovery and reference data may not transfer equally across populations. [Free full text](https://pmc.ncbi.nlm.nih.gov/articles/PMC6563838/).
