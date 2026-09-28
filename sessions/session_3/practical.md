---
layout: page
permalink: sessions/session_3/practical
menubar_toc: true
---

## Tutorial notebook

Work through the [Gene–Environment Interaction Lab (`03_gxe_lab.Rmd`)](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/03_gxe_lab.Rmd), prepared by Jayati Sharma for the DCEG Statistical Genetics Workshop 2026. [Download the R Markdown file](https://raw.githubusercontent.com/DCEG-workshops/statgen_workshop_tutorial/main/src/03_gxe_lab.Rmd).

The lab uses two simulated datasets to explore how smoking and a single SNP jointly relate to disease status. Run the supplied code blocks in order and answer the interpretation questions in the notebook. **You do not need to write any code.**

## Objectives

- Compare gene–environment interaction on multiplicative and additive scales.
- Interpret interaction estimates from logistic and linear-probability models.
- Examine smoking-by-carrier tables and relative excess risk due to interaction (RERI).
- Explain why an answer to “Is there an interaction?” must specify a scale.

## Setup

1. Launch RStudio through [NIH HPC OnDemand](https://hpcondemand.nih.gov). See the [Session 1 RStudio setup instructions]({{ '/sessions/session_1/practical' | relative_url }}#launch-rstudio-on-hpc-ondemand).
2. Save a personal copy of `03_gxe_lab.Rmd` and open it in RStudio.
3. Run the setup and data-reading chunks first. The notebook creates a working directory at `/vf/users/<your-username>/Stats_Gen/workshop3` and reads the two shared CSV files listed below.
4. Continue through the chunks and type your answers beneath each set of questions. You can also knit the notebook to HTML using `rmarkdown` and `knitr`.

The notebook uses these Biowulf data files:

```text
/data/DCEG_shared/statgen_workshop_2026/data/workshop3/gxe_dataset1.csv
/data/DCEG_shared/statgen_workshop_2026/data/workshop3/gxe_dataset2.csv
```

## Lab activities

1. **Dataset 1:** Inspect the variable distributions, fit the interaction models, and examine the smoking-by-carrier table and RERI.
2. **Dataset 2:** Repeat the analyses, calculate RERI confidence intervals, and compare the conclusions across scales.
3. **Synthesis:** Compare the two datasets and discuss which scale addresses the scientific or public-health question of interest.
4. **Optional visualization:** Plot both datasets on the risk and log-odds scales and compare the patterns.
