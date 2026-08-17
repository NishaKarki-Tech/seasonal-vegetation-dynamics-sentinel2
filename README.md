🌿 Seasonal Vegetation Dynamics Using Sentinel-2 Remote Sensing
Multi-Index Assessment of Seasonal Vegetation Dynamics in Changunarayan Municipality, Nepal — 2025

Author: Nisha Karki
Year: 2026

📌 Project Overview

This project analyzes seasonal vegetation dynamics in Changunarayan Municipality, Bhaktapur, Nepal, using Sentinel-2 multispectral satellite imagery.

Four vegetation indices were calculated:

NDVI — overall vegetation vigor
GNDVI — chlorophyll/canopy response
NDRE — chlorophyll and vegetation condition
SAVI — vegetation response with reduced soil influence

The indices were calculated for four seasons of 2025 to compare how vegetation response changed throughout the year.

🛠️ Main Tools
Tool	Purpose
Google Earth Engine	Satellite-image processing, SCL masking, seasonal composites, index calculation
Python / Google Colab	Data analysis, correlation analysis, visualization
ArcGIS Pro	Spatial visualization and map preparation
GitHub	Code, data, figures, documentation
🎯 Objectives
Analyze seasonal vegetation dynamics using Sentinel-2 imagery.
Calculate NDVI, GNDVI, NDRE, and SAVI.
Compare vegetation-index responses across four seasons.
📍 Study Area

Changunarayan Municipality, Bhaktapur, Nepal

The study area contains a mixed landscape of agricultural and other land-cover types. The analysis focuses on how vegetation response changes across the municipality throughout the year.

🛰️ Data
Sentinel-2 MSI Surface Reflectance
Parameter	Details
Satellite	Sentinel-2
Sensor	MultiSpectral Instrument (MSI)
Dataset	COPERNICUS/S2_SR_HARMONIZED
Study year	2025
Spatial resolution	10–20 m depending on band
Processing platform	Google Earth Engine
Study boundary	Changunarayan Municipality
🔬 Methodology
Overall Workflow

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
Correlation analysis & visualization

1️⃣ Image Collection

Sentinel-2 Surface Reflectance Harmonized imagery was filtered to:

Changunarayan Municipality
January–December 2025
2️⃣ ☁️ Cloud Masking

Cloud masking was performed using the Sentinel-2 Scene Classification Layer (SCL).

The analysis retained pixels classified as:

🌱 Vegetation
🟤 Bare soil
💧 Water

Unwanted classes, including clouds and cloud shadows, were masked before creating the seasonal composites.

Why? Clouds and their shadows can interfere with surface reflectance and produce unreliable vegetation-index values.

3️⃣ 📅 Seasonal Compositing

The year was divided into four seasons:

Season	Period
❄️ Winter	January–February
🌱 Pre-monsoon	March–May
🌧️ Monsoon	June–September
🍂 Post-monsoon	October–December

A median composite was generated for each season.

This gives one representative image for each season instead of analyzing every individual satellite image separately.

🌿 4️⃣ Vegetation Indices
🟢 NDVI — Normalized Difference Vegetation Index

Measures overall vegetation vigor.

Formula:

NDVI = (NIR − Red) / (NIR + Red)

Sentinel-2 bands:

Red → B4
NIR → B8
🟩 GNDVI — Green Normalized Difference Vegetation Index

Uses the green band and provides sensitivity to chlorophyll and canopy condition.

Formula:

GNDVI = (NIR − Green) / (NIR + Green)

Bands:

Green → B3
NIR → B8
🔵 NDRE — Normalized Difference Red Edge Index

Uses the red-edge region and is useful for detecting changes in vegetation chlorophyll and canopy condition.

Formula:

NDRE = (NIR − Red Edge) / (NIR + Red Edge)

Bands used:

Red Edge → B5
NIR → B8
🟠 SAVI — Soil Adjusted Vegetation Index

Designed to reduce the influence of exposed soil on vegetation-index values.

Formula:

SAVI = ((NIR − Red) / (NIR + Red + L)) × (1 + L)

where L = 0.5.

📈 Seasonal Results

The seasonal mean values of NDVI, GNDVI, NDRE, and SAVI were compared across the four seasons.

Overall, the vegetation indices showed a clear seasonal pattern:

Values were generally lower during winter.
Vegetation response increased during pre-monsoon.
Values were generally highest during monsoon.
Values decreased again during post-monsoon.

This indicates stronger vegetation activity during the main rainy/growing period.

📊 Figure 1 — Seasonal Vegetation Indices

Figure 1. Seasonal variation in NDVI, GNDVI, NDRE, and SAVI during 2025.

🔗 Correlation Among Vegetation Indices

The correlation analysis was used to examine whether the four vegetation indices showed similar seasonal patterns.

The indices showed very strong positive correlations within this seasonal dataset.

Because the correlation analysis is based on four seasonal observations, these correlations should be interpreted as describing the pattern in this dataset rather than as a broad statistical validation.

📊 Figure 2 — Correlation Among Vegetation Indices

Figure 2. Correlation among the four vegetation indices.

🔬 Key Findings
🌱 1. Clear Seasonal Variation

All four vegetation indices showed seasonal changes in vegetation response.

🌧️ 2. Highest Vegetation Response During Monsoon

The indices generally reached their highest values during the monsoon season.

📊 3. Similar Seasonal Patterns

NDVI, GNDVI, NDRE, and SAVI followed similar overall seasonal trends.

🛰️ 4. Sentinel-2 Was Effective for Seasonal Monitoring

The project demonstrated how Sentinel-2 imagery can be used to monitor vegetation dynamics over a relatively small agricultural landscape.

💻 Google Earth Engine

The complete Sentinel-2 processing workflow was developed in Google Earth Engine.

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

📄 GEE script: GEE/vegetation_analysis.js

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

Other files from earlier exploratory analysis may remain in the repository but are not part of the main seasonal vegetation analysis presented here.

🚀 Future Improvements
🌾 Apply an agricultural/crop-land mask for crop-specific analysis.
📍 Validate satellite-derived vegetation patterns using field observations.
🚁 Integrate UAV imagery for higher-resolution validation.
📅 Extend the analysis to multiple years.
🌦️ Integrate weather and environmental data.
🤖 Explore machine-learning approaches for crop monitoring.
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
