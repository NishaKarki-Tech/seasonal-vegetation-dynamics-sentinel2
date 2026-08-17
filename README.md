🌿 Seasonal Vegetation Dynamics Using Sentinel-2 Remote Sensing

Multi-Index Assessment of Seasonal Vegetation Dynamics in Changunarayan Municipality, Nepal (2025)

Author: Nisha Karki
Year: 2026

📌 Project Overview

This project analyzes seasonal vegetation dynamics in Changunarayan Municipality, Bhaktapur, Nepal using Sentinel-2 multispectral satellite imagery.

Four vegetation indices—NDVI, GNDVI, NDRE, and SAVI—were calculated for four seasons of 2025 to compare how vegetation response changed throughout the year.

The workflow used Google Earth Engine for satellite-image processing, Python for data analysis and visualization, and ArcGIS Pro for spatial mapping.

🎯 Objectives

Analyze seasonal vegetation dynamics using Sentinel-2 imagery.

Calculate NDVI, GNDVI, NDRE, and SAVI.

Compare vegetation-index responses across four seasons.

Examine the relationships among the vegetation indices.

Develop a reproducible Google Earth Engine workflow for seasonal vegetation monitoring.

Visualize the results using Python and GIS.

📍 Study Area

Changunarayan Municipality, Bhaktapur, Nepal

The study area contains a mixed landscape including agricultural and other land-cover types. The project examines seasonal variation in vegetation response across the municipality.

🛰️ Data

Sentinel-2 MSI Surface Reflectance

Satellite: Sentinel-2

Sensor: MultiSpectral Instrument (MSI)

Dataset: COPERNICUS/S2_SR_HARMONIZED

Study year: 2025

Spatial resolution: 10–20 m depending on the spectral band

Platform: Google Earth Engine

A Changunarayan Municipality boundary was used to define the study area.

🛠️ Tools

Tool

Purpose

Google Earth Engine

Image filtering, SCL-based masking, seasonal compositing, and vegetation-index calculation

Python / Google Colab

Data analysis, correlation analysis, and visualization

ArcGIS Pro

Spatial visualization and map preparation

GitHub

Code, data, figures, and documentation

🔬 Methodology

Workflow

Sentinel-2 imagery
↓
Study-area filtering
↓
SCL-based pixel masking
↓
Seasonal median composites
↓
NDVI + GNDVI + NDRE + SAVI
↓
Seasonal comparison
↓
Correlation analysis and visualization

1. Image Collection

Sentinel-2 Surface Reflectance Harmonized imagery was filtered to the Changunarayan study area for 2025.

2. Cloud Masking

The Sentinel-2 Scene Classification Layer (SCL) was used to retain pixels classified as:

Vegetation

Bare soil

Water

Other classes, including clouds and cloud shadows, were masked before creating the seasonal composites.

3. Seasonal Compositing

Median composites were generated for:

Season

Period

Winter

January–February 2025

Pre-monsoon

March–May 2025

Monsoon

June–September 2025

Post-monsoon

October–December 2025

4. Vegetation-Index Calculation

The four vegetation indices were calculated for each seasonal composite.

🌿 Vegetation Indices

NDVI — Normalized Difference Vegetation Index

Used to assess general vegetation vigor.

NDVI = (NIR - Red) / (NIR + Red)

Sentinel-2 bands:

Red = B4

NIR = B8

GNDVI — Green Normalized Difference Vegetation Index

Uses the green band and is sensitive to vegetation chlorophyll and canopy condition.

GNDVI = (NIR - Green) / (NIR + Green)

Sentinel-2 bands:

Green = B3

NIR = B8

NDRE — Normalized Difference Red Edge Index

Uses a red-edge band and is sensitive to changes in vegetation chlorophyll and canopy condition.

NDRE = (NIR - Red Edge) / (NIR + Red Edge)

Sentinel-2 bands used:

Red Edge = B5

NIR = B8

SAVI — Soil Adjusted Vegetation Index

Reduces the influence of exposed soil on vegetation-index values.

SAVI = ((NIR - Red) / (NIR + Red + 0.5)) × 1.5

where L = 0.5 is the soil-adjustment factor.

📈 Seasonal Results

The seasonal mean values of the four vegetation indices were compared across winter, pre-monsoon, monsoon, and post-monsoon.

The results show that the vegetation indices generally increased during the monsoon period and decreased after the monsoon, indicating stronger vegetation response during the main rainy/growing period.

## Figure 1 — Seasonal Vegetation Indices

![Seasonal Vegetation Indices](https://raw.githubusercontent.com/NishaKarki-Tech/seasonal-vegetation-dynamics-sentinel2/main/Figures/Figure1_Seasonal_Vegetation_Indices.png)

**Figure 1.** Seasonal variation in NDVI, GNDVI, NDRE, and SAVI during 2025.

## Figure 2 — Correlation Among Vegetation Indices

![Correlation Heatmap](https://raw.githubusercontent.com/NishaKarki-Tech/seasonal-vegetation-dynamics-sentinel2/main/Figures/Figure3_Correlation_Heatmap.png)

**Figure 2.** Correlation among the four vegetation indices.

🔬 Key Findings

Sentinel-2 imagery was used to assess seasonal vegetation dynamics in Changunarayan Municipality.

NDVI, GNDVI, NDRE, and SAVI showed clear seasonal variation.

Vegetation-index values were generally highest during the monsoon period.

The four indices showed very strong positive relationships in the seasonal dataset.

The workflow demonstrates the integration of Google Earth Engine, Python, and GIS for remote-sensing-based vegetation monitoring.

💻 Google Earth Engine

The Sentinel-2 processing and vegetation-index workflow was developed in Google Earth Engine.

The script includes:

Sentinel-2 image filtering

SCL-based pixel masking

Seasonal median compositing

NDVI calculation

GNDVI calculation

NDRE calculation

SAVI calculation

Seasonal statistics

Data export

GEE script: GEE/vegetation_analysis.js

📂 Repository Structure

crop-stress-monitoring-sentinel2/
│
├── DATA/
│   └── Seasonal_Vegetation_Indices_2025.csv
│
├── Figures/
│   ├── Figure1_Seasonal_Vegetation_Indices.png
│   └── Figure3_Correlation_Heatmap.png
│
├── GEE/
│   └── vegetation_analysis.js
│
└── README.md

Other files from earlier exploratory analysis may remain in the repository but are not presented as part of the main seasonal vegetation analysis.

🚀 Future Improvements

Apply an agricultural/crop-land mask for crop-specific analysis.

Validate satellite-derived vegetation patterns with field observations.

Integrate UAV imagery for higher-resolution validation.

Extend the analysis to multiple years.

Integrate weather and environmental data.

Explore machine-learning approaches for crop monitoring.

📚 Skills Demonstrated

Google Earth Engine

Sentinel-2 Multispectral Remote Sensing

Vegetation Index Analysis

Seasonal Remote Sensing Analysis

Python Data Analysis and Visualization

GIS Mapping

Spatial Data Processing

Agricultural Remote Sensing

GitHub Documentation

📬 Contact

Nisha Karki
Remote Sensing & Precision Agriculture Enthusiast
