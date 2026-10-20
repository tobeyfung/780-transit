# 780-transit

Transportation convenience analysis across U.S. cities (2020–2023), focused on helping students and recent graduates compare car-free mobility options.

## Project Overview

This repository contains a single Jupyter notebook:

- `/home/runner/work/780-transit/780-transit/A03-Transportation-Convenience-Across-US cities.ipynb`

The notebook combines public data on population, transit funding, transit ridership, and walkability to build a **Transportation Convenience Score** (0–100) for 230 U.S. cities across 2020–2023 (920 city-year observations).

## Main Goal

Evaluate how transportation convenience differs by city size tier and whether population growth is associated with changes in convenience over time.

City tiers used in the analysis:

- **Small:** under 100K population  
- **Medium:** 100K–450K population  
- **Big:** 450K+ population

## Data Sources Used in the Notebook

1. U.S. Census city/town population estimates (`data/population_2020.xlsx`)
2. FTA total funding time series (`data/2024 TS1.1 Total Funding Time Series.xlsx`)
3. FTA monthly ridership data (`data/ridership.xlsx`)
4. Social Data Commons walkability index (`data/2017_2023_walkability_index.csv`)
5. EPA National Walkability Index shapefile (`Natl_WI.shp`)
6. 2010 Census DP1 Places shapefile (`Place_2010Census_DP1.zip`)

## High-Level Workflow

1. Import and clean each source dataset.
2. Standardize city/state naming and align years (2020–2023).
3. Aggregate walkability to city-level metrics.
4. Merge population, transit, and walkability data.
5. Compute convenience components:
   - transit funding per capita
   - transit ridership per capita
   - walkability
6. Min-max scale components and combine them equally into a final score.
7. Compare results across tiers, regions, and years with EDA visualizations.

## Key Findings (from notebook narrative)

- Big cities generally score highest on overall transportation convenience.
- Several small/medium cities perform at or above big-city averages.
- Walkability is strongly associated with overall convenience.
- Population growth (2020–2023) shows weak relationship with convenience changes.

## Environment Notes

The notebook was authored in Google Colab and mounts Google Drive paths (e.g., `/content/drive/...`) for data access. To run it locally, update file paths and ensure the required datasets are available.

Core libraries used:

- `numpy`
- `pandas`
- `seaborn`
- `matplotlib`
- `geopandas`

## Repository Contents

- `A03-Transportation-Convenience-Across-US cities.ipynb` — full analysis notebook
- `README.md` — project summary (this file)
