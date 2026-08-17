# 🌿 Seasonal Vegetation Dynamics Using Sentinel-2 Remote Sensing

## Multi-Index Assessment of Seasonal Vegetation Dynamics in Changunarayan Municipality, Nepal (2025)

**Author:** Nisha Karki  
**Year:** 2026

---

## 📌 Project Overview

This project analyzes **seasonal vegetation dynamics** in **Changunarayan Municipality, Bhaktapur, Nepal** using **Sentinel-2 multispectral satellite imagery**.

Four vegetation indices were calculated for four seasons of 2025:

- **NDVI** — general vegetation vigor
- **GNDVI** — chlorophyll and canopy response
- **NDRE** — chlorophyll and vegetation condition
- **SAVI** — vegetation response with reduced soil influence

The analysis compares how vegetation response changed throughout the year.

The workflow used:

- **Google Earth Engine** for satellite-image processing
- **Python / Google Colab** for data analysis and visualization
- **ArcGIS Pro** for spatial mapping
- **GitHub** for code and project documentation

---

## 🎯 Objectives

- Analyze **seasonal vegetation dynamics** using Sentinel-2 imagery.
- Calculate **NDVI, GNDVI, NDRE, and SAVI**.
- Compare vegetation-index responses across **four seasons**.
- Examine the relationships among the vegetation indices.
- Visualize seasonal vegetation patterns using **Python and GIS**.

---

## 📍 Study Area

**Changunarayan Municipality, Bhaktapur, Nepal**

The study area contains a mixed landscape including **agricultural areas and other land-cover types**.

The project focuses on understanding how vegetation response varies across the municipality throughout the year.

---

## 🛰️ Satellite Data

### Sentinel-2 MSI Surface Reflectance

- **Satellite:** Sentinel-2
- **Sensor:** MultiSpectral Instrument (MSI)
- **Dataset:** `COPERNICUS/S2_SR_HARMONIZED`
- **Study year:** 2025
- **Spatial resolution:** 10 m for the main bands used in this analysis
- **Platform:** Google Earth Engine

A **Changunarayan Municipality boundary** was used to define the study area.

---

## 🛠️ Tools and Their Uses

| Tool | Purpose |
|---|---|
| **Google Earth Engine** | Image filtering, cloud masking, seasonal compositing, and vegetation-index calculation |
| **Python / Google Colab** | Data analysis, correlation analysis, and visualization |
| **ArcGIS Pro** | Spatial visualization and map preparation |
| **GitHub** | Code, data, figures, and documentation |

---

# 🔬 Methodology

### Overall Workflow

**Sentinel-2 imagery**  
↓  
**Study-area filtering**  
↓  
**SCL-based pixel masking**  
↓  
**Seasonal median composites**  
↓  
**NDVI + GNDVI + NDRE + SAVI**  
↓  
**Seasonal comparison**  
↓  
**Correlation analysis and visualization**

---

## 1️⃣ Image Collection

Sentinel-2 Surface Reflectance Harmonized imagery was filtered to the **Changunarayan Municipality study area** for the year **2025**.

---

## 2️⃣ Cloud Masking

Cloud masking was performed using the **Sentinel-2 Scene Classification Layer (SCL)** in Google Earth Engine.

The SCL information was used to keep useful pixels such as:

- **Vegetation**
- **Bare soil**
- **Water**

Clouds, cloud shadows, and other unwanted classes were masked before creating the seasonal composites.

This step helps prevent clouds and their shadows from affecting the vegetation-index calculations.

---

## 3️⃣ Seasonal Compositing

The year 2025 was divided into four seasons:

| Season | Period |
|---|---|
| **Winter** | January–February 2025 |
| **Pre-monsoon** | March–May 2025 |
| **Monsoon** | June–September 2025 |
| **Post-monsoon** | October–December 2025 |

A **median composite** was generated for each season.

This provides one representative satellite image for each season while reducing the influence of individual cloudy or abnormal observations.

---

# 🌿 4️⃣ Vegetation Indices

## NDVI — Normalized Difference Vegetation Index

NDVI was used to assess **general vegetation vigor**.

### Formula

**NDVI = (NIR − Red) / (NIR + Red)**

### Sentinel-2 bands

- **Red = B4**
- **NIR = B8**

---

## GNDVI — Green Normalized Difference Vegetation Index

GNDVI uses the green band and provides information related to **vegetation chlorophyll and canopy condition**.

### Formula

**GNDVI = (NIR − Green) / (NIR + Green)**

### Sentinel-2 bands

- **Green = B3**
- **NIR = B8**

---

## NDRE — Normalized Difference Red Edge Index

NDRE uses a red-edge band and is useful for assessing **changes in vegetation chlorophyll and canopy condition**.

### Formula

**NDRE = (NIR − Red Edge) / (NIR + Red Edge)**

### Sentinel-2 bands

- **Red Edge = B5**
- **NIR = B8**

---

## SAVI — Soil Adjusted Vegetation Index

SAVI was used to reduce the influence of **exposed soil** on vegetation-index values.

### Formula

**SAVI = ((NIR − Red) / (NIR + Red + L)) × (1 + L)**

where:

**L = 0.5**

Therefore:

**SAVI = ((NIR − Red) / (NIR + Red + 0.5)) × 1.5**

---

# 📈 Seasonal Analysis

The four vegetation indices were compared across:

**Winter → Pre-monsoon → Monsoon → Post-monsoon**

The analysis showed that vegetation-index values generally **increased during the monsoon period** and decreased after the monsoon.

This indicates a stronger overall vegetation response during the main rainy/growing period.

---

# 📊 Results

## Figure 1 — Seasonal Vegetation Indices

![Seasonal Vegetation Indices](Figures/Figure1_Seasonal_Vegetation_Indices.png)

**Figure 1.** Seasonal variation in **NDVI, GNDVI, NDRE, and SAVI** during 2025.

The figure shows that all four indices followed a broadly similar seasonal pattern, with their values generally increasing during the monsoon period.

---

## Figure 2 — Correlation Among Vegetation Indices

![Correlation Among Vegetation Indices](Figures/Figure3_Correlation_Heatmap.png)

**Figure 2.** Correlation among the four vegetation indices.

The indices showed **very strong positive relationships** in the seasonal dataset, indicating that they generally followed similar seasonal patterns.

> **Note:** The correlation analysis is descriptive and is based on the seasonal observations.

---

# 🔬 Key Findings

- **Sentinel-2 imagery** successfully captured seasonal vegetation variation in Changunarayan Municipality.
- **NDVI, GNDVI, NDRE, and SAVI** all showed clear seasonal changes.
- Vegetation-index values were generally **highest during the monsoon period**.
- The four indices showed **very strong positive relationships** in the seasonal dataset.
- The project demonstrates how **Google Earth Engine, Python, and GIS** can be integrated for remote-sensing-based vegetation monitoring.

---

# 💻 Google Earth Engine

The Sentinel-2 processing and vegetation-index workflow was developed in **Google Earth Engine**.

The workflow includes:

- Sentinel-2 image filtering
- SCL-based pixel masking
- Seasonal median compositing
- NDVI calculation
- GNDVI calculation
- NDRE calculation
- SAVI calculation
- Seasonal statistics
- Data export

### GEE Script

`GEE/vegetation_analysis.js`

---

# 📂 Repository Structure

```text
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
