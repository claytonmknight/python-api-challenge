# python-api-challenge
# WeatherPy and VacationPy Analysis

This repository contains Python scripts for analyzing weather data and finding ideal vacation spots using data obtained from the OpenWeatherMap API and the Geoapify API, respectively.

## WeatherPy

### Overview

The WeatherPy script generates scatter plots and performs linear regression analysis to explore the relationship between weather variables and latitude. It fetches weather data for various cities from the OpenWeatherMap API and visualizes the data using Matplotlib.

### Usage

1. Clone this repository to your local machine.
2. Ensure you have Python installed along with the required dependencies listed in `requirements.txt`.
3. Replace the placeholder in `api_keys.py` with your actual OpenWeatherMap API key.
4. Run the `WeatherPy.ipynb` or `WeatherPy.py` script to generate scatter plots and analyze weather data.

### Analysis

The script analyzes the following relationships:

- Temperature vs. Latitude: The closer to the equator, the warmer the temperature.
- Humidity vs. Latitude: Relative humidity tends to be higher nearer the equator.
- Cloudiness vs. Latitude: Proximity to the equator does not necessarily mean it will be cloudier.
- Wind Speed vs. Latitude: Proximity to the equator does not seem to equate to higher wind speed.

### Assistance

- AskBCS assisted with parsing out latitude, longitude, max temp, humidity, cloudiness, wind speed, country, and date.
- Time format assistance for incorporating other graph properties was found on [Tutorialspoint](https://www.tutorialspoint.com/python/time_strftime.htm).
- Linear regression assistance was obtained from [AdamSmith.haus](https://www.adamsmith.haus/python/examples/658/scipy-compute-a-linear-regression-line).

## VacationPy

### Overview

The VacationPy script creates a map displaying cities from the WeatherPy analysis and finds ideal vacation spots based on specified weather conditions. It uses the Geoapify API to search for hotels near selected cities and plots the results on a map.

### Usage

1. Ensure you have the required dependencies installed, including `hvplot` and `pandas`.
2. Replace the placeholder in `api_keys.py` with your actual Geoapify API key.
3. Run the `VacationPy.ipynb` or `VacationPy.py` script to generate a map displaying vacation spots and nearby hotels.

### Analysis

The script narrows down cities based on specific weather criteria, such as temperature range, wind speed, and cloudiness. It then searches for nearby hotels using the Geoapify API and displays the results on a map, providing additional information such as the hotel name and country in the hover message.

### Assistance

The instructor assisted with Step 4, which involved using the Geoapify API to find the first hotel located within 10,000 meters of each city's coordinates.
