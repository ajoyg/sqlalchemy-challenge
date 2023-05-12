# SQLAlchemy Challenge
Analyze the weather in Hawaii to help plan for a vacation. Module 10 SQLAlchemy challenge in the UCB bootcamp.

## Part 1
In this section the Jupyter notebook climate.ipynb in the SurfsUp folder has the basic climate analysis and data exploration of the climate database hawaii.sqlite in the Resources folder. The climate.ipynb code connects with the sqlite database using SQLAlchemy, reflects the tables into classes and performs the following precipitation analysis:
* Get the most recent date in the dataset.
* Using that date, get the previous 12 months of precipitation data by querying the previous 12 months of data.
* Select the date and precipitation values, sort them by date and plot the data.
* Get the total number of weather stations and the most active eather station
* Calculate the lowest, highest, and average temperatures for the active station
* Plot the previous 12 months of temperature for the most active station.

## Part 2
This section creates a Flask API based on the queries built in Part 1.
The file app.py in the SurfsUp has the following api routes:
* / (Homepage) - Returns a list of all available apis on the home page
* /api/v1.0/precipitation - Returns the last 12 months of precipitation data in a json format (date:precipitation)
* /api/v1.0/stations - Returns a json list of stations in a json format (station id)
* /api/v1.0/tobs - Returns a json list of temperature observations for a 12 month period for the most active station (date, temperature)
* /api/v1.0/<start_date> - Returns a json list of minimum, average, and maximum temperatures for all dates greater than or equal to the start date.
*  /api/v1.0/<start_date>/<end_date> - Returns a json list of minimum, average, and maximum temperatures for all dates from the start date to the end date, inclusive.
