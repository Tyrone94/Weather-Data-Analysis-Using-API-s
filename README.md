## South African Cities Weather Data Analysis
This Python project fetches, processes, and visualizes weather data for major South African cities using the Open-Meteo API. It demonstrates how to retrieve multiple weather parameters, handle API requests efficiently with caching and retries, and create clear visualizations for temperature, wind speed, and sunshine duration.

## Features
Fetches daily and current weather data for Cape Town, Johannesburg, Durban, and Pretoria.

Implements caching to reduce redundant API calls (cache expires after 1 hour).

Uses retry logic to automatically handle failed API requests with retries and exponential backoff.

Extracts key weather metrics including minimum, maximum, and current temperature, wind speed, precipitation, and sunshine duration.

Prints detailed location info and weather data in a readable format for each city.

Generates bar charts and line plots to compare weather parameters across cities.

## Technologies Used
Python 3.x

openmeteo_requests (Open-Meteo API client)

requests_cache (for caching API responses)

retry_requests (for retrying failed requests)

pandas and numpy (for data processing)

matplotlib (for plotting visualizations)

## Installation
Clone this repository:

git clone https://github.com/yourusername/sa-weather-analysis.git
cd sa-weather-analysis

(Optional) Create and activate a virtual environment:

## For Linux/macOS:
python -m venv env
source env/bin/activate

## For Windows:
python -m venv env
.\env\Scripts\activate

## Install dependencies:

pip install -r requirements.txt

Usage
Run the main Python script:

python weather_analysis.py

The script will:

Print detailed location information (latitude, longitude, elevation, timezone) for each city.

Display current weather conditions like temperature, precipitation, rain, snowfall, and pressure.

Show daily weather data including min/max temperature, wind speed, precipitation, and sunshine duration.

Generate visual plots comparing min/max temperatures, current temperatures, max wind speeds, and sunshine duration across the cities.

## Project Structure
weather_analysis.py — The main script that fetches, processes, and visualizes weather data.

requirements.txt — Lists all required Python libraries for easy setup.

## API Details
The project uses the Open-Meteo API, which offers free global weather data with a variety of forecast models and parameters.

## Important Notes
API responses are cached locally for 1 hour to optimize performance and reduce the number of requests.

Failed API requests are retried up to 5 times with exponential backoff to handle intermittent network or server issues.

The script fetches weather data for the past 7 days to provide comprehensive historical insights.

Potential Enhancements
Add support for more cities or user-defined locations.

Include hourly weather data visualizations for more granular analysis.

Develop an interactive web dashboard for live weather data exploration.

## Author
Anele Khanyile
