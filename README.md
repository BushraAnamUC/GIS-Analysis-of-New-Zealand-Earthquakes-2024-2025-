# GIS Analysis of New Zealand Earthquakes (2024)

## Table of Contents

- [Introduction](#introduction)
- [Dataset Information](#dataset-information)
- [Project Structure](#project-structure)
- [Installation and Setup](#installation-and-setup)
- [Data Preprocessing](#data-preprocessing)
- [Visualisation](#visualisation)
- [Statistical Analysis](#statistical-analysis)
- [Conclusion](#conclusion)

---

## Introduction

This project focuses on exploring earthquake patterns, magnitude distribution, spatial clustering, and temporal trends in New Zealand. By leveraging GIS tools and visualization libraries, we aim to provide insightful analyses of seismic activity.

## Dataset Information

- **Source 1:** Earthquake data from [geonet.nz](https://www.geonet.org.nz/)
- All files are available in CSV as well as GeoJSON formats. From GeoNet, we have used the CSV file.
- **Source 2:** Shapefiles for New Zealand regions from [state.nz](https://data.govt.nz/)
- Data type: Vector polygon layer (Multipolygon)
- CRS as stored: NZGD2000 / New Zealand Transverse Mercator 2000 (EPSG:2193)



### Key Columns in Dataset:

- `origintime`: Time of the earthquake event
- `latitude` and `longitude`: Geographic coordinates
- `magnitude`: Earthquake magnitude
- `depth`: Depth of the earthquake
- `eventtype`: Type of seismic event (filtered for earthquakes only)

## Project Structure

```
GIS-NZ-Earthquakes/
│
├── data/
│   ├── merged_earthquake_data.csv
│   └── shapefiles/
│
├── notebooks/
│   ├── data_preprocessing.ipynb
│   ├── visualisation.ipynb
│   └── statistical_analysis.ipynb
│
├── outputs/
│   ├── earthquake_map.html
│   ├── heatmap.html
│   └── graphs/
│
├── README.md
└── requirements.txt
```

## Installation and Setup

1. Clone this repository:
   ```bash
   git clone https://github.com/username/GIS-NZ-Earthquakes.git
   ```
2. Navigate to the project directory:
   ```bash
   cd GIS-NZ-Earthquakes
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## Data Preprocessing

The data preprocessing steps include:

- Loading data from CSV files.
- Filtering only earthquake events.
- Dropping rows with missing values.
- Converting `origintime` to datetime format.
- Aggregating average magnitude and depth by region.

**Code:** See `notebooks/data_preprocessing.ipynb`

## Visualisation

The project includes various visualisations:

1. **Interactive Map of Earthquakes:** Circle markers for earthquake locations with magnitudes represented by marker size.
2. **Heatmap:** Density of earthquakes across New Zealand.
3. **Spatial Distribution Scatterplot:** Geographic clustering of earthquake events.
4. **Magnitude vs Location:** Magnitude distribution by geographic region.
5. **Depth vs Magnitude:** Correlation between depth and magnitude.

**Code:** See `notebooks/visualisation.ipynb`



## Statistical Analysis

- Temporal trends in earthquake occurrences (monthly and weekday analysis).
- Comparison of earthquake frequencies between North and South Islands.
- Magnitude distribution.

**Code:** See `notebooks/statistical_analysis.ipynb`

## Conclusion

This project provides a detailed GIS-based analysis of earthquakes in New Zealand. The findings can support further research and disaster preparedness strategies.

---

**Acknowledgments:**
Special thanks to [GeoNet](https://www.geonet.org.nz/) for providing the earthquake data.

**License:**
This project is licensed under the MIT License. See the LICENSE file for details.

