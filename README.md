# Assignment-4


````markdown
# Assessment 4 — SLE777 (R Project)

## Overview
This project analyses tree growth across two sites from 2005–2020 and includes a short sequence analysis task. The main deliverable is a knitted report.

## Files
- MMM.Rmd — primary analysis notebook (R Markdown).
- MMM.html — knitted report produced from `MMM.Rmd`.

## Inputs
> Update filenames/paths below to match what you actually used.
- Tree growth dataset (CSV): e.g., `TreeGrowth.csv`  
  Expected columns:  
  `Site`, `Circumf_2005_cm`, `Circumf_2010_cm`, `Circumf_2015_cm`, `Circumf_2020_cm`
- Sequence dataset (FASTA or list of CDS): e.g., `ecoli_cds.fasta`  
  Used for nucleotide frequency counts with the `seqinr` package.

## What each script/notebook does
- MMM.Rmd → MMM.html
  - Loads growth and sequence data.
  - Q7: Computes per-site mean and SD of circumference at the start (2005) and end (2020).
  - Q8: Draws a boxplot comparing 2005 vs 2020 for each site.
  - Computes nucleotide frequencies across coding sequences and plots a bar chart.
  - Prints tidy tables and labelled figures to the knitted report.

## Outputs (files / figures / tables)
- Q7 Summary table — per-site Mean/SD for 2005 and 2020 (displayed in the report).
- Q8 Boxplot — “Tree Growth (Start vs End of Study)” comparing 2005 vs 2020 for both sites (figure in the report).
- Nucleotide frequency barplot — counts of A/C/G/T across CDS (figure in the report).
- Knitted report: `MMM.html`.

## How to run
1. Open `MMM.Rmd` in RStudio.
2. Install packages (first run only):
   ```r
   install.packages(c("seqinr"))
   # If you knit to PDF later with Unicode characters, consider tinytex:
   # tinytex::install_tinytex()
````

3. Place input files (CSV/FASTA) in the project root or update the paths in the code.
4. Click Knit → Knit to HTML to produce `MMM.html`.

## Reproducibility notes

 R version, package versions, and session info are included in the knitted HTML footer.

## Directory layout

```
.
├─ MMM.Rmd
├─ MMM.html
├─ data/
│  ├─ TreeGrowth.csv
│  └─ ecoli_cds.fasta
└─ README.md
```

#Marking hint (code clarity)

All code chunks in `MMM.Rmd` include clear, top-of-chunk comments describing goal → steps → output so another reader can follow the logic quickly.

```


```
