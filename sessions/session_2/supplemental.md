---
layout: page
permalink: sessions/session_2/supplemental
menubar_toc: true
---


## Session 2 supplemental

**Additional GWAS Programs**

**Regenie:**
- Mixed models for population structure and relatedness
- quantitative and binary traits, including binary traits with unbalanced case-control ratios
- multiple phenotypes at once efficiently
- For binary traits, it supports Firth logistic regression and an SPA test
- Fast and memory efficient 
Citation: Mbatchou, J., Barnard, L., Backman, J. et al. Computationally efficient whole-genome regression for quantitative and binary traits. Nat Genet 53, 1097–1103 (2021). https://doi.org/10.1038/s41588-021-00870-7

**SAIGE:**
- Mixed model for sample relatedness and population structure
- Unbalanced Case-Control Sets
- Saddlepoint Approximation (SPA) to handle unbalanced case-control
- Computationally efficient
Citation: Zhou W, Nielsen JB, Fritsche LG, Dey R, Gabrielsen ME, Wolford BN, LeFaive J, VandeHaar P, Gagliano SA, Gifford A, Bastarache LA, Wei WQ, Denny JC, Lin M, Hveem K, Kang HM, Abecasis GR, Willer CJ, Lee S. Efficiently controlling for case-control imbalance and sample relatedness in large-scale genetic association studies. Nat Genet. 2018 Sep;50(9):1335-1341. doi: 10.1038/s41588-018-0184-y. Epub 2018 Aug 13. PMID: 30104761; PMCID: PMC6119127.

**BOLT-LMM:**
- Mixed model association testing
- For analyses of data with > 5,000 samples
- Quantitative Traits and reasonably balanced case/control sets
- Assumes a Bayesian mixture-of-normals prior for the random effect attributed to SNPs other than the one being tested
- Generalizes the standard “infinitesimal” mixed model used by previous mixed model association methods
Citation: Loh, PR., Tucker, G., Bulik-Sullivan, B. et al. Efficient Bayesian mixed-model analysis increases association power in large cohorts. Nat Genet 47, 284–290 (2015). https://doi.org/10.1038/ng.3190

**fastGWA-GLMM**
- Mixed model
- quantitative and binary (even unbalanced)
Citation: https://pubmed.ncbi.nlm.nih.gov/34737426/


###Software for Miami plots and interactive Manhattan!
**Hudson package:** https://github.com/anastasia-lucas/hudson
