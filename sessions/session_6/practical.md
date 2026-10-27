---
layout: page
permalink: sessions/session_6/practical
menubar_toc: true
---

## Tutorial notebook

Work through [Session 6: Polygenic Risk Scores (`06_PRS_LDpred2.Rmd`)](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/06_PRS/06_PRS_LDpred2.Rmd). The [Session 6 tutorial folder](https://github.com/DCEG-workshops/statgen_workshop_tutorial/tree/main/src/06_PRS) contains the notebook, a completed HTML report, and prepared LDpred2 results for the backup workflow.

This **90-minute practical** compares clumping and thresholding (C+T) with LDpred2 using the same chromosome 22 inputs. Complete the RStudio launch, package installation, LD download, and data-access checks **before class**.

## Setup before class

1. Launch RStudio through [NIH HPC OnDemand](https://hpcondemand.nih.gov) on a Biowulf compute node. Select **R 4.6**, **2 CPUs**, **8 GB RAM**, **at least 2 hours**, and **5 GB local scratch**. See the [Session 1 RStudio launch instructions]({{ '/sessions/session_1/practical' | relative_url }}#launch-rstudio-on-hpc-ondemand). This notebook loads the required PLINK modules itself.
2. Open the **Terminal** tab in RStudio. The tutorial repository contains materials for all sessions, so you only need one copy.

   **If you cloned the repository before**, update your existing copy and enter the Session 6 folder:

   ```bash
   cd /data/$USER/Stats_Gen/statgen_workshop_tutorial
   git pull
   cd src/06_PRS
   ```

   Replace the first `cd` path with your existing repository location if you cloned it elsewhere.

   **If this is your first time cloning the repository**, run:

   ```bash
   mkdir -p /data/$USER/Stats_Gen
   cd /data/$USER/Stats_Gen
   git clone https://github.com/DCEG-workshops/statgen_workshop_tutorial.git
   cd statgen_workshop_tutorial/src/06_PRS
   ```

3. Download the supplied LD matrix from the [Session 6 data release](https://github.com/DCEG-workshops/statgen_workshop_tutorial/releases/tag/prs-tutorial-2026-10-27). Run these commands in the **Terminal**, from `src/06_PRS/`:

   ```bash
   curl --fail --location --retry 3 \
     --output 06_PRS_1000G_LD.rds \
     https://github.com/DCEG-workshops/statgen_workshop_tutorial/releases/download/prs-tutorial-2026-10-27/06_PRS_1000G_LD.rds
   sha256sum -c SHA256SUMS
   ```

   The **276 MiB LD file is not included by `git clone`**. Every listed file should report `OK`; check before editing the notebook, because your edits will change its checksum. Keep the notebook and both RDS files together in your own writable directory. On macOS, the equivalent checksum command is `shasum -a 256 -c SHA256SUMS`.
4. In RStudio, choose **File > Open File** and open `src/06_PRS/06_PRS_LDpred2.Rmd` in your clone. Choose **Session > Set Working Directory > To Source File Location**. Changing directories in the Terminal does not change R's working directory.
5. Follow **Install and check R packages before class** in the notebook, running the installation code in the RStudio **Console**. Live fitting uses `data.table`, `knitr`, `rmarkdown`, `Matrix`, `bigsnpr`, and `bigsparser`. Install into the notebook's project library using the same R version as your RStudio session.
6. Confirm that your account can read the shared input directory below. The notebook's `paths-and-resources` chunk checks the required files and reports missing or unreadable inputs. Contact the instructor if access is missing.

```text
/data/DCEG_shared/statgen_workshop_2026/data/workshop6/data/
```

The shared inputs are `EUR_sum_data` (GWAS summary statistics), `1kg_eur_22/chr_22.{bed,bim,fam}` (European LD reference), `prs_genotype/chr22_test.{bed,bim,fam}` (target genotypes), and `y_out` (quantitative outcomes). These raw inputs are not included in the GitHub tutorial folder.

## Run the practical

Keep the default notebook settings for live fitting:

```yaml
execute: true
run_ldpred2: true
ldpred_mode: "fit"
rebuild_ld: false
```

Run the **setup** chunk first, then subsequent chunks in order, **or** use **Knit** to run the notebook and generate an HTML report. Doing both repeats the analysis. Save any YAML changes before rerunning setup or knitting. Leave `rebuild_ld: false` during class: students load the supplied LD matrix, while LD construction is an optional instructor appendix.

### Lab activities

1. **Inspect and align the inputs:** Check GWAS effects, effect alleles, sample IDs, and the common eligible variant pool used by both methods. Review the 10,000-sample tuning set and the separate 10,000-sample validation set.
2. **Construct C+T scores:** Use PLINK 1.9 for LD clumping and PLINK 2 for scoring at nine GWAS p-value thresholds. Select the threshold using tuning-set R-squared.
3. **Fit and tune LDpred2:** Use the supplied LD matrix to fit four combinations of `p` (0.01 or 0.1) and `h2` (0.01 or 0.1). Inspect model status, exclude failed fits, and select a model using tuning samples only.
4. **Compare the selected scores:** Freeze the chosen settings and evaluate each score once in the validation set. Compare R-squared and how similarly the scores rank individuals.
5. **Discuss interpretation:** Explain why validation outcomes must not guide parameter selection, why the teaching grid does not estimate whole-genome heritability, and how ancestry, LD-reference size, covariates, and genome-wide coverage could affect results.

Suggested timing: setup checks (10 minutes), C+T (30), tuning discussion (10), LDpred2 (20), comparison (15), and buffer (5).

## Prepared-results backup

If the LD download or fitting packages are unavailable, or fitting cannot finish during class, use `06_PRS_LDpred2_prepared.rds`, which is included in the repository. It supplies LDpred2 weights and target scores; C+T still runs using the shared inputs. Prepared mode needs `data.table`, `knitr`, `rmarkdown`, and `Matrix`, but does not require the LD matrix, `bigsnpr`, or `bigsparser`.

For a fresh run, change **only** `ldpred_mode` to `"prepared"`, save the notebook, and run all chunks or Knit. Keep the input files, model grid, and other settings unchanged so that the backup matches them. If switching during an interactive run, stop the active chunk, wait for the Console prompt, then follow the notebook's **Choose live fitting or the prepared backup** instructions for the chunks to rerun.

To review the completed example without running it, [download the prepared HTML report](https://raw.githubusercontent.com/DCEG-workshops/statgen_workshop_tutorial/main/src/06_PRS/06_PRS_LDpred2.prepared.html) and open the saved file in a browser.

## Results and interpretation

Each run writes to a new subdirectory of `06_PRS_results/` beside your notebook. Review `method_comparison.tsv`, `selected_scores.tsv`, the tuning-performance tables, plots, and PLINK logs. The notebook also records the sample split, parameters, and software environment.

For this quantitative-trait example, validation R-squared is the squared correlation between the score and outcome in held-out samples. It measures association, not calibration of a frozen prediction equation or clinical usefulness. The chromosome 22 subset, simulated target data, and small European LD reference limit generalization; the exercise does not establish that either method is universally better.

See the [Session 6 reading material]({{ '/sessions/session_6' | relative_url }}#reading-material) for background and the official LDpred2 tutorial.
