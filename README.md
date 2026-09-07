# CRISPRi screen analysis workflow

This repository contains the initial analysis used for the associated bioRxiv paper. The code is provided as a reference and is not intended to be run. The experimental data are not included.

## Associated study

**Reference paper:** 

Genome-wide high-density CRISPR interference screens reveal condition-specific metabolic vulnerabilities in Pseudomonas aeruginosa PAO1

Andreas Kaczmarczyk, Alexander Klotz, Pablo Manfredi, Urs Jenal

bioRxiv 2025.08.12.669819; doi: https://doi.org/10.1101/2025.08.12.669819


## Repository contents

The numbered notebooks reflect the main stages of the analysis:

1. **`01_library_QC.ipynb`** — evaluates sgRNA library coverage, compares count distributions across samples, calculates summary statistics, examines gene representation, and identifies genes absent from the library.

2. **`02_screen_analysis.ipynb`** — pairs gene-level and sgRNA-level result files, adds genome annotations, applies significance criteria, and generates processed tables, volcano plots, gene-level comparisons, and enriched/depleted gene sets.

3. **`03_essential_genes_comparison.ipynb`** — compares significant-gene sets across time points and analysis strategies, and compares depleted genes with published essential-gene sets from Lee et al. (2015).

4. **`04_sgrna_plots.ipynb`** — visualizes individual-sgRNA fold changes for selected genes across growth conditions and displays the corresponding gene-level summary values.

5. **`05_heatmap.ipynb`** — combines gene-level fold changes across conditions, produces a clustered heatmap, and compares significant-gene overlap between 24-hour and 48-hour measurements.

## Required inputs

Depending on the notebook, the workflow expects:

- an sgRNA count matrix;
- gene-summary and sgRNA-summary result files;
- a PAO1 genome annotation table;
- processed comparison tables produced by the screen-analysis notebook;
- the Lee et al. essential-gene supplementary table; and
- a curated list of genes used in the sgRNA-level plots.


