---
layout: page
permalink: sessions/session_1/practical
menubar_toc: true
---

## Tutorial source

The practical tutorial files are available in the [`src` folder of the Statistical Genetics Workshop tutorial repository](https://github.com/DCEG-workshops/statgen_workshop_tutorial/tree/main/src).

The tutorial data is also available on [Google Drive](https://drive.google.com/drive/folders/1kVJH4tM8R8O0hITnvifCV-hoai-Mgn-b?usp=sharing).

## Objectives

- Introduce the RStudio Server / Biowulf HPC environment for genetic data analysis.
- Introduce the importance of Quality Control (QC) in the GWAS analysis pipeline.
- Provide hands-on practice performing standard QC steps on real GWAS data using PLINK.

## Prerequisites

- A basic understanding of genetics, genome-wide association studies (GWAS), and the role of QC in GWAS.
- Familiarity with the command line, since we will use PLINK (a command-line tool) for QC.
- A Biowulf HPC account.
- RStudio launched from NIH OnDemand.
- **PLINK 1.9 must be loaded before starting your OnDemand RStudio session.**

## Launch RStudio on HPC OnDemand

If you plan to run the hands-on tutorial on Biowulf:

1. Confirm that your Biowulf account is active before the session.
2. Bring your PIV card and a compatible card reader.
3. Open [HPC OnDemand](https://hpcondemand.nih.gov).
4. Sign in with NIH multi-factor authentication.
5. Open **RStudio Server** from the **Interactive Apps** area.
6. Enter the workshop-provided resource and working-directory settings, then launch the job.
7. When the job starts, click **Connect to RStudio Server**.

For account or login problems before the workshop, contact [NIH HPC support](mailto:staff@hpc.nih.gov).

## Workshop Overview

We will use PLINK to carry out several essential QC procedures on real genotype data from the PennCATH study of coronary artery disease. This dataset includes 1,401 individuals genotyped at 861,473 markers.

In this session we will:

1. Check sample and SNP missingness
2. Identify markers that deviate from Hardy-Weinberg Equilibrium
3. Check heterozygosity across samples
4. Check estimated relatedness (IBD) between samples
5. Examine population structure using PCA, including a joint analysis with 1000 Genomes (1KG) reference samples to interpret study-sample genetic similarity relative to 1KG reference ancestry labels
6. Use GrafAnc to obtain reference-based genetic ancestry assignments and compare them with the PCA patterns

**Note:** These steps illustrate core GWAS QC concepts but are not an exhaustive production QC protocol. Depending on the study and genotyping platform, additional checks may include sex-chromosome concordance, duplicate/sample identity checks, batch effects, allele/build harmonization, differential missingness, external allele-frequency comparisons, and post-imputation QC.

## External resources

- [PLINK 1.9 Documentation](https://www.cog-genomics.org/plink/)
- [GrafAnc Software Documentation](https://github.com/jimmy-penn/grafanc/blob/master/GrafAncDocumentation.md)
