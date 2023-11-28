---
layout: page
permalink: sessions/session_7
---

### Lecture overview
- Population-specific and trans-ancestry GWAS
- Multi-population fine-mapping
- PRS construction
- PRS evaluation across populations
- Absolute risk across populations

### Practical:

- Perform multi-population fine-mapping
- Perform multi-population PRS construction using PRS-CSx
- Perform multi-population PRS evaluation

#### Data Used:
- Summary statistics from Wang et. al. [https://pubmed.ncbi.nlm.nih.gov/37945903/](https://pubmed.ncbi.nlm.nih.gov/37945903/)
- PRS evaluation: subset of data from [https://www.ncbi.nlm.nih.gov/projects/gap/cgi-bin/study.cgi?study_id=phs001081.v2.p2](https://www.ncbi.nlm.nih.gov/projects/gap/cgi-bin/study.cgi?study_id=phs001081.v2.p2) and will be updated and available for the Multiethnic Cohort on dbGaP.

#### Programs Used:
- mJAM (program link and corresponding papers):
    - latest CRAN link: [https://cran.r-project.org/web/packages/hJAM/index.html](https://cran.r-project.org/web/packages/hJAM/index.html)
    - https://www.biorxiv.org/content/10.1101/2022.12.22.521659v1
    - Lai Jiang, Shujing Xu, Nicholas Mancuso, Paul J. Newcombe, David V. Conti (2020). "A Hierarchical Approach Using Marginal Summary Statistics for Multiple Intermediates in a Mendelian Randomization or Transcriptome Analysis.” https://pubmed.ncbi.nlm.nih.gov/33404048/ 
    - Jiayi Shen, Lai Jiang, Kan Wang, Anqi Wang, Fei Chen, Paul J. Newcombe, Christopher A. Haiman, David V. Conti “Fine-Mapping and Credible Set Construction using a Multi-population Joint Analysis of Marginal Summary Statistics from Genome-wide Association Studies” https://www.biorxiv.org/content/10.1101/2022.12.22.521659v1.full.pdf 
- COJO:
    - https://yanglab.westlake.edu.cn/software/gcta/#COJO
    - Yang et al. (2012) Conditional and joint multiple-SNP analysis of GWAS summary statistics identifies additional variants influencing complex traits. Nat Genet 44(4):369-375.
- msCAVIAR:
    - https://github.com/nlapier2/MsCAVIAR
    - Identifying Causal Variants by Fine Mapping Across Multiple Studies
    - Nathan LaPierre, Kodi Taraszka, Helen Huang, Rosemary He, Farhad Hormozdiari, Eleazar Eskin (2021) PLOS Genetics.
- PRS-CSx
    - https://github.com/getian107/PRScsx
    - Y Ruan, YF Lin, YCA Feng, CY Chen, M Lam, Z Guo, Stanley Global Asia Initiatives, L He, A Sawa, AR Martin, S Qin, H Huang, T Ge. Improving polygenic prediction in ancestrally diverse populations. Nature Genetics, 54:573-580, 2022.

### Suggested Readings

- Zaitlen, N., Paşaniuc, B., Gur, T., Ziv, E., & Halperin, E. (2010). Leveraging genetic variability across populations for the identification of causal variants. American Journal of Human Genetics, 86(1), 23–33. [https://doi.org/10.1016/j.ajhg.2009.11.016](https://doi.org/10.1016/j.ajhg.2009.11.016)
- Wang, A., Shen, J., Rodriguez, A. A., Saunders, E. J., Chen, F., Janivara, R., Darst, B. F., Sheng, X., Xu, Y., Chou, A. J., Benlloch, S., Dadaev, T., Brook, M. N., Plym, A., Sahimi, A., Hoffman, T. J., Takahashi, A., Matsuda, K., Momozawa, Y., … Haiman, C. A. (2023). Characterizing prostate cancer risk through multi-ancestry genome-wide discovery of 187 novel risk variants. Nature Genetics. [https://doi.org/10.1038/s41588-023-01534-4](https://doi.org/10.1038/s41588-023-01534-4)
- Martin, A. R., Kanai, M., Kamatani, Y., Okada, Y., Neale, B. M., & Daly, M. J. (2019). Clinical use of current polygenic risk scores may exacerbate health disparities. Nature Genetics, 51(4), 584–591. [https://doi.org/10.1038/s41588-019-0379-x](https://doi.org/10.1038/s41588-019-0379-x)