# Melbourne Solar Adoption Analysis
## Geospatial Clustering Analysis of Residential Solar Energy Patterns

**Author:** Claudia Chu  
**Date:** November 2025  
**Tools:** Python, pandas, geopandas, scikit-learn, folium, matplotlib, seaborn  
**Context:** Independent analysis simulating a brief commissioned by ARENA  

---

## Overview

This project investigates what drives solar energy adoption across Melbourne's 
residential postcodes by integrating three public datasets — solar installation 
records from the Clean Energy Regulator (CER), housing market data from Kaggle, 
and postcode boundary shapefiles from the Australian Bureau of Statistics (ABS).

K-means clustering (k=3) is applied to identify distinct market segments based on 
property price, distance to CBD, solar capacity, and installation density. Results 
are visualised through interactive geospatial maps using Folium.

---

## Key Findings

- **3 distinct market segments** identified across Melbourne postcodes, validated 
  by Elbow and Silhouette methods
- **Outer suburbs lead adoption** — highest kW_per_property and units_per_property, 
  driven by larger land size and detached housing
- **Inner city postcodes show lowest uptake** despite highest property values — 
  density and space constraints override financial capacity
- **kW_per_unit is consistent across all clusters** — adoption differences are 
  behavioural and locational, not technological
- **Cluster boundaries align with postcode geography**, confirming spatial coherence 
  and supporting location-based policy design

---

## Data Sources

| Source | Dataset | Access |
|---|---|---|
| [Clean Energy Regulator](https://www.cer.gov.au) | Solar capacity & installations by postcode (2011–present) | Public URL |
| [Kaggle](https://www.kaggle.com/datasets/anthonypino/melbourne-housing-market) | Melbourne housing market | Manual download |
| [Australian Bureau of Statistics](https://www.abs.gov.au) | Postcode boundary shapefiles (ASGS 2021) | Manual download |

---

## Repository Structure
```
melbourne-solar-adoption-analysis/
│
├── README.md
├── notebooks/
│   └── solar_adoption_analysis_melbourne.ipynb
└── data/
    └── .gitkeep
```

> Data files are not included. Download from the sources above and place in `data/` folder.  
> Required files: CER CSVs (loaded directly from URL), Melbourne housing CSVs, POA_2021 shapefile.

---

## How to Run

1. Clone the repository
2. Create and activate a virtual environment
3. Install dependencies:
```
pip install pandas geopandas numpy scikit-learn folium matplotlib seaborn jupyter
```
4. Download data files and place in `data/` folder
5. Open `notebooks/solar_adoption_analysis_melbourne.ipynb` in JupyterLab

---

## Skills Demonstrated

- Data integration from multiple heterogeneous sources
- Geospatial analysis with GeoPandas and Folium
- Unsupervised machine learning (K-means clustering)
- Feature engineering and normalisation
- Interactive choropleth mapping
- Evidence-based policy recommendations
