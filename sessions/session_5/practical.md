---
layout: page
permalink: sessions/session_5/practical
menubar_toc: true
---

## Tutorial notebook

Work through [Heritability Analysis in GWAS (`05_Heritability.Rmd`)](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/05_Heritability/05_Heritability.Rmd). The practical covers SNP heritability with GCTA/GREML and LD Score regression, genetic correlation, and enrichment with stratified LD Score regression.

## Setup

1. Launch RStudio through [NIH HPC OnDemand](https://hpcondemand.nih.gov). See the [Session 1 RStudio setup instructions]({{ '/sessions/session_1/practical' | relative_url }}#launch-rstudio-on-hpc-ondemand).
2. Open the **Terminal** tab in RStudio. The tutorial repository contains materials for all sessions, so you only need one copy.

   **If you cloned the repository before**, go to that existing folder and run `git pull` to get the latest materials:

   ```bash
   cd /data/$USER/Stats_Gen/statgen_workshop_tutorial
   git pull
   ```

   Replace the `cd` path with your existing repository location if you cloned it elsewhere. Run `git pull` from that folder before future sessions too.

   **If this is your first time cloning the repository**, run:

   ```bash
   cd /data/$USER/Stats_Gen
   git clone https://github.com/DCEG-workshops/statgen_workshop_tutorial.git
   ```

3. In RStudio, choose **File > Open File**, browse to your `statgen_workshop_tutorial` folder, and open `src/05_Heritability/05_Heritability.Rmd`. Keep the accompanying `R/` and `scripts/` folders beside the notebook; they are included in the repository.
4. Choose **Session > Set Working Directory > To Source File Location**. Changing directories in the Terminal does not change R's working directory.
5. Install any missing packages listed in the notebook: `data.table`, `knitr`, and `rmarkdown`.
6. Run the setup chunk and subsequent chunks in order, or use **Knit** to run the notebook and generate an HTML report. Follow the notebook's preparation and data-path instructions; the supplied scripts load the Biowulf GCTA and LDSC modules.
