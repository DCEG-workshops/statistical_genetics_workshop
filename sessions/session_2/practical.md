---
layout: page
permalink: sessions/session_2/practical
menubar_toc: true
---

## Tutorial notebooks

Work through these R Markdown notebooks in order. Both are available in the [tutorial repository's `src` folder](https://github.com/DCEG-workshops/statgen_workshop_tutorial/tree/main/src).

| Part | Notebook | Focus |
| --- | --- | --- |
| 2a | [Basic GWAS with REGENIE (`02a_gwas.Rmd`)](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/02a_gwas.Rmd) | Quantitative- and binary-trait association testing using PennCATH data |
| 2b | [Cross-Ancestry GWAS Meta-Analysis with METASOFT (`02b_meta_analysis.Rmd`)](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/02b_meta_analysis.Rmd) | Combining BCAC2017 summary statistics at the TERT locus |

## Objectives

- Understand REGENIE's two-step whole-genome regression approach and leave-one-chromosome-out (LOCO) predictions.
- Run association tests for a simulated quantitative trait and coronary artery disease (CAD) status, and interpret QQ plots, Manhattan plots, and genomic inflation.
- Compare REGENIE with PLINK's single-marker regression in a take-home exercise.
- Inspect harmonized summary statistics and compare fixed-effect, conventional random-effects, and Han–Eskin RE2 meta-analysis.
- Use heterogeneity statistics, forest plots, and M-values to interpret results across ancestry strata.

## Prerequisites and setup

- Complete [Session 1]({{ '/sessions/session_1' | relative_url }}), or be familiar with PLINK, GWAS QC, and principal-component adjustment.
- Have an active Biowulf account and launch RStudio through [NIH HPC OnDemand](https://hpcondemand.nih.gov). See the [Session 1 setup instructions]({{ '/sessions/session_1/practical' | relative_url }}#launch-rstudio-on-hpc-ondemand).
- **Load REGENIE 4.0 and PLINK 1.9 before starting the OnDemand RStudio session.** Confirm their availability using the checks in notebook 2a.
- Have the R packages used by the notebooks available: `tidyverse`, `data.table`, `glue`, `qqman`, `ggplot2`, and `scales`.
- For notebook 2b, confirm Java is available. The notebook includes commands to download, install, and test METASOFT 2.0.1 in your analysis directory.

The notebooks use prepared workshop inputs under `/data/DCEG_shared/statgen_workshop_2026/data/workshop2/`: `gwas` for part 2a and `meta_analysis` for part 2b. Their setup chunks create separate output directories under `/data/$USER/Stats_Gen/workshop2/02a_analysis` and `/data/$USER/Stats_Gen/workshop2/02b_analysis`. Run the setup chunks first to define the paths used by the R and Bash chunks.

## Part 2a: Basic GWAS with REGENIE

Using the PennCATH dataset introduced in Session 1, we will:

1. Review the prepared phenotypes, ten genetic principal components, and trait-specific sample lists.
2. Prune the genotype data for Step 1, subset samples for each trait, and investigate extreme heterozygosity and HWE filtering.
3. Examine Step 1 LOCO predictions, which account for polygenic effects from the other chromosomes.
4. Run Step 2 association tests for the simulated quantitative trait and CAD, including selective approximate Firth correction for CAD.
5. Summarize association statistics, calculate genomic inflation, create QQ and Manhattan plots, and identify genome-wide significant variants.

**Class-time shortcut:** Step 1 fitting chunks are marked `eval=FALSE`, and prepared Step 1 predictions are provided. The supplied Step 2 commands use those shared predictions; follow the notebook's precomputed-output workflow during class.

**Take-home exercise:** Run PLINK 1.9 linear and logistic regression on the same filtered data and covariates, then compare effect estimates and p-values with REGENIE. Discuss the role of LOCO adjustment and Firth correction in any differences.

## Part 2b: Cross-Ancestry Meta-Analysis with METASOFT

This exercise uses a prepared **TERT region on chromosome 5 (GRCh37)** from BCAC2017 breast-cancer GWAS summary statistics. AFR, ASN, and EUR are the ancestry-stratum labels in the input files.

1. Inspect aligned effect alleles, beta/standard-error pairs, and missing data in the prepared summary statistics.
2. Install METASOFT and run its bundled example.
3. Run fixed-effect, conventional random-effects, and RE2 analyses, then calculate M-values.
4. Parse and annotate the results; compare fixed-effect and RE2 association evidence.
5. Examine Cochran's Q and I², regional association plots, forest plots, and an M-value heatmap.

**Interpretation:** Cross-stratum meta-analysis requires at least two available beta/standard-error pairs. M-values are posterior probabilities under METASOFT's model and priors. Differences across strata can reflect sampling variation, linkage disequilibrium, allele frequency, imputation quality, or study design; interpret them alongside the underlying effect estimates.

## External resources

- [REGENIE documentation](https://rgcgithub.github.io/regenie/)
- [PLINK 1.9 documentation](https://www.cog-genomics.org/plink/1.9/)
- [METASOFT tutorial and downloads](https://hanlab-snu.github.io/METASOFT/)
