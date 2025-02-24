Hawaii Weather Data Analysis & API

Overview

This project analyzes historical weather data from Hawaii and provides an interactive API for accessing this information. It leverages robust data processing and visualization tools alongside a RESTful web service to offer both insights and programmatic access to the data.

Key Components

1. Data Processing & Visualization

    Database Connection & Data Retrieval:
    Utilizes SQLAlchemy to connect to a SQLite database (hawaii.sqlite) containing historical weather measurements. The project reflects the database tables (e.g., Measurement and Station) and extracts relevant data.

    Data Analysis:
    Processes weather data with Pandas to compute summary statistics for precipitation and temperature, including measures such as minimum, maximum, and average values.
    
    Visualizations:

     **Precipitation Bar Chart:**
     Displays a year’s worth of precipitation data in a clear, color-coded bar chart.

     **Temperature Histogram:**
     Illustrates the distribution of temperature observations from the most active weather station (USC00519281) using a histogram.
   
3. RESTful API with Flask
      Web Application:
   
      Implements a Flask-based API to serve weather data in JSON format, allowing seamless integration with other applications.

       Key Endpoints Include:
          /api/v1.0/precipitation – Returns precipitation data for the last year.
          /api/v1.0/stations – Provides a list of all weather stations.
          /api/v1.0/tobs – Offers temperature observations for the most active station.
          /api/v1.0/stats/<start_date> and /api/v1.0/stats/<start_date>/<end_date> – Delivers summary statistics for temperature over specified date ranges.
