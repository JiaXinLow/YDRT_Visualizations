# Developing an Effort-Aware Visual Analytics Framework for Interpreting Citizen Science Riverfly Monitoring Data  
### A Case Study of the River Nidd (2015–2025)  
**In collaboration with the Yorkshire Dales Rivers Trust (YDRT)**
By Low Jia Xin
---

## Overview

This repository contains a fully reproducible Jupyter Notebook-based analytical workflow for exploring long-term Riverfly monitoring data collected across the River Nidd catchment between 2015 and 2025.

The dataset consists of citizen science macroinvertebrate records collected by volunteers as part of the Riverfly Monitoring Initiative. These taxa are widely used as bioindicators of freshwater ecosystem health due to their sensitivity to pollution and environmental disturbance.

---
## Objectives
This project develops a structured analytical pipeline to:
- Standardise and clean volunteer-collected ecological monitoring data.  
- Account for uneven sampling effort across sites and years.  
- Visualise spatial and temporal patterns in riverfly communities.  
- Support ecological interpretation of river health trends.  
- Enable transparent and reproducible citizen science analysis.
---
## Research Questions
The analysis is structured around four key ecological questions:

**RQ1 – Monitoring Effort**

How does survey effort vary across sites and years, and to what extent are monitoring targets (6 surveys per site per year) achieved?

**RQ2 – Spatial Variation**

How can monitoring sites be ordered along the River Nidd (upstream → downstream), and how does species richness vary along this gradient?

**RQ3 – Between-Site Community Structure**

How does riverfly community composition differ between monitoring sites across the catchment?

**RQ4 – Within-Site Temporal Dynamics**

How do riverfly communities change over time within individual monitoring sites?

---
## Methodological Approach
This workflow implements an **effort-aware ecological analytics framework**, consisting of four core stages:
### 1. Data Preparation
- Loading raw Excel-based monitoring records
- Data validation (missing values, duplicates, structure checks)
- Cleaning and standardisation of variables
- Date parsing and categorical formatting
- Export of cleaned dataset for reproducibility
### 2. Effort Standardisation
To ensure comparability across uneven sampling effort:

$$
\bar{x}_{s,y,t} = \frac{S_{s,y,t}}{N_{s,y}}
$$

Where:
- \(S_{s,y,t}\): total abundance of taxon *t* at site *s* in year *y*
- \(N_{s,y}\): number of surveys at site *s* in year *y*
- \(\bar{x}_{s,y,t}\): mean abundance per survey
---
### 3. Spatial Structuring
- Manual upstream-to-downstream ordering of sites
- Justification due to river meander complexity
- Spatial interpretation aligned with catchment hydrology rather than raw coordinates
---
### 4. Ecological Visual Analytics
The notebook includes multiple interactive visualisations:
#### Monitoring Effort
- Time series of total and site-level survey frequency
- Heatmaps of survey coverage
- Site-level monitoring performance ranking
#### Spatial Patterns
- River flow map of monitoring locations
- ARMI-based river health gradients
- Species richness heatmaps across space and time
#### Community Structure
- Species abundance matrices
- Effort-standardised abundance heatmaps
- Spatial–temporal species distribution trends
- Animated visualisations of ecological change over time
#### Temporal Dynamics
- Site-level time series of riverfly abundance
- Relative abundance (community composition shifts)
---
## Key Outputs
The framework produces:
- Cleaned and standardised ecological dataset (`riverfly_cleaned.xlsx`).
- Interactive Plotly visualisations.
- Spatial flow mapping of monitoring sites.
- Effort-adjusted ecological indicators (mean abundance per survey).
- Species richness and community composition trends.
- Site ranking based on monitoring consistency.
---
## Assumptions and Design Choices
- Missing numerical values are treated as zero abundance.
- Missing categorical values are labelled as `not_applicable`.
- Site ordering is manually defined based on hydrological knowledge.
- Relative abundance is used to control for differences in total abundance.
---
## Limitations
- Citizen science sampling is inherently uneven in space and time.
- Survey effort is not fully randomised across sites.
- Some years/sites may have limited data coverage.
- Manual spatial ordering introduces expert-dependent assumptions.
- Taxonomic resolution depends on volunteer identification accuracy.
---
## Technologies Used
- Python (pandas, numpy)
- Plotly (interactive visualisation)
- Folium (spatial mapping)
- Jupyter Notebook
- Excel-based ecological datasets
---
## Reproducibility
All analyses are fully reproducible within the provided notebook:
1. Load raw dataset  
2. Run validation and cleaning pipeline  
3. Execute analysis sections sequentially  
4. Generate interactive visual outputs  
---
## License
This project is intended for academic and non-commercial research use unless otherwise specified.

---
