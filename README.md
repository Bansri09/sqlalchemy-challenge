# SQLAlchemy Challenge: Climate Analysis for Honolulu, Hawaii

## Overview

This challenge involves performing a climate analysis and data exploration for Honolulu, Hawaii using Python, SQLAlchemy, Pandas, and Matplotlib. Additionally, a Flask API is designed based on the queries developed during the analysis.

## Challenge Structure

### 1. Analyze and Explore the Climate Data

In this section, you will use Python and SQLAlchemy to perform a basic climate analysis and data exploration of the climate database.

1. **Setup**:
   - Use `SQLAlchemy create_engine()` to connect to your SQLite database.
   - Use `SQLAlchemy automap_base()` to reflect your tables into classes.
   - Save references to the classes named `station` and `measurement`.
   - Create a SQLAlchemy session to link Python to the database.
   - **Important**: Close your session at the end of your notebook.

2. **Precipitation Analysis**:
   - Find the most recent date in the dataset.
   - Get the previous 12 months of precipitation data.
   - Load the query results into a Pandas DataFrame and set column names.
   - Sort the DataFrame values by date.
   - Plot the results using the DataFrame plot method.
   - Print the summary statistics for the precipitation data.

  
<img width="468" alt="precipitation" src="https://github.com/user-attachments/assets/7648db8f-b065-406d-a0cf-2fcfccc4cb51" />

3. **Station Analysis**:
   - Design a query to calculate the total number of stations.
   - Find the most-active stations and list them in descending order by observation counts.
   - Identify the station ID with the greatest number of observations.
   - Design a query to calculate the lowest, highest, and average temperatures for the most-active station.
   - Get the previous 12 months of temperature observation (TOBS) data for the most-active station.
   - Plot the TOBS data as a histogram with bins=12.
   - Close your session.
   - 
<img width="478" alt="station-histogram" src="https://github.com/user-attachments/assets/e7be39fb-d6b9-4bad-afed-a80d3ce83e66" />

### 2. Design Your Climate App

Now that the initial analysis is complete, design a Flask API based on the queries developed.

1. **Flask Routes**:
   - `/`: Start at the homepage and list all available routes.
   - `/api/v1.0/precipitation`: Convert the last 12 months of precipitation data to a dictionary and return the JSON representation.
   - `/api/v1.0/stations`: Return a JSON list of stations from the dataset.
   - `/api/v1.0/tobs`: Return a JSON list of temperature observations for the previous year for the most-active station.
   - `/api/v1.0/<start>` and `/api/v1.0/<start>/<end>`: Return a JSON list of the minimum, average, and maximum temperature for a specified start or start-end range.


---


