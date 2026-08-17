🌿 Seasonal Vegetation Dynamics Using Sentinel-2 Remote Sensing

Multi-Index Assessment of Seasonal Vegetation Dynamics in Changunarayan Municipality, Nepal (2025)

Author: Nisha Karki
Year: 2026

📌 Project Overview

This project analyzes seasonal vegetation dynamics in Changunarayan Municipality, Bhaktapur, Nepal, using Sentinel-2 multispectral satellite imagery.

Four vegetation indices were calculated for four seasons of 2025:

NDVI — overall vegetation vigor

GNDVI — chlorophyll and canopy response

NDRE — chlorophyll and vegetation condition

SAVI — vegetation response with reduced soil influence

The workflow used Google Earth Engine for satellite-image processing, Python/Google Colab for data analysis and visualization, and ArcGIS Pro for spatial mapping.

🎯 Objectives

Analyze seasonal vegetation dynamics using Sentinel-2 imagery.

Calculate NDVI, GNDVI, NDRE, and SAVI.

Compare vegetation-index responses across four seasons.

📍 Study Area

Changunarayan Municipality, Bhaktapur, Nepal

The study area contains a mixed landscape including agricultural and other land-cover types. The project examines seasonal variation in vegetation response across the municipality.

🛰️ Data

Parameter

Details

Satellite

Sentinel-2

Sensor

MultiSpectral Instrument (MSI)

Dataset

COPERNICUS/S2_SR_HARMONIZED

Study year

2025

Spatial resolution

10–20 m depending on spectral band

Platform

Google Earth Engine

Study boundary

Changunarayan Municipality

🛠️ Tools

Tool

Purpose

Google Earth Engine

Image filtering, SCL masking, seasonal compositing, vegetation-index calculation

Python / Google Colab

Data analysis, correlation analysis, visualization

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

1️⃣ Image Collection

Sentinel-2 Surface Reflectance Harmonized imagery was filtered to the Changunarayan study area for 2025.

2️⃣ ☁️ Cloud Masking

The Sentinel-2 Scene Classification Layer (SCL) was used for pixel-level masking.

Pixels classified as:

🌱 Vegetation

🟤 Bare soil

💧 Water

were retained.

Unwanted classes, including clouds and cloud shadows, were masked before creating seasonal composites.

3️⃣ 📅 Seasonal Compositing

The year was divided into four seasons:

Season

Period

❄️ Winter

January–February 2025

🌱 Pre-monsoon

March–May 2025

🌧️ Monsoon

June–September 2025

🍂 Post-monsoon

October–December 2025

A median composite was generated for each season.

4️⃣ 🌿 Vegetation-Index Calculation

Four vegetation indices were calculated for each seasonal composite.

🌿 Vegetation Indices

🟢 NDVI — Normalized Difference Vegetation Index

Used to assess general vegetation vigor.

Formula:

NDVI = (NIR - Red) / (NIR + Red)

Sentinel-2 bands:

Red = B4

NIR = B8

🟩 GNDVI — Green Normalized Difference Vegetation Index

Uses the green band and is sensitive to vegetation chlorophyll and canopy condition.

Formula:

GNDVI = (NIR - Green) / (NIR + Green)

Sentinel-2 bands:

Green = B3

NIR = B8

🔵 NDRE — Normalized Difference Red Edge Index

Uses a red-edge band and is sensitive to changes in vegetation chlorophyll and canopy condition.

Formula:

NDRE = (NIR - Red Edge) / (NIR + Red Edge)

Sentinel-2 bands:

Red Edge = B5

NIR = B8

🟠 SAVI — Soil Adjusted Vegetation Index

Reduces the influence of exposed soil on vegetation-index values.

Formula:

SAVI = ((NIR - Red) / (NIR + Red + L)) × (1 + L)

where L = 0.5.

📈 Seasonal Results

The seasonal mean values of the four vegetation indices were compared across winter, pre-monsoon, monsoon, and post-monsoon.

Overall, the vegetation indices showed a clear seasonal pattern:

Values were generally lower during winter.

Vegetation response increased during pre-monsoon.

Values were generally highest during monsoon.

Values decreased again during post-monsoon.

This indicates stronger vegetation activity during the main rainy/growing period.

📊 Figure 1 — Seasonal Vegetation Indices

<img src="https://raw.githubusercontent.com/NishaKarki-Tech/seasonal-vegetation-dynamics-sentinel2/main/Figures/Figure1_Seasonal_Vegetation_Indices.png" alt="Seasonal Vegetation Indices" width="900">

Figure 1. Seasonal variation in NDVI, GNDVI, NDRE, and SAVI during 2025.

🔗 Correlation Among Vegetation Indices

Correlation analysis was used to examine whether the four vegetation indices showed similar seasonal patterns.

The indices showed very strong positive correlations within this seasonal dataset. Because the correlation analysis is based on four seasonal observations, these correlations describe the pattern in this dataset rather than providing broad statistical validation.

📊 Figure 2 — Correlation Among Vegetation Indices

<img src="https://raw.githubusercontent.com/NishaKarki-Tech/seasonal-vegetation-dynamics-sentinel2/main/Figures/Figure3_Correlation_Heatmap.png" alt="Correlation Heatmap" width="900">

Figure 2. Correlation among the four vegetation indices.

🔬 Key Findings

Sentinel-2 successfully captured seasonal vegetation variation in Changunarayan Municipality.

NDVI, GNDVI, NDRE, and SAVI showed clear seasonal changes.

Vegetation-index values were generally highest during the monsoon period.

The four indices showed similar seasonal patterns.

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

seasonal-vegetation-dynamics-sentinel2/
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

Remote Sensing

Sentinel-2 multispectral imagery

Vegetation-index analysis

Seasonal remote sensing

Geospatial Analysis

Google Earth Engine

ArcGIS Pro

Spatial data processing

Data Analysis

Python

Google Colab

Correlation analysis

Data visualization

Research & Reproducibility

GitHub

GEE scripting

Research documentation

📬 Contact

Nisha Karki
Remote Sensing & Precision Agriculture Enthusiast
