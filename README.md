[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.15881253.svg)](https://doi.org/10.5281/zenodo.15881253)

# GAZEL-ADN notebook

<img src="logo.png" alt="Logo" width="250" align="left" style="margin-right: 15px; margin-bottom: 10px;" />

This repository contains the data and scripts necessary to reproduce all figures in the paper: *“Performing human whole genome sequencing from saliva samples provides highly reliable information about the salivary microbiome.”* The study evaluates whether standard host-DNA extraction protocols can reliably support salivary microbiome profiling when paired with deep shotgun sequencing.

This analysis compares two saliva sample sets:

- **GAZEL-ADN samples**: Collected using Oragene saliva kits (DNA Genotek™) and extracted using Maxwell magnetic bead–based technology (PROMEGA™). Sequenced on an Illumina NovaSeq 6000 with the TruSeq PCR-free protocol.  
- **ASAL samples**: Fastq files downloaded from ENA under accession [PRJEB57658](https://www.ebi.ac.uk/ena/browser/view/PRJEB57658). DNA was extracted using two microbiome-oriented protocols and sequenced using the Ion Proton platform.

All data used in this analysis were processed for human read removal and taxonomic profiling as described in the manuscript.

Both datasets were analyzed using:
- [`meteor`](https://github.com/metagenopolis/meteor): for genome coverage–based profiling using their [saliva-specific microbial reference database](https://zenodo.org/records/14181351).
- [`sylph`](https://github.com/bluenote-1577/sylph): for broad taxonomic classification using the [GTDB](https://gtdb.ecogenomic.org/) (release R220, April 2024).

<br clear="left"/>

## 📌 TL;DR

<details>
<summary><strong>🧬 Background</strong></summary>

The salivary microbiome is a key indicator of health and immunity. While saliva samples are widely collected for human DNA analysis in genomic biobanks, these protocols are not optimized for microbial recovery — raising concerns about their microbiome profiling utility.

</details>

<details>
<summary><strong>🔍 Key Findings</strong></summary>

- Deep sequencing compensates for the lack of microbial-specific extraction.
- Higher microbial richness and reproducibility in GAZEL-ADN samples.
- Species-level resolution is maintained even without lysis-focused protocols.
- Community structures converge between protocols after rarefaction.
- GAZEL-ADN shows lower variability at fine taxonomic levels (per FAVA).

</details>

---

## 📁 Repository structure

- `data/`: Sample metadata and example output files   
- `figures/`: Exported figures from the manuscript  
- `env/`: Conda environment files and package dependencies  
- `notebooks/`: Jupyter notebooks for exploratory analyses and used to generate each figure 

Each of the three figures/analyses presented in the paper corresponds to a different Jupyter notebook in the `notebooks/` repository:

1. `alpha-beta.ipynb`

2. `FAVA.ipynb`

3. `KS-CM.ipynb`


