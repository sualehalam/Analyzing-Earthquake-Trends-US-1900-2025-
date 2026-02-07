# Analyzing Earthquake Trends in the US (1900–2025)
<img width="800" height="603" alt="image" src="https://github.com/user-attachments/assets/0db4ed12-ad50-45f4-be88-2f36c552c1c8" />

## Project Overview
This repository contains the final project for **STAT 651 (Data Visualization)**, completed as part of my Master’s program in Statistics. The project demonstrates an end-to-end statistical workflow in **R**, including data cleaning, exploratory data analysis (EDA), geospatial visualization, and interpretation of real-world earthquake data.

The objective of this project is to analyze long-term **temporal and spatial patterns** in U.S. earthquake activity and identify regions and conditions associated with higher seismic risk.


### Common Earthquake Terminology:  
**Seismicity:** The frequency of earthquakes in a region.

**Aftershocks:** A smaller earthquake following the main shock of a large earthquake.

**Fault:** It is a fracture in the Earth's crust where rocks slide past each other. 

**Magnitude:** A measure of the energy released, often on the Richter Scale (now often Moment Magnitude, Mw).

**Induced seismicity:** It refers to earthquakes caused by human activities that alter stress on the Earth’s crust, such as mining, which can increase pressure on existing faults, triggering seismic events.

**Subduction Zones:** They are areas where one tectonic plate dives under another, creating Earth’s most powerful earthquakes, tsunamis, and volcanoes

**Ring of Fire:** Pacific Ring of Fire is a horseshoe-shaped zone around the Pacific Ocean known for intense earthquakes and volcanic activity.

## Data Description

**Source:** U.S. Geological Survey (USGS)  https://earthquake.usgs.gov/earthquakes/search/

**Geographic Scope:** Conterminous United States

**Time Range:** 1900–2025

**Observations:** 3,439 earthquakes

**Inclusion Criteria:** Magnitude ≥ 4.5

## Key Variables Used:

* Event Time (date-time)
* Latitude 
* Longitude
* Depth (km)
* Magnitude
* Location (place)
* Event type

## Libraries Used:

This project requires R (RStudio environment) and the following R libraries installed:

1. `tidyverse`  
2. `leaflet`  
3. `ggplot2`  
4. `lubridate`  
5. `tidyverse`  
6. `lubridate`  
7. `tidygeocoder`  
8. `plotly`  
9. `hexbin`  
10. `viridis`
11. `scales`
12. `maps`

## Analytical Workflow
This project follows a structured, data analysis pipeline:

1. **Data Loading**
   - Imported raw USGS CSV data into R
2. **Data Cleaning**
   - Removed irrelevant columns
   - Filtered events by magnitude threshold
3. **Feature Engineering**
   - Extracted year, decade, month, weekday, and hour
4. **Exploratory Data Analysis (EDA)**
   - Temporal trends and frequency analysis
5. **Geospatial Visualization**
   - Static and interactive U.S. maps animation
6. **Clustering & Extreme Event Analysis**
   - Identification of top 10 strongest earthquakes
7. **Interpretation & Reporting**
   - Linking patterns to tectonic and human-induced causes

## 📈 Key Research Questions & Findings

1. How has earthquake frequency changed from the 1990s to the 2020s?
2. How has the spatial distribution of moderate earthquakes (M >=4.5) evolved across the U.S.?
3. Which regions produce the most powerful earthquakes?
4. Top 10 Most Powerful Earthquakes (Cluster Analysis)
5. How does the earthquake activity vary by month across over the past decades?
6. Which month has had the highest earthquakes on average and are certain months or seasons more seismically active?
7. Which day of the week earthquakes are most likely to occur ?
8. Which time of the day earthquakes are most common on average?

## Conclusions

- Earthquake activity is **heavily concentrated in western U.S. coastal regions**, especially _California_ and _Mexico_
- Large-magnitude earthquakes _(M ≥ 7)_ are strongly associated with **tectonic plate boundaries**
- A noticeable increase in earthquakes during **2009–2016** aligns with induced seismicity (human activities impacting seismicity) in _Oklahoma_
- Earthquake Activity declined after **2016**, following strict regulatory changes
- While temporal patterns exist, but earthquakes can occur at any time, reinforcing the need for continuous preparedness


## Authors
 [![](https://img.shields.io/badge/LinkedIn-%40Sualeh%20Alam-lightgrey?colorA=abcdef&logo=data:image/jpeg;base64,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)](https://www.linkedin.com/in/sualeh-alam/)
