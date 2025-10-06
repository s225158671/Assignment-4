# Assignment-4


Assessment 4 — SLE777 (R Project)
Overview

This project analyses tree growth across two sites from 2005–2020 and includes a short sequence analysis task. The main deliverable is a knitted report.

Files

MMM.Rmd — primary analysis notebook (R Markdown).

MMM.html — knitted report produced from MMM.Rmd.

Inputs

Tree growth dataset (CSV): TreeGrowth.csv
Expected columns:
Site, Circumf_2005_cm, Circumf_2010_cm, Circumf_2015_cm, Circumf_2020_cm

Sequence dataset (FASTA or list of CDS): ecoli_cds.fasta
Used for nucleotide frequency counts with the seqinr package.

What each script/notebook does

MMM.Rmd → MMM.html

Loads growth and sequence data.

Q7: Computes per-site mean and SD of circumference at the start (2005) and end (2020).

Q8: Draws a boxplot comparing 2005 vs 2020 for each site.

Computes nucleotide frequencies across coding sequences and plots a bar chart.

Prints tidy tables and labelled figures to the knitted report.

Outputs

All outputs are embedded directly into the knitted MMM.html report:

Q7 Summary table — per-site Mean/SD for 2005 and 2020.

Q8 Boxplot — “Tree Growth (Start vs End of Study)” comparing 2005 vs 2020 for both sites.

Nucleotide frequency barplot — counts of A, C, G, T across CDS.

How to run

Open MMM.Rmd in RStudio.

Install packages (first run only):
install.packages("seqinr")

Place input files (CSV/FASTA) in the project root or update the paths in the code.

Click Knit → Knit to HTML to produce MMM.html.

Reproducibility notes

R version, package versions, and session info are included in the knitted HTML footer.

Directory layout
.
├─ MMM.Rmd
├─ MMM.html
├─ data/
│  ├─ TreeGrowth.csv
│  └─ ecoli_cds.fasta
└─ README.md

