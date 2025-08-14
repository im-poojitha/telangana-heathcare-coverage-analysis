# Mapping Health Infrastructure Gaps in Telangana Using Geospatial Analysis

## Overview
This project uses *geospatial analysis* to identify healthcare coverage gaps across Telangana, India.  
By combining *open government datasets* with *H3 hexagonal spatial indexing* and *interactive mapping*, we can pinpoint underserved regions and provide a data-driven framework for better healthcare planning.

---

## Features
- *H3 Hexagonal Spatial Indexing* at resolution 7 (~0.74 km² per hexagon)
- *Population mapping* using WorldPop gridded data
- *Healthcare facility geolocation mapping*
- *Interactive Folium Map* with:
  - Green hexagons: Areas with at least one healthcare centre
  - Clickable popups showing:
    - Population in the hexagon
    - Number of health centres
    - Area covered (km²)
    - H3 index for spatial analysis

---

## Data Sources
- *Telangana Health Facility Geolocations* — [State Government Open Data TGDex](https://tgdex.telangana.gov.in/data-bank/details?id=67aadd1c-5249-4387-8ed0-b35eaee34e46) 
- *WorldPop Gridded Population Data* — [WorldPop Hub](https://https://hub.worldpop.org/www.worldpop.org)

---

## Methodology
1. *Data Cleaning & Preparation*  
   - Extracted and cleaned healthcare facility coordinates  
   - Loaded high-resolution population grids  

2. *Spatial Indexing with H3*  
   - Converted geographic coordinates into H3 hexagons at resolution 7  
   - Mapped population counts and facility counts per hexagon  

3. *Interactive Mapping*  
   - Used *Folium* to create a color-coded map   
   - Added popups for detailed insights  

4. *Analysis*  
   - Calculated total covered vs uncovered area and population  
   - Identified regions for priority intervention  

---

## Key Findings
- Only *21% of Telangana’s land area* falls within a covered healthcare hexagon  
- Nearly *half the population* lives in those covered areas  
- Around *20 million rural residents* remain outside effective coverage  
- *91,000 km²* of the state has no nearby healthcare facilities  

---

## Why This Matters
Healthcare gaps lead to:
- Delayed emergency medical response
- Reduced disease surveillance & vaccination efficiency
- Poor maternal & child health outcomes in remote areas

---

## Tech Stack
- *Python* (Pandas, Geopandas, Folium, h3-py)
- *H3 Spatial Indexing*
- *Jupyter Notebook*
- *Open Data Sources*

---

## How to Run
```bash
# Clone repository
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>

# Install dependencies
pip install -r requirements.txt

# Run analysis
jupyter notebook analysis.ipynb
