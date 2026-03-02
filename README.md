# HaitiAeaeENM

This repository contains data, code, figures, and interactive visualizations associated with a species distribution modelling study of *Aedes aegypti* in Haiti. The study predicts current and future habitat suitability under multiple climate warming scenarios and integrates these predictions with population and vulnerability metrics to assess spatial patterns of potential public health risk.

An interactive project website is hosted via GitHub Pages and serves as the primary entry point for exploring results and maps:

**https://ianpsheasmith.github.io/HaitiAeaeENM/**

---

## Overview

*Aedes aegypti* is the primary vector of dengue, Zika, chikungunya, and yellow fever viruses, pathogens of ongoing public health importance worldwide, and either currently or historically in Haiti. This project applies distribution modelling to quantify how climatic suitability for *Ae. aegypti* is expected to change under global warming, and to examine how these changes intersect with population exposure and measures of humanitarian deprivation.

Key components of the analysis include:
- ensemble boosted regression tree (BRT) models
- current (baseline) and future climate projections using warming levels (+1.5°C to +4°C)
- population exposure estimates
- integration with humanitarian deprivation metrics to produce composite risk indices

---

## Repository Structure

```text
HaitiAeaeENM/
├── index.html
├── README.md
├── Data/
│   ├── Covars/
│   ├── Ensemble_Rasters/
│   ├── HaitiShapefiles/
│   ├── JIAF_Data/
│   ├── PseudoAbsence_Datasets/
│   └── WarmingLevelsList/
├── Figures/
├── Haiti_Aeae_Preds.html
├── Haiti_Aeae_Preds_files/
├── Haiti_Communes_Map.html
├── Haiti_Communes_Map_files/
├── Haiti_Risk_Map.html
└── Haiti_Risk_Map_files/
````

The `*_files/` directories contain JavaScript and CSS dependencies required for Leaflet-based interactive maps and should be kept alongside their corresponding HTML files.

---

## Data

All datasets required to reproduce analyses are contained in the `Data/` directory.

### Occurrence and spatial data

* **`Data/HaitiShapefiles/HaitiTrapsBin.csv`**
  Presence locations of *Aedes aegypti* used for model training.

* **`Data/HaitiShapefiles/`**
  Administrative boundaries and national shapefiles for Haiti, including versions with water bodies removed.

### Environmental covariates

* **`Data/Covars/Haiti_bioclim_covars.grd/.gri`**
  Raster stack of WorldClim 2.1 bioclimatic variables (~1 km resolution).

### Climate warming scenarios

* **`Data/WarmingLevelsList/cmip6_warming_levels_Hauser2022.csv`**
  Lookup table assigning CMIP6 model projections to warming levels following Hauser et al. (2022).

### Vulnerability and exposure

* **`Data/JIAF_Data/jiaf_haiti_2025.xlsx`**
  Joint Intersectoral Analysis Framework (JIAF) humanitarian needs data used to construct deprivation indices.

### Pseudo-absence datasets

* **`Data/PseudoAbsence_Datasets/`**
  Replicated pseudo-absence datasets (`.rds`) used for ensemble model fitting.

### Ensemble predictions

* **`Data/Ensemble_Rasters/`**
  Raster outputs summarizing ensemble predictions (mean, median, SD, CV, confidence intervals).

---

## Analysis Code

* **`Supp_File_3.rmd`**
  R Markdown document containing the complete analytical workflow, including:

  * data preprocessing and covariate extraction
  * pseudo-absence generation
  * BRT model fitting and evaluation
  * baseline and future predictions
  * population exposure and risk index construction
  * map and figure generation

Rendering this document reproduces the analyses and outputs presented in the manuscript and on the project website.
All code was confirmed functional and reproducible at time of publication, however please note that some modifications to directories are required to run the code from beginning to end, and some chunks require both large storage quotas and significant computational requirements.

---

## Figures and Supplementary Outputs

All manuscript figures and supplemental materials are stored in the `Figures/` directory.

This includes:

* main manuscript figures (`Figure_1.tif` – `Figure_4.tif`)
* supplemental figures
* supplemental tables and data files

These files are intended for direct reuse and citation.

---

## Interactive Maps

This repository includes several Leaflet-based interactive maps:

* **`Haiti_Aeae_Preds.html`**
  Baseline ensemble suitability predictions for *Aedes aegypti*.

* **`Haiti_Communes_Map.html`**
  Commune-level summaries of predicted suitability.

* **`Haiti_Risk_Map.html`**
  Integrated risk maps combining suitability, population exposure, and vulnerability metrics.

These maps are accessible via GitHub Pages at URLs of the form:

```
https://ianpsheasmith.github.io/HaitiAeaeENM/<map_name>.html
```

---

## Usage

### Clone the repository

```bash
git clone https://github.com/IanPsheaSmith/HaitiAeaeENM.git
cd HaitiAeaeENM
```

### Reproduce analyses

1. Open `Supp_File_3.rmd` in RStudio or another compatible IDE.
2. Install required R packages listed at the top of the document.
3. Render the file to reproduce analyses and outputs.

---

## Citation

If you use this repository in your work, please cite the associated manuscript (citation will be updated upon publication):

> Pshea-Smith, I.A., Okech, B., Boncy, J., Existe, A., Punch, B., Matulis, G.A., Koehler, J.W., Dunford, J., Blackburn, J.K., von Fricken, M.E. (2025). *Increasing suitability of Aedes aegypti as a global health equity issue under warming temperature regimes in the country of Haiti.* Manuscript in preparation.

---

## Contact

Ian Pshea-Smith — [ianpsheasmith@ufl.edu](mailto:ianpsheasmith@ufl.edu)
Michael E. von Fricken — [mvonf@phhp.ufl.edu](mailto:mvonf@phhp.ufl.edu)
