# GeoAI Solar Potential: Automated Infrastructure Analysis

## 🌍 Project Objective
This project demonstrates an automated Geospatial AI (GeoAI) framework designed to accelerate renewable energy tracking. The pipeline simulates high-resolution imagery, isolates rooftop infrastructure layouts using Meta's **Segment Anything Model (SAM)** implementation (`samgeo`), and performs vector spatial engineering to calculate clean energy output metrics.

## 🛠️ Tech Stack & Architecture
- **Environment:** Python 3, Google Colab (T4 GPU Engine)
- **Deep Learning Framework:** `samgeo` (Vision Transformer Architecture)
- **Spatial Engineering:** `GeoPandas`, `Rasterio`, `Shapely`
- **Visualization:** `leafmap` with integrated Google Satellite API engines

## 📊 Analytical Workflow & Data Logic
1. **Local Scene Synthesis:** Created a georeferenced metric multi-band raster layout initialized under the Austrian coordinate framework.
2. **AI Segmentation Execution:** Scaled an absolute edge-detection model (`vit_b` backbone) to generate crisp spatial extraction masks.
3. **Vector Topology Conversion:** Programmatically transformed raw pixel segments into standard GIS polygon geometry vector tables.
4. **Geospatial Projections:** Projected coordinates into **EPSG:31287 (MGI / Austria Lambert)** to preserve geometric true-area integrity.
5. **Applied Engineering Metric Formula:**
   \[\text{Annual Energy Potential (MWh)} = \frac{\text{Area }(m^2) \times 1200 \text{ kWh/m}^2 \times 0.20 \text{ Efficiency}}{1000}\]
