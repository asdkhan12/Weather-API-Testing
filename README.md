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

