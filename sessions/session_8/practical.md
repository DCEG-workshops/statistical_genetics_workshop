---
layout: page
permalink: sessions/session_8/practical
menubar_toc: true
---

## Tutorial notebook

Work through [Genetic Mosaicism Practical — Biowulf 2026 (`08_mCA_Biowulf_2026_final.Rmd`)](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/08_mCA_Biowulf_2026_final.Rmd). [Download the R Markdown file](https://raw.githubusercontent.com/DCEG-workshops/statgen_workshop_tutorial/main/src/08_mCA_Biowulf_2026_final.Rmd).

This practical uses SNP-array intensity data to detect and visualize mosaic chromosomal alterations (mCAs). You will convert GenomeStudio data to BCF, check sample contamination with BAFRegress, phase genotypes with EAGLE2, identify mCAs with MOChA, and create regional and Circos plots.

## Setup

1. Launch **RStudio Server on a Biowulf compute node** through [NIH HPC OnDemand](https://hpcondemand.nih.gov), following the [Session 1 RStudio launch instructions]({{ '/sessions/session_1/practical' | relative_url }}#launch-rstudio-on-hpc-ondemand).
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

3. In RStudio, choose **File > Open File** and open `src/08_mCA_Biowulf_2026_final.Rmd` from your checkout.
4. Run the **Define paths** and **Verify the setup** R chunks in Section 1 first. These create your output folders, make paths available to later Bash chunks, and check the required shared files. If a resource is missing or your output directory is not writable, contact the instructor before continuing.
5. Run the container checks in Section 2. The notebook loads `singularity` and uses the shared bcftools 1.20 and EAGLE2 container images.
6. The plotting sections require `optparse`, `reshape2`, `data.table`, `ggplot2`, and `circlize`; the R Markdown notebook also uses `knitr` and `rmarkdown`. Check for missing packages in the RStudio **Console** before class:

   ```r
   needed <- c("optparse", "reshape2", "data.table", "ggplot2", "circlize",
               "knitr", "rmarkdown")
   missing <- needed[!vapply(needed, requireNamespace, logical(1), quietly = TRUE)]
   if (length(missing)) install.packages(missing)
   ```

### Shared inputs and personal outputs

The notebook reads reference files, test data, container images, and plotting scripts from:

```text
/data/DCEG_shared/statgen_workshop_2026/statgen_workshop_tutorial/DCEG_mosaicism_workshop
```

The GenomeStudio test input is `test_set/full_data_table_test_set.txt` within that directory. Keep the shared resources unchanged. The notebook writes intermediate files, logs, and results to your personal working area, using your Biowulf username automatically:

```text
/data/<Biowulf-username>/statgen_workshop_2026/session8/mosaicism
```

## Run the practical

Work through the notebook **interactively, in section order**. Code chunks marked `{r}` run in R; use the green **Run** button for each `{bash}` chunk to execute its commands on the compute node allocated to RStudio. Run the Section 1 setup again if you restart the R session.

1. **Convert the intensity data (Section 3):** Use `bcftools +gtc2vcf`, sort and normalize the data against GRCh37, and check for `to_bcf/samples.bcf` and its index.
2. **Check contamination (Section 4):** Run BAFRegress and inspect `baf_regress/baf_regress.txt`.
3. **Phase the genotypes (Section 5):** Check the chromosome reference files, then submit EAGLE2. This step submits **23 Slurm jobs**, one for each chromosome 1–22 and X. Run the monitoring chunk and confirm that all jobs completed successfully and all phased BCF files and indexes exist before proceeding. Job IDs and logs are saved under `logs/`; inspect the chromosome-specific `.err` and `.out` files if a job fails.
4. **Combine the phased data (Section 6):** Concatenate the chromosome files into `phasing/samples.pgt.bcf` and index it.
5. **Detect mCAs (Section 7):** Run MOChA and inspect `mocha/samples.calls.tsv`, sample statistics, and the annotated BCF. Distinguish gains, deletions, and copy-neutral loss of heterozygosity (CN-LOH).
6. **Visualize individual events (Section 8):** Generate the regional plots and examine log R ratio (LRR), B-allele frequency (BAF), and estimated abnormal cell fractions.
7. **Summarize events with Circos (Section 9):** Use the supplied synthetic examples to create plots for three and four event types. These examples use **hg38**, while the preceding MOChA analysis uses **GRCh37**; keep the genome setting matched to each input.

**Run the phasing submission chunk once for each intended analysis.** Re-running it, or knitting the entire notebook, submits the jobs again and reruns the workflow. Use the monitoring and output-check chunks to follow the jobs already submitted.

## Expected outputs

Within your personal working area, review:

- `mocha/samples.calls.tsv` and `mocha/samples.stats.tsv` for detected events and sample statistics.
- `plots/S5.png`, `S6.png`, `S8.png`, `S9.png`, and `S10.png` for regional examples.
- `circos/mosaic_events_autosomal.circos.png` and `.pdf`, plus the `circos2` versions and TSV summaries, for the synthetic Circos examples.

See the [Session 8 reading material]({{ '/sessions/session_8' | relative_url }}#reading-material) for background and documentation for the methods.
