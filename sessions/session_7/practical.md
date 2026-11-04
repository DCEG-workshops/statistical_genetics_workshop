---
layout: page
permalink: sessions/session_7/practical
menubar_toc: true
---

## Tutorial R script

Work through [Session 7: Rare Variants (`07_rare_variants.R`)](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/07_rare_variants.R).

This practical uses simulated rare-variant data to compare gene-level burden tests with the sequence kernel association test (SKAT). Explore carrier status, weighted burden scores, and variant effects to understand how effects in opposite directions can affect the two tests.

## Setup

1. Launch RStudio on a Biowulf compute node using the [Session 1 RStudio launch instructions]({{ '/sessions/session_1/practical' | relative_url }}#launch-rstudio-on-hpc-ondemand).
2. In the RStudio **Terminal**, update your existing tutorial checkout:

   ```bash
   cd /data/$USER/Stats_Gen/statgen_workshop_tutorial
   git pull
   ```

   Replace the path with your existing repository location if needed. If this is your first time cloning the repository, run:

   ```bash
   mkdir -p /data/$USER/Stats_Gen
   cd /data/$USER/Stats_Gen
   git clone https://github.com/DCEG-workshops/statgen_workshop_tutorial.git
   ```

3. Open `src/07_rare_variants.R` in RStudio. The script uses the R packages `SKAT`, `ggplot2`, and `patchwork`. If needed, install them in the RStudio **Console** before class:

   ```r
   install.packages(c("SKAT", "ggplot2", "patchwork"))
   ```

4. Confirm that your account can read the shared input file:

   ```text
   /data/DCEG_shared/statgen_workshop_2026/data/workshop7/rare_variants/rare_variant_data.rds
   ```

   The script sets R's working directory to this shared data folder before loading the file. Contact the instructor if the file is unavailable to your account.

## Run the practical

Run all setup code at the top of the script, including package loading, then work through the script's numbered sections in order:

1. **Inspect the data:** Review phenotypes, genotypes, and gene annotations; align sample and variant IDs; inspect allele frequencies, allele counts, and missingness.
2. **Visualize the data:** Explore the outcome, variant frequencies, gene sizes, and covariates.
3. **Compare burden and SKAT tests:** Use the same covariates, variants, and weights for both tests, and apply the multiple-testing correction across genes and methods.
4. **Explore carriers and burden scores:** Compare carrier and non-carrier outcomes and distinguish binary carrier status from a weighted dosage burden.
5. **Interpret effect directions:** Examine the simulated LDLR and APOE examples, variant effect estimates, and signed scores to understand why opposing effects can cancel in a burden test.

The simulated examples illustrate statistical behavior; they do not establish biological findings about these genes. See the [Session 7 reading material]({{ '/sessions/session_7' | relative_url }}#reading-material) for background.
