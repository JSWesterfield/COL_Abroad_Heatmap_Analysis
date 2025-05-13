# Cost of Living Abroad Heatmap Analysis

This repository contains a Python script (`cost_of_living_heatmap.py`) that scrapes cost of living data for major Turkish cities from Numbeo, visualizes this data on a map of Turkey, and generates a heatmap representing the cost of living index across the region.

## Overview

The script performs the following steps:

1.  **Scrapes Data:** Fetches the cost of living rankings for the current year from Numbeo ([https://www.numbeo.com/cost-of-living/rankings.jsp](https://www.numbeo.com/cost-of-living/rankings.jsp)).
2.  **Extracts City Data:** Parses the HTML to extract the Cost of Living Index for a predefined list of major Turkish cities.
3.  **Geocoding:** Uses a hardcoded dictionary to associate these cities with their approximate latitudes and longitudes.git 
4.  **Data Structuring:** Creates a Pandas DataFrame to organize the city names, coordinates, and cost of living indices.
5.  **Heatmap Visualization:**
    * Uses the `cartopy` library to create a map of Turkey.
    * Employs `scipy.interpolate.griddata` to interpolate the cost of living data from the discrete cities onto a regular grid.
    * Generates a heatmap using `matplotlib` to display the interpolated cost of living index across the map.
    * Overlays city markers and annotations for geographical context.
    * Includes a colorbar to understand the cost of living scale.

## Files

* `cost_of_living_heatmap.py`: The main Python script containing the web scraping, data processing, and visualization logic.
* `README.md`: This file, providing an overview and instructions for the repository.

## Prerequisites

Before running the script, ensure you have the following Python libraries installed:

```bash
pip install requests beautifulsoup4 pandas geopandas matplotlib seaborn python-dotenv