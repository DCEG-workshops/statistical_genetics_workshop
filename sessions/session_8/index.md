---
layout: page
permalink: sessions/session_8
---

**Date:** November 18, 2026

**Instructors:** Mitch Machiela, Weiyin Zhou

## Topics Covered

This session introduces genetic mosaicism and clonal hematopoiesis, focusing on mosaic chromosomal alterations (mCAs). Building on the 2023 session, we will address:

- How are mosaic chromosomal alterations detected?
- What risk factors are associated with the development and clonal expansion of mosaic chromosomal alterations?
- Do mosaic chromosomal alterations alter disease risk (e.g., cancer)?

The practical follows a workflow from SNP-array intensity data through contamination checks, genotype phasing, mCA detection, and visualization on Biowulf.

## Learning Objectives

By the end of the session, participants should be able to:

- Describe genetic mosaicism and its relationship to clonal hematopoiesis, aging, and cancer.
- Recognize mosaic gains, deletions, and copy-neutral loss of heterozygosity (CN-LOH), and interpret their intensity and allelic-balance patterns.
- Explain the roles of contamination checks and haplotype phasing in an mCA detection workflow.
- Run the workshop MOChA workflow and interpret event tables, regional plots, and Circos summaries.

## Session Materials

Follow the [practical setup instructions and lab activities]({{ '/sessions/session_8/practical' | relative_url }}) using the [Genetic Mosaicism Practical — Biowulf 2026 notebook (`08_mCA_Biowulf_2026_final.Rmd`)](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/08_mCA_Biowulf_2026_final.Rmd).

## Reading Material

### Suggested Readings

The readings below follow the [2023 Session 8 reading list]({{ '/2023/sessions/session_8.html' | relative_url }}#suggested-readings).

- Jacobs KB, Yeager M, Zhou W, et al. (2012). [Detectable clonal mosaicism and its relationship to aging and cancer](https://pubmed.ncbi.nlm.nih.gov/22561519/). *Nature Genetics*, 44, 651–658.
- Laurie CC, Laurie CA, Rice K, et al. (2012). [Detectable clonal mosaicism from birth to old age and its relationship to cancer](https://pubmed.ncbi.nlm.nih.gov/22561516/). *Nature Genetics*, 44, 642–650.
- Vattathil S, Scheet P. (2016). [Extensive Hidden Genomic Mosaicism Revealed in Normal Tissue](https://pubmed.ncbi.nlm.nih.gov/26942289/). *American Journal of Human Genetics*, 98, 571–578.
- Loh PR, Genovese G, Handsaker RE, et al. (2018). [Insights into clonal haematopoiesis from 8,342 mosaic chromosomal alterations](https://pubmed.ncbi.nlm.nih.gov/29995854/). *Nature*, 559, 350–355.

### Software and Method Resources

- [gtc2vcf](https://github.com/freeseek/gtc2vcf): tools to convert Illumina intensity data to VCF/BCF.
- [MOChA](https://github.com/freeseek/mocha): haplotype-based detection of mosaic chromosomal alterations.
- [MOChA WDL pipelines](https://github.com/freeseek/mochawdl): workflow implementations for mCA analysis.
- [EAGLE2](https://alkesgroup.broadinstitute.org/Eagle/): genotype phasing used in the 2026 practical.
- [SHAPEIT4](https://odelaneau.github.io/shapeit4/): an additional phasing resource from the 2023 reading list.
