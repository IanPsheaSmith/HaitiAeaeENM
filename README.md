# HaitiAeaeENM

This repository contains data and code associated with a species distribution modeling study of _Aedes aegypti_ in Haiti. The study aims to predict the current and future distribution of _Ae. aegypti_ across Haiti under various climate warming scenarios and to assess population risk associated with mosquito habitat suitability.

## Repository Contents

### Datasets

- **HaitiTrapsBin.csv**  
  Contains coordinates and presence locations for _Aedes aegypti_ across Haiti, used as occurrence data for the ecological niche models.

- **HaitiShapefiles folder**  
  Contains spatial data files for mapping and analysis:
  - `HaitiPolygon.shp`: Base shapefile for Haiti
  - `Haiti_no_Wtrwy.shp`: Haiti shapefile with bodies of water removed
  - `hti_admbnda_adm3_cnigs_20181129.shp`: Haiti's 1st-3rd level administrative divisions, enabling visualization of administrative districts (communes and communal sections)

- **WarmingLevelsList folder**  
  Contains a CSV file from Hauser et al. (2022) with warming level assignments for Global Climate Models (GCMs). The file includes columns for:
  - Model name
  - Shared Socioeconomic Pathway (SSP)
  - Warming level (1.5°C, 2°C, 3°C, and 4°C)
  - Approximate dates
  
  These data are used to assign appropriate climate projections for future habitat suitability predictions.

### Analysis Code

- **HaitiENM.qmd**  
  Quarto markdown file containing all code for:
  - Boosted regression tree (BRT) modeling
  - Current habitat suitability predictions
  - Future habitat suitability under climate warming scenarios
  - Population at risk analyses
  - Map generation and visualization

## Usage Instructions

1. Clone the repository:
   ```bash
   git clone https://github.com/IanPsheaSmith/HaitiAeaeENM.git
   ```
2. Open the `HaitiENM.qmd` file in RStudio or another Quarto-compatible IDE.
3. Install any required R packages (listed at the top of the `.qmd` file).
4. Render the document to reproduce analyses, outputs, and figures.

## Citation

If you use this code or data in your research, please cite the associated manuscript:

> Pshea-Smith, I.A., Okech, B., Boncy, J., Existe, A., Punch, B., Matulis, G.A., Koehler, J.W., Dunford, J., Blackburn, J.K., von Fricken, M.E. (2025). Increasing suitability of <i>Aedes aegypti</i> as a global health equity issue under warming temperature regimes in the country of Haiti. [Manuscript in preparation]

## Funding and Disclaimer

This work was funded by the Armed Forces Health Surveillance Branch (AFHSB), Global Emerging Infections Surveillance (GEIS) Section, under ProMIS ID (P0154_24_EC and P0118-24-RD). These funders had no role in study design, data collection and analysis, decision to publish, or preparation of the manuscript. This work was also funded in part through Battelle Memorial Institute's contract with the Information Analysis Center Multiple Award Contract (IAC MAC) No. FA807518D0005-FA807523F0016: Ongoing Force Health Protection (FHP) Analysis, Assessment, and Evaluation for Navy and Marine Corps Force Health Protection Command (NMCFHPC). This material is based upon work supported by the DoD Information Analysis Center Program Management Office (DoD IAC PMO) and the Navy and Marine Corps Force Health Protection Command (NMCFHPC) under Contract No. FA807518D0005-FA807523F0016. Any opinions, findings and conclusions or recommendations expressed in this material are those of the author(s) and do not necessarily reflect the views of the US Navy and Marine Corps Force Health Protection Command (NMCFHPC), the 774 Enterprise Sourcing Squadron (774 ESS), the Air Force Installation Contracting Center (AFICC), the DoD Information Analysis Center Program Management Office (DoD IAC PMO), or of the institutions and companies affiliated with the authors.

The use of either trade or manufacturers' names in this repository does not constitute an official endorsement of any commercial products. This repository may not be cited for purposes of advertisement. The opinions, interpretations, conclusions, recommendations and views in this repository are those of the authors and do not necessarily reflect the official policy or position of the Uniformed Services University of the Health Sciences, Department of the Army, Department of the Navy, Department of Defense, nor the U.S. Government. Multiple authors are military service members of the U.S. Government. This work was prepared as part of their official duties. Title 17, U.S.C., §105 provides that copyright protection under this title is not available for any work of the U.S. Government. Title 17, U.S.C., §101 defines a U.S. Government work as a work prepared by a military Service member or employee of the U.S. Government as part of that person's official duties.

## Contact

For questions or collaborations, please contact:  
Ian Pshea-Smith: ianpsheasmith@ufl.edu  
Michael von Fricken: mvonf@phhp.ufl.edu
