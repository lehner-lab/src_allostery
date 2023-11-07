# src_allostery
Source code for analyses and to reproduce all figures in the following publication: The allosteric landscape of Src (Beltran et al., 2023)



Welcome to the GitHub repository for the following publication: The allosteric landscape of the Src kinase (Beltran A & Lehner B, 2023)

Here you'll find source code for computational analyses and to reproduce the figures in the paper.

# Table Of Contents

* **1. [Required Software](#required-software)**
* **2. [Required Data](#required-data)**
* **3. [Installation Instructions](#installation-instructions)**
* **4. [Usage](#usage)**

# Required Software

To run the Stop_codon_readthrough pipeline you will need the following software and associated packages:

* **[_R_](https://www.r-project.org/)** (dplyr, stringr, stringi, GGally, ggpubr, ggplot2, viridis, tidyverse, seqinr, matrixStats, data.table, rtracklayer, openxlsx, reshape2, caret, hexbin, png, grid, gridExtra, MuMIn, tidyr, rstatix, ggridges, hrbrthemes, glmnet, spgs)

# Required Data

Read counts (DiMSum output), readthrough efficiencies, and required miscellaneous files should be downloaded from **[here](link)** to your project directory (named 'base_dir') i.e. where output files should be written.

# Installation Instructions

Make sure you have git and conda installed and then run (expected install time <10min):

```
# Install dependencies (preferably in a fresh conda environment)
conda install -c conda-forge r-dplyr, r-stringr, r-stringi, r-ggally, r-ggpubr, r-ggplot2, r-viridis, r-tidyverse, r-seqinr, r-matrixstats, r-data.table, r-rtracklayer, r-openxlsx, r-reshape2, r-caret, r-hexbin, r-png, r-grid, r-gridextra, r-mumin, r-tidyr, r-rstatix, r-ggridges, r-hrbrthemes, r-glmnet, r-spgs, r-biocmanager, r-biomart
```

# Usage

The R Markdown files contain the code to reproduce the figures and results from the computational analyses described in the following publication: The allosteric landscape of the Src kinase (Beltran A & Lehner B, 2023) (Beltran A & Lehner B, 2023). See [Required Data](#required-data) for instructions on how to obtain all required data and miscellaneous files before running the pipeline. If using/downloading the files from [Required Data](#required-data) and only plotting the figures, the expected run time is <10min. 

R Markdown files are meant to be run in the following order:

* **1. name.Rmd**
* **2. name.Rmd**
* **3. name.Rmd**
* **4. name.Rmd**
* **5. name.Rmd**
* **6. name.Rmd**
* **7. name.Rmd**

# Additional scripts and software

The following software package is required for pre-processing of raw FASTQ files:

* **[DiMSum](https://github.com/lehner-lab/DiMSum) v1.2.9** (pipeline for pre-processing deep mutational scanning data i.e. FASTQ to fitness). Download the FastQ files from Sequence Read Archive (SRA) with accession number ####:link to your base directory (base_dir). Shell scripts to run both Dimsum rounds can be found in [Required Data](#required-data).
  
Configuration files and additional scripts for running DiMSum are available in the "DiMSum" folder **[here](link)**.
