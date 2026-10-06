---
layout: page
permalink: sessions/session_4/practical
menubar_toc: true
---

## Tutorial notebook

Work through the [Fine Mapping and Colocalization Lab (`04_finemapping_colocalization.Rmd`)](https://github.com/DCEG-workshops/statgen_workshop_tutorial/blob/main/src/04_finemapping_colocalization.Rmd). [Download the R Markdown file](https://raw.githubusercontent.com/DCEG-workshops/statgen_workshop_tutorial/main/src/04_finemapping_colocalization.Rmd).

The lab uses GWAS summary statistics, linkage disequilibrium (LD), and gene-expression association data to explore candidate causal variants and shared association signals.

## Setup

1. Launch RStudio through [NIH HPC OnDemand](https://hpcondemand.nih.gov). See the [Session 1 RStudio setup instructions]({{ '/sessions/session_1/practical' | relative_url }}#launch-rstudio-on-hpc-ondemand).
2. Open the **Terminal** tab in RStudio and run these shell commands to clone the tutorial repository into your own workshop folder:

   ```bash
   mkdir -p /data/$USER/Stats_Gen/workshop4
   cd /data/$USER/Stats_Gen/workshop4
   git clone https://github.com/DCEG-workshops/statgen_workshop_tutorial.git
   ```

   If you already cloned the repository, use your existing copy.
3. In RStudio, choose **File > Open File** and open `/data/<your-username>/Stats_Gen/workshop4/statgen_workshop_tutorial/src/04_finemapping_colocalization.Rmd`, replacing `<your-username>` with your Biowulf username. If you are using an existing clone elsewhere, open `src/04_finemapping_colocalization.Rmd` from that folder.
4. Choose **Session > Set Working Directory > To Source File Location**. Changing directories in the Terminal does not change R's working directory.
5. Install any missing packages listed in the notebook: `susieR`, `coloc`, `knitr`, and `rmarkdown`.
6. Run the setup chunks, then work through the analysis chunks in order. The notebook reads shared inputs from the directory below and saves results in `/vf/users/<your-username>/Stats_Gen/workshop4`.

```text
/data/DCEG_shared/statgen_workshop_2026/data/workshop4
```

## Lab activities

1. **Fine-mapping with SuSiE:** Examine GWAS summary statistics and LD at FGFR2, run SuSiE, and interpret posterior inclusion probabilities and 95% credible sets.
2. **Colocalization with coloc:** Compare GWAS and gene-expression signals in two tissues and interpret evidence for distinct versus shared causal variants. Discuss why colocalization does not establish mediation through gene expression.
3. **Optional extensions:** Explore multiple signals at TERT and assess sensitivity to colocalization priors.

See the [Session 4 reading materials]({{ '/sessions/session_4' | relative_url }}#reading-materials) for background on fine-mapping and colocalization.
