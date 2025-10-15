# Weather-Forecast
1. Project Overview
This repository contains the Power BI dashboard file (weather forecast.pbix) for an interactive solution designed to visualize and analyze historical weather data and future forecasts.

The dashboard's primary goal is to provide a comprehensive, location-specific view of meteorological trends to support data-driven decision-making in areas sensitive to weather changes (e.g., logistics, energy, or retail).

Key Component	Description
Data Scope	Historical weather data and a 7-day forecast model.
Output	Interactive Power BI Report focusing on temperature, precipitation, and model accuracy.
Technology	Power BI Desktop (DAX & M Language).

Export to Sheets
2. Data Model & Structure
The dashboard utilizes a Star Schema to ensure optimal performance and filter accuracy. Filters flow from the central date and location dimensions to the corresponding fact tables.

Table Name	Role	Key Column	Relationship
DimDate	Central Dimension	Date	1-to-Many (*) to all Fact Tables.
DimLocation	Dimension	Location_ID or City	1-to-Many (*) to all Fact Tables.
Fact_Historical_Weather	Fact	Date, Location_ID	Stores daily observed weather metrics.
Fact_Forecast_Model	Fact	Date, Location_ID	Stores predicted weather data.

Export to Sheets
3. Key Dashboard Sections & Analysis
The report is divided into distinct pages to address different analytical needs:

Page 1: Current Conditions & Model Accuracy 🎯
Key Performance Indicators (KPIs): Displays the current/last recorded metrics for Temperature, Wind Speed, and Humidity.

Forecast Deviation: Compares Actual vs. Forecasted values (e.g., daily high temperature) to gauge the predictive model's performance and track historical error rates.

Filters: Primary slicers for City and Date Range.

Page 2: Time-Series Trends 📈
Trend Analysis: Line charts tracking long-term trends for key variables (Temperature, Precipitation) across the historical period.

Comparative View: Allows users to view the 7-day rolling forecast overlaid onto the historical averages to identify potential anomalies or plan for upcoming weather events.

Page 3: Geographical Overview 🌍
Map Visualization: Displays aggregated weather data (e.g., average max temperature) across all monitored locations, allowing for quick regional comparison.

Drill-down: Enables selection of a specific location to automatically filter all other visuals to the detailed data for that city.
