# NDVI_project
# NDVI Analysis of Gaindakot Using Sentinel-2

## Overview
This project calculates the Normalized Difference Vegetation Index (NDVI) for the Gaindakot region using Sentinel-2 SR Harmonized imagery. NDVI is a widely used indicator for assessing vegetation health and cover.

The analysis includes:
- Filtering Sentinel-2 imagery by date and study area
- Calculating NDVI for each image
- Computing mean NDVI over the study period
- Visualizing NDVI on a map with a legend

---

## Data Sources
- Sentinel-2 Surface Reflectance Harmonized  
  Collection ID: `COPERNICUS/S2_SR_HARMONIZED`  
  Period: `2022-10-01` to `2022-11-30`  

- Study Area Boundary 
  The boundary is provided as a FeatureCollection named `table` in Google Earth Engine.

---

## Methodology

1. Load and Filter Images  
   Sentinel-2 images are filtered by date and the study area.

2. NDVI Calculation 
   NDVI is computed using the formula:  
   \[
   NDVI = \frac{NIR - RED}{NIR + RED}
   \]  
   where:
   - `NIR` = Band 8 (Near Infrared)
   - `RED` = Band 4 (Red)

3. Compute Mean NDVI 
   NDVI images are averaged to obtain a mean NDVI map for the study period.

4. Visualization
   - NDVI values are visualized using a color palette:
     - Blue: Water / No vegetation
     - Red: Bare soil / Built-up
     - Yellow: Low vegetation
     - Green: Healthy vegetation
   - A legend is added to the map for reference.

---

## How to Run

1. Open **[Google Earth Engine Code Editor](https://code.earthengine.google.com/)**.
2. Create a new script and add the `NDVI` JavaScript code.
3. Make sure the `table` variable is set to your study area FeatureCollection.
4. Run the script. You will see:
   - Individual NDVI images
   - Mean NDVI map
   - NDVI legend

---

## Outputs

- NDVI Collection:All NDVI images for the selected period
- Mean NDVI Map: Clipped to Gaindakot boundary
- NDVI Legend: Color-coded vegetation classes

---

## Notes

- Adjust the date range or visualization parameters as needed for different seasons.

---

