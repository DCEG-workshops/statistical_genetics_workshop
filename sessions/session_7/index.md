---
layout: page
permalink: sessions/session_7
---

**Date:** November 4, 2026

**Instructor:** Diptavo Dutta

## Topics Covered

This session introduces rare genetic variants and the use of exome and whole-genome sequencing to study them. We will discuss gene-based association tests, including burden tests and the sequence kernel association test (SKAT), as well as approaches for non-coding variants and incorporating functional annotations. The practical uses simulated data to explore how variant frequencies, carrier status, and the direction of variant effects influence gene-level tests.

## Learning Objectives

By the end of the session, participants should be able to:

- Explain why rare variants are often analyzed together within a gene or other variant set.
- Compare burden tests and SKAT, including how they respond to effects in opposite directions.
- Inspect rare-variant data and interpret covariate-adjusted gene-level tests with multiple-testing correction.
- Distinguish binary carrier status from a weighted dosage burden and interpret the simulated examples.

## Session Materials

- **Lecture:** [View the lecture page]({{ '/sessions/session_7/lecture' | relative_url }}) or [download the slides (PDF)]({{ '/sessions/session_7/assets/Rare_var_v3.pdf' | relative_url }}).
- **Practical:** Follow the [setup instructions and lab activities]({{ '/sessions/session_7/practical' | relative_url }}) using the [Rare Variants R script (`07_rare_variants.R`)](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/07_rare_variants.R).

## Reading Material

### Background

Gibson G. (2012). [Rare and common variants: twenty arguments](https://pubmed.ncbi.nlm.nih.gov/22251874/). *Nature Reviews Genetics*, 13, 135–145.

### WES generation methods

Lee S, Abecasis GR, Boehnke M, Lin X. (2014). [Rare-variant association analysis: study designs and statistical tests](https://pubmed.ncbi.nlm.nih.gov/24995866/). *American Journal of Human Genetics*, 95, 5–23.

### Additional methods and concepts

Povysil G, et al. (2019). [Rare-variant collapsing analyses for complex traits: guidelines and applications](https://www.nature.com/articles/s41576-019-0177-4). *Nature Reviews Genetics*, 20, 747–759.
