# Assignment-4

# Analysis of Coding Sequences, Codon Usage, and Growth Patterns

This repository contains an RMarkdown workflow that explores:

1.bacterial coding sequence (CDS) characteristics and codon usage (Salmonella Weltevreden vs. E. coli MG1655), and
2.a small time-series dataset of tree circumference growth across two sites (northeast vs. southwest).
The HTML report (“MM”) was rendered on 2025-10-05 and includes code, figures, and narrative answers for each task. 

#Features

Data Ingestion: Programmatic download of input files (e.g., `gene_expression.tsv`) via `download.file()` with local verification. 
CDS Length Summary: Computation of mean/median CDS lengths per organism; discussion of right-skewed distributions and outliers, supported by boxplots. 
Codon Usage Profiling: RSCU-based ranking highlighting GC-ending codon preference (e.g., CTG, CGC, CCG, GGC) and ties to tRNA availability. 
Amino-Acid k-mer Motifs: Comparison of common/rare peptides (k=3–5) between species; notes on Leu/Ala-rich motifs and rarer Trp/Cys/His/Tyr combinations. 
Tree Growth Time Series: Site-level summaries (means/SDs for 2005 vs. 2020) and visual comparisons via boxplots to illustrate growth and increasing variability. 

# Repository Contents

01_cds_lengths_and_codon_usage.Rmd`

Loads bacterial CDS data, computes CDS length summaries, creates boxplots, and ranks codon usage by RSCU; includes k-mer motif exploration.  
Figures:

Figure 1: CDS length distributions (boxplots) per organism. 
Figure 2: Ranked RSCU bar/point plots (top/bottom codons). 
Supplementary: k-mer frequency panels (k=3–5). 
`02_tree_growth_timecourse.Rmd`

Imports the tree circumference dataset (2005–2020), computes site-wise stats, and visualises changes over time with boxplots. 
Figures:
Figure 3: Boxplots of circumference by site (2005 vs 2020). 
Tables:
Table 1: Site means/SDs at start/end of study. 
`functions.R`

Utility helpers (e.g., tidy wrappers, plotting helpers, and summary functions) used across Rmd notebooks. *(Organization placeholder for your custom helpers.)*

>Rendered Report: `MMM (1).html` (title “MM”, dated 2025-10-05) aggregates all sections, code, and outputs. 

# Prerequisites

This project requires R (≥ 4.0) and the following packages:

Core & Tidy

`tidyverse` (incl. `dplyr`, `ggplot2`, `readr`, `tibble`, `tidyr`)
`knitr`, `rmarkdown`

Visualization

`ggpubr`, `ggrepel`, `cowplot`, `RColorBrewer`, `viridis`

Sequence / Genomics (if extending RSCU/k-mer work)

`Biostrings`, `seqinr`, `DECIPHER` *(or equivalents you used for codon/k-mer parsing)

# How to Reproduce

1. Clone/download the repo and open the R project.
2. Run the notebooks in order (they will download inputs as needed):

   * `01_cds_lengths_and_codon_usage.Rmd`
   * `02_tree_growth_timecourse.Rmd`
     *(The HTML indicates programmatic downloads via `download.file()`.)* 
3. Outputs (figures/tables) will be written to `figs/` and `tables/` (or embedded in the knitted HTML, as in “MM”).

# Data Sources

Bacterial CDS / Gene Expression: Downloaded during execution (see code chunk with `download.file()` and local verification). 
Tree Growth Dataset: Wide-format circumference data with columns for 2005, 2010, 2015, 2020 and a site indicator. 

# Outputs

CDS/Usage:

Summary table of CDS lengths per organism; boxplots showing right-skew. 
RSCU-ranked codon lists and plots; brief interpretation of GC bias and translation selection. 
Tree Growth:

Site-wise mean/SD table (2005 vs. 2020). 
Boxplots comparing site distributions across time. 

