---
layout: page
permalink: sessions/session_1/supplemental
menubar_toc: true
---


## Using workflow languages to manage the GWAS QC workflow

In practice, we should be using workflow languages to manage the GWAS QC procedures. First, it ensures reproducibility, a fundamental aspect in scientific research, by documenting the sequence of steps and parameters used. This not only aids in validation by other researchers but also makes it easier for the original researchers to replicate their results or adapt the workflow for future studies. Second, workflow languages allow for efficient automation and scaling of processes, accommodating the large datasets typical of GWAS. This automation reduces the risk of manual errors and streamlines the analysis. Lastly, by defining the workflow in a language designed for this purpose, researchers can benefit from better error handling, logging, and even resource allocation, ensuring that the QC process is both robust and efficient.

There are a few popular bioinformatics workflow languages, such as Nextflow, Snakemake, and WDL. There are GWAS QC workflow written in each of these workflow lanaguages available on GitHub:

- Nextflow:
    - [H3AGWAS](https://github.com/h3abionet/h3agwas/): This workflow included both QC, imputaiton and association analysis
- Snakemake:
    - [GwasQcPipeline](https://github.com/NCI-CGR/GwasQcPipeline): The DCEG CGR GWAS QC processing workflow
- WDL:
    - [qc_imputation](https://github.com/FINNGEN/qc_imputation): The Finngen GWAS QC/imputation pipeline    



## References:

Brandenburg, J.-T., Clark, L., Botha, G., Panji, S., Baichoo, S., Fields, C., & Hazelhurst, S. (2022). H3AGWAS: a portable workflow for genome wide association studies. BMC Bioinformatics, 23(1), 498. https://doi.org/10.1186/s12859-022-05034-w