---
layout: page
permalink: sessions/session_2
---

**Date:** September 16, 2026

**Instructors:** Peter Kraft, Xueyao Wu

## Topics Covered

This session builds on the data management and quality control introduced in Session 1. We will cover how to test genetic associations, assess GWAS results, and combine evidence across studies, followed by hands-on exercises using REGENIE and METASOFT.

### Lecture

- Association models for quantitative, binary, and time-to-event outcomes; additive genetic effects and mixed models.
- Covariate selection, population stratification, and potential bias from inappropriate adjustment.
- Multiple testing and genome-wide significance.
- QQ plots, genomic inflation, Manhattan plots, and regional association plots.
- Genotype imputation, fixed- and random-effects meta-analysis, heterogeneity, and analysis across ancestry groups.
- Variant annotation and the challenges of moving from an associated region to a causal variant or gene.

### Practical

1. **Basic GWAS with REGENIE:** Analyze a simulated quantitative trait and coronary artery disease status in PennCATH data. Use supplied leave-one-chromosome-out (LOCO) predictions, run association tests, and examine diagnostic plots. A take-home exercise compares the results with PLINK regression.
2. **Meta-analysis with METASOFT:** Combine prepared BCAC2017 breast-cancer GWAS summary statistics from AFR, ASN, and EUR ancestry strata at the TERT region. Compare fixed-effect, conventional random-effects, and RE2 results, and interpret heterogeneity, forest plots, and M-values.

## Learning Objectives

By the end of this session, participants should be able to:

- Choose association models and covariates appropriate to the phenotype and study design.
- Interpret GWAS effect estimates, significance, and diagnostic plots in the context of QC and population structure.
- Explain the purpose of REGENIE's two-step approach and LOCO adjustment.
- Compare meta-analysis methods and assess differences in association evidence across studies or ancestry strata.

## Session Materials

- [Lecture slides and PDF download]({{ '/sessions/session_2/lecture' | relative_url }})
- [Practical notebooks, software requirements, and setup instructions]({{ '/sessions/session_2/practical' | relative_url }})

Before the session, review [Session 1's QC practical]({{ '/sessions/session_1/practical' | relative_url }}) and check the Session 2 software requirements before launching RStudio on NIH HPC OnDemand.
