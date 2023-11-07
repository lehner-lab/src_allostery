Welcome to the GitHub repository for the following publication: The allosteric landscape of the Src kinase (Beltran A & Lehner B, 2023)

Here you'll find source code for computational analyses and to reproduce the figures in the paper.

# Table Of Contents

* **1. [Required Software](#required-software)**
* **2. [Required Data](#required-data)**
* **3. [Installation Instructions](#installation-instructions)**
* **4. [Usage](#usage)**

# Required Software

To run the Stop_codon_readthrough pipeline you will need the following software and associated packages:

* **[_R_](https://www.r-project.org/)** (GGally, bio3d, data.table, ggplot2, ggpubr, gplots, msir, scales, viridis)

# Required Data

The read counts (DiMSum output), fitness scores, MoCHI weights, and required miscellaneous files should be downloaded from **[here](link)** and copied to an analysis_files folder in your project directory (named 'base_dir'). An output_files directory in which results files will be written should be created in 'base_dir'.

# Installation Instructions

Make sure you have git and conda installed and then run (expected install time <10min):

```
# Install dependencies (preferably in a fresh conda environment)
conda install -c conda-forge r-ggally, r-bio3d, r-data.table, r-ggplot2, r-ggpubr, r-gplots, r-msir, r-scales, r-viridis
```

# Usage

The R Markdown files contain the code to reproduce the figures and results from the computational analyses described in the following publication: The allosteric landscape of the Src kinase (Beltran A & Lehner B, 2023). See [Required Data](#required-data) for instructions on how to obtain all required data and miscellaneous files before running the pipeline.

R Markdown files are meant to be run in the following order:

* **1. 00_fitness_reproducibility_and_mochi_evaluation.Rmd**
* **2. 00_mochi_ddGs_onto_structure.Rmd**
* **3. 01_Figure1.Rmd**
* **4. 02_Figure2.Rmd**
* **5. 03_Figure3.Rmd**
* **6. 04_Figure4.Rmd**
* **7. 05_Figure5.Rmd**
* **8. 06_Figure6.Rmd** 

# Additional scripts and software

The following software packages are required for pre-processing of raw FASTQ files:

* **[DiMSum](https://github.com/lehner-lab/DiMSum) v1.2.9** (pipeline for pre-processing deep mutational scanning data i.e. FASTQ to fitness). Download the FastQ files from Sequence Read Archive (SRA) with accession number ####:link to your base directory (base_dir). Shell scripts to run Dimsum can be found in [Required Data](#required-data). Configuration files and additional scripts for running DiMSum are available in the "DiMSum" folder.

The following software package is required to fit thermodynamic models to the fitness data (DiMSum output):

* **[MoCHI](https://github.com/lehner-lab/MoCHI) v?.?.?** (pipeline to fit thermodynamic models to fitness data i.e. fitness to energies). In order to fit all 5 blocks of Src together, DiMSum fitness tables need to be modified to extend the sequence of each block to the full length Src sequence, and the sign of the kinase activity fitness assay needs to be changed due to the inverse relationship between fitness and activity in the activity assay. The original DiMSum output tables, the modified tables ready for MoCHI fitting, and shell scripts to execute MoCHI can be found in [Required Data](#required-data). 


