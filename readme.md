# Temperature Analysis - NOAA Dataset

## Project Overview
This project analyzes temperature data from the NOAA dataset for the region near Ann Arbor, Michigan. It focuses on visualizing historical high and low temperatures from 2005-2014 and identifying record-breaking temperatures in 2015. Additionally, a map of station locations is provided.

## Dataset Description
The dataset consists of two CSV files:
1. **temperature.csv**: Contains temperature records with the following fields:
   - `id`: Station identification code
   - `Date`: Date in YYYY-MM-DD format
   - `Element`: Type of temperature measurement (`TMAX` for max temp, `TMIN` for min temp)
   - `Data_Value`: Temperature in tenths of degrees Celsius

2. **BinSize.csv**: Contains station location data with:
   - `LATITUDE`: Latitude of the station
   - `LONGITUDE`: Longitude of the station

## Requirements
Ensure the following Python libraries are installed before running the code:
```bash
pip install pandas matplotlib folium
```

## Implementation Steps
1. Load the dataset and preprocess the data:
   - Convert `Date` to datetime format.
   - Remove leap days (Feb 29).
   - Split data into two periods: 2005-2014 and 2015.
   - Extract `DayOfYear` for easier aggregation.

2. Compute temperature records:
   - Identify the record high and low temperatures for each day from 2005-2014.
   - Find record-breaking highs and lows in 2015.

3. Visualize the results:
   - A line graph with a shaded area between record highs and lows.
   - Scatter plot overlay for 2015 records that broke past extremes.

4. Map weather stations:
   - Use `folium` to plot station locations on an interactive map.

## Running the Code
- Open Jupyter Notebook:
- Open the provided .ipynb file and run each cell sequentially.

## Results & Observations
- The plot shows temperature variations over time, highlighting record-breaking 2015 temperatures.
- The station map provides geographic context for the data sources.

## Notes
- The dataset contains temperatures in tenths of degrees Celsius; conversion may be needed for interpretation.
- Leap days are removed to ensure consistency in year-over-year comparisons.

## Future Improvements
- Enhance visualization with interactive plots (e.g., using Plotly or Bokeh).
- Include additional weather elements like precipitation or wind speed.
- Expand the dataset for a broader geographical area.

## Author
Developed as part of a data analysis assignment using NOAA climate data.

