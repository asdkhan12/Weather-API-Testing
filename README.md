# Weather-API-Testing
This project fetches current weather data for a set of major world cities using the OpenWeatherMap API, stores the results in a local SQLite database, and then uses pandas and Matplotlib to analyze and visualize temperature and wind patterns. It highlights the cities with the highest and lowest temperatures, examines wind-speed trends. 


# Weather API Analysis

This repository contains a Jupyter Notebook that demonstrates how to fetch, store, analyze, and visualize current weather data for a collection of major world cities using the OpenWeatherMap API.

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Prerequisites](#prerequisites)  
3. [Installation](#installation)  
4. [Configuration](#configuration)  
5. [Usage](#usage)  
   - [Fetching and Storing Data](#fetching-and-storing-data)  
   - [Data Analysis & Visualization](#data-analysis--visualization)  
6. [Results](#results)  
7. [Extending This Project](#extending-this-project)  
8. [License](#license)

---

## Project Overview

This notebook performs the following steps:

1. Sets up required libraries (`pandas`, `requests`, `sqlite3`, `pyowm`, `matplotlib`).  
2. Defines a list of 25 global cities (e.g., New York, London, Tokyo, Cairo).  
3. Tests a sample API call for Tokyo to verify connectivity.  
4. Creates a local SQLite database and table to store raw JSON responses for each city’s weather.  
5. Iterates over each city:
   - Sends an HTTP request to OpenWeatherMap.
   - Inserts the returned JSON into SQLite.
6. Reads the stored data into a pandas DataFrame.  
7. Converts temperatures from Kelvin to Fahrenheit and calculates additional metrics as needed.  
8. Uses pandas and Matplotlib to:
   - Identify and plot the five hottest and five coldest cities.  
   - Aggregate average wind speeds by weather status and plot the results.  
   - Determine which city currently has the most favorable weather.  
9. Summarizes key insights about temperature, wind speed, and overall comfort.

## Prerequisites

- Python 3.8+  
- A valid [OpenWeatherMap API key](https://openweathermap.org/api)  
- Jupyter environment (Notebook or JupyterLab)  

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/weather-api-analysis.git
   cd weather-api-analysis

python3 -m venv venv
source venv/bin/activate   # on Windows: venv\Scripts\activate


pip install pandas requests matplotlib pyowm sqlite3


api_key = "YOUR_OPENWEATHERMAP_API_KEY"


## Usage

### Fetching and Storing Data
- Run the first code cell to install any missing packages and import libraries.
- Ensure that Step 0 (API setup) and Step 1 (database creation) execute without errors.
- In Step 2, verify that the test request for Tokyo returns a valid response.
- Run the cell that defines the list of cities and loops through each, fetching weather data and inserting it into the SQLite database.

### Data Analysis & Visualization
- Execute the cell that reads from SQLite into a pandas DataFrame.
- Run the cells that:
  - Convert temperature units from Kelvin to Fahrenheit.
  - Compute top 5 hottest and coldest cities and plot bar charts.
  - Aggregate average wind speed by weather status and plot another chart.
  - Identify the most favorable weather city and summarize observations.
- Inspect the generated charts and summary to draw insights.

## Results
- **Hottest Cities**: Displays the five cities currently experiencing the highest temperatures, with bar chart visualization.
- **Coldest Cities**: Displays the five cities with the lowest temperatures.
- **Wind Speed by Weather**: Bar chart showing how average wind speed varies across different weather conditions (for example, clear, broken clouds, rain).
- **Most Favorable Weather**: Identifies the single city (for example, Los Angeles, US) that offers the most comfortable combination of temperature, weather status, and wind speed at runtime.

![Example: Average Wind Speed by Weather Status]

![download](https://github.com/user-attachments/assets/6a7f7891-e15a-43eb-869f-6d1b1d67d3c8)

![download (1)](https://github.com/user-attachments/assets/0f3953ea-efd6-437d-a174-145e6851ca81)





## Extending This Project
- **Additional Metrics**: Compute humidity or “feels like” temperature comparisons.
- **Time Series Analysis**: Schedule this notebook to run daily (for example, via cron or GitHub Actions), store historical data, and visualize trends over time.
- **Geospatial Mapping**: Use libraries like folium or plotly to map cities colored by temperature or wind speed.
- **User Input**: Allow interactive selection of cities or date-range filters via Jupyter widgets.



