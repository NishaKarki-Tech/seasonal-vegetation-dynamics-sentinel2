Seasonal Vegetation Dynamics Using Sentinel-2 Remote Sensing

Multi-Index Assessment of Seasonal Vegetation Dynamics in Changunarayan Municipality, Nepal (2025)

Author: Nisha Karki
Year: 2026

📌 Project Overview

This project analyzes seasonal vegetation dynamics in Changunarayan Municipality, Bhaktapur, Nepal using Sentinel-2 multispectral satellite imagery and vegetation indices.

Four vegetation indices—NDVI, GNDVI, NDRE, and SAVI—were calculated for four seasons of 2025 to compare how vegetation response changed throughout the year. The workflow combines Google Earth Engine for satellite-data processing, Python for data analysis and visualization, and ArcGIS Pro for spatial mapping.

🎯 Objectives

Analyze seasonal vegetation dynamics using Sentinel-2 imagery.

Calculate NDVI, GNDVI, NDRE, and SAVI for seasonal vegetation assessment.

Compare vegetation-index responses across winter, pre-monsoon, monsoon, and post-monsoon periods.

Examine the relationships among the vegetation indices.

Develop a reproducible Google Earth Engine workflow for seasonal vegetation monitoring.

Visualize seasonal vegetation patterns using Python and GIS.

📍 Study Area

Changunarayan Municipality, Bhaktapur, Nepal

The study area contains a mixed landscape including agricultural and other land-cover types. The analysis examines the spatial and seasonal variation in vegetation response across the municipality.

🛰️ Data

Sentinel-2 MSI Surface Reflectance

Satellite: Sentinel-2

Sensor: MultiSpectral Instrument (MSI)

Dataset: COPERNICUS/S2_SR_HARMONIZED

Study period: 2025

Spatial resolution: 10–20 m depending on the spectral band

Platform: Google Earth Engine

A Changunarayan Municipality boundary was used to define the study area.

🛠️ Tools

Tool

Purpose

Google Earth Engine

Sentinel-2 filtering, SCL masking, seasonal compositing, index calculation, and export

Python / Google Colab

Data analysis, comparison, correlation analysis, and visualization

ArcGIS Pro

Spatial visualization and map preparation

GitHub

Code, figures, data, and project documentation

🔬 Methodology

Overall workflow

Sentinel-2 imagery
↓
Study-area filtering
↓
SCL-based unwanted-pixel masking
↓
Seasonal median composites
↓
NDVI + GNDVI + NDRE + SAVI
↓
Seasonal mean calculation
↓
Seasonal comparison and correlation analysis
↓
Visualization and GIS mapping

1. Sentinel-2 image collection

Sentinel-2 Surface Reflectance Harmonized imagery was filtered to the Changunarayan study area for 2025.

2. Cloud and unwanted-pixel masking

The Sentinel-2 Scene Classification Layer (SCL) was used to retain pixels classified as:

Vegetation

Bare soil

Water

Other SCL classes, including cloud and cloud-shadow classes, were excluded before creating seasonal composites.

This pixel-level masking helps reduce contamination of the vegetation-index calculations by clouds and their shadows.

3. Seasonal composites

Median composites were generated for four periods:

Season

Period used

Winter

January–February 2025

Pre-monsoon

March–May 2025

Monsoon

June–September 2025

Post-monsoon

October–December 2025

4. Vegetation-index calculation

The four indices were calculated for each seasonal composite.

🌿 Vegetation Indices

1. NDVI — Normalized Difference Vegetation Index

NDVI is a widely used index for assessing general vegetation vigor.

Formula:

NDVI = (NIR - Red) / (NIR + Red)

For Sentinel-2:

Red = B4

NIR = B8

2. GNDVI — Green Normalized Difference Vegetation Index

GNDVI replaces the red band with the green band and is sensitive to variation in vegetation chlorophyll and canopy condition.

Formula:

GNDVI = (NIR - Green) / (NIR + Green)

For Sentinel-2:

Green = B3

NIR = B8

3. NDRE — Normalized Difference Red Edge Index

NDRE uses a red-edge band and is sensitive to changes in vegetation chlorophyll and canopy condition.

Formula:

NDRE = (NIR - Red Edge) / (NIR + Red Edge)

In this project:

Red Edge = B5

NIR = B8

4. SAVI — Soil Adjusted Vegetation Index

SAVI reduces the influence of exposed soil on vegetation-index values.

Formula used in the project:

SAVI = ((NIR - Red) / (NIR + Red + 0.5)) × 1.5

where L = 0.5 is the soil-adjustment factor.

📈 Seasonal Analysis

The seasonal mean values of all four vegetation indices were calculated and compared.

The analysis provides a simple way to examine how vegetation response changes from:

Winter → Pre-monsoon → Monsoon → Post-monsoon

The seasonal results show that vegetation-index values generally increased during the monsoon period and decreased after the monsoon, indicating stronger vegetation response during the main rainy/growing period.

📊 Results

Seasonal Vegetation Indices



Figure 1. Seasonal variation in NDVI, GNDVI, NDRE, and SAVI during 2025.

The figure shows that all four indices followed broadly similar seasonal patterns, with their highest values occurring during the monsoon period.

Correlation Among Vegetation Indices



Figure 2. Correlation among the four vegetation indices.

The indices showed very strong positive correlations in the seasonal dataset, indicating that they generally followed similar seasonal patterns.

Note: The correlation analysis is based on the seasonal observations and is used here as a descriptive comparison of the indices.

🔬 Key Findings

Sentinel-2 imagery was successfully used to assess seasonal vegetation dynamics in Changunarayan Municipality.

NDVI, GNDVI, NDRE, and SAVI all showed clear seasonal variation.

Vegetation-index values were generally highest during the monsoon period.

The four indices showed very strong positive relationships in the seasonal dataset.

The workflow demonstrates how Google Earth Engine, Python, and GIS can be combined for satellite-based vegetation monitoring.

💻 Google Earth Engine

The main preprocessing and vegetation-index workflow was developed in Google Earth Engine.

The script includes:

Sentinel-2 image filtering

SCL-based pixel masking

Seasonal median compositing

NDVI calculation

GNDVI calculation

NDRE calculation

SAVI calculation

Seasonal mean statistics

CSV export

GEE script: vegetation_analysis.js

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

Other files generated during earlier exploratory analysis may remain in the repository but are not part of the main seasonal vegetation analysis presented here.

🚀 Future Improvements

Apply an agricultural/crop-land mask for crop-specific analysis.

Validate satellite-derived vegetation patterns using field observations.

Integrate UAV imagery for higher-resolution validation.

Extend the analysis to multiple years.

Incorporate weather and environmental variables.

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
