🌿 Seasonal Vegetation Dynamics Using Sentinel-2 Remote Sensing
Multi-Index Assessment of Seasonal Vegetation Dynamics in Changunarayan Municipality, Nepal (2025)

Author: Nisha Karki
Year: 2026

📌 Project Overview

This project analyzes seasonal vegetation dynamics in Changunarayan Municipality, Bhaktapur, Nepal, using Sentinel-2 multispectral satellite imagery.

Four vegetation indices were calculated for four seasons of 2025:

NDVI — general vegetation vigor
GNDVI — chlorophyll and canopy response
NDRE — chlorophyll and vegetation condition
SAVI — vegetation response with reduced soil influence

The analysis compares how vegetation response changed throughout the year.

The workflow used Google Earth Engine for satellite-image processing, Python / Google Colab for data analysis and visualization, and ArcGIS Pro for spatial mapping.

🎯 Objectives
Analyze seasonal vegetation dynamics using Sentinel-2 imagery.
Calculate NDVI, GNDVI, NDRE, and SAVI.
Compare vegetation-index responses across four seasons.
📍 Study Area

Changunarayan Municipality, Bhaktapur, Nepal

The study area contains a mixed landscape including agricultural areas and other land-cover types. The project examines seasonal variation in vegetation response across the municipality.

🛰️ Data
Item	Details
Satellite	Sentinel-2
Sensor	MultiSpectral Instrument (MSI)
Dataset	COPERNICUS/S2_SR_HARMONIZED
Study year	2025
Spatial resolution	10–20 m depending on spectral band
Platform	Google Earth Engine
Study area boundary	Changunarayan Municipality
🛠️ Tools Used
Tool	Purpose
Google Earth Engine	Image filtering, SCL masking, seasonal compositing, vegetation-index calculation
Python / Google Colab	Data analysis, correlation analysis, visualization
ArcGIS Pro	Spatial visualization and map preparation
GitHub	Code, data, figures, and documentation
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

1️⃣ Sentinel-2 Image Collection

Sentinel-2 Surface Reflectance Harmonized imagery was filtered to the Changunarayan Municipality boundary for 2025.

2️⃣ ☁️ Cloud Masking

The Sentinel-2 Scene Classification Layer (SCL) was used for pixel-level masking.

Pixels classified as:

🌱 Vegetation
🟤 Bare soil
💧 Water

were retained.

Unwanted classes, including clouds and cloud shadows, were masked before creating the seasonal composites.

3️⃣ 📅 Seasonal Compositing

The year was divided into four seasons:

Season	Period
❄️ Winter	January–February 2025
🌱 Pre-monsoon	March–May 2025
🌧️ Monsoon	June–September 2025
🍂 Post-monsoon	October–December 2025

A median composite was generated for each season.

4️⃣ 🌿 Vegetation-Index Calculation

Four vegetation indices were calculated for each seasonal composite.

🌿 Vegetation Indices
1. 🟢 NDVI — Normalized Difference Vegetation Index

Used to assess general vegetation vigor.

Formula:

NDVI = (NIR − Red) / (NIR + Red)

Sentinel-2 bands:

Red = B4
NIR = B8
2. 🟩 GNDVI — Green Normalized Difference Vegetation Index

Uses the green band and is sensitive to vegetation chlorophyll and canopy condition.

Formula:

GNDVI = (NIR − Green) / (NIR + Green)

Sentinel-2 bands:

Green = B3
NIR = B8
3. 🔵 NDRE — Normalized Difference Red Edge Index

Uses a red-edge band and is sensitive to changes in vegetation chlorophyll and canopy condition.

Formula:

NDRE = (NIR − Red Edge) / (NIR + Red Edge)

Sentinel-2 bands:

Red Edge = B5
NIR = B8
4. 🟠 SAVI — Soil Adjusted Vegetation Index

Used to reduce the influence of exposed soil on vegetation-index values.

Formula:

SAVI = ((NIR − Red) / (NIR + Red + 0.5)) × 1.5

where L = 0.5 is the soil-adjustment factor.

📈 Seasonal Results

The seasonal mean values of NDVI, GNDVI, NDRE, and SAVI were compared across winter, pre-monsoon, monsoon, and post-monsoon.

The vegetation indices generally increased during the monsoon period and decreased after the monsoon, indicating stronger vegetation response during the main rainy/growing period.

📊 Figure 1 — Seasonal Vegetation Indices
<p align="center"> <img src="https://raw.githubusercontent.com/NishaKarki-Tech/seasonal-vegetation-dynamics-sentinel2/main/Figures/Figure1_Seasonal_Vegetation_Indices.png" alt="Seasonal Vegetation Indices" width="900"> </p>

Figure 1. Seasonal variation in NDVI, GNDVI, NDRE, and SAVI during 2025.

🔗 Correlation Among Vegetation Indices

Correlation analysis was used to examine how strongly the four vegetation indices were related to each other in the seasonal dataset.

The indices showed very strong positive relationships within this dataset.

📊 Figure 2 — Correlation Heatmap
<p align="center"> <img src="https://raw.githubusercontent.com/NishaKarki-Tech/seasonal-vegetation-dynamics-sentinel2/main/Figures/Figure3_Correlation_Heatmap.png" alt="Correlation Heatmap" width="900"> </p>

Figure 2. Correlation among NDVI, GNDVI, NDRE, and SAVI.

🔑 Key Findings
🌱 Four vegetation indices captured seasonal variation in vegetation response.
🌧️ Vegetation-index values were generally highest during the monsoon period.
📊 NDVI, GNDVI, NDRE, and SAVI showed very strong positive relationships in the seasonal dataset.
🛰️ Sentinel-2 provided suitable data for seasonal vegetation monitoring.
💻 The workflow integrated Google Earth Engine, Python, and ArcGIS Pro.
💻 Google Earth Engine

The Sentinel-2 processing and vegetation-index workflow was developed in Google Earth Engine.

The script includes:

✅ Sentinel-2 image filtering
✅ SCL-based pixel masking
✅ Seasonal median compositing
✅ NDVI calculation
✅ GNDVI calculation
✅ NDRE calculation
✅ SAVI calculation
✅ Seasonal statistics
✅ Data export

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
🚀 Future Improvements
🌾 Apply an agricultural/crop-land mask for crop-specific analysis.
📍 Validate satellite-derived vegetation patterns with field observations.
🚁 Integrate UAV imagery for higher-resolution validation.
📅 Extend the analysis to multiple years.
🌦️ Integrate weather and environmental data.
🤖 Explore machine-learning approaches for crop monitoring.
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
