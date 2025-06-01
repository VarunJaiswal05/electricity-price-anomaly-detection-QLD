Electricity Price Anomaly Detection – Queensland (NEM Market)
This project was developed for IFN695 - Minor Research Project at Queensland University of Technology (QUT). It focuses on detecting electricity price anomalies in Queensland’s National Electricity Market (NEM) using two unsupervised learning techniques: Isolation Forest and LSTM Autoencoder.

Objective:
To develop a label-free anomaly detection framework that identifies electricity price spikes or drops by analyzing historical market and weather data.

Dataset Used:

AEMO data (DISPATCHPRICE, DISPATCHREGIONSUM, TRADINGPRICE)

Bureau of Meteorology (BoM) weather data (Temperature, Rainfall, Solar Radiation)

Time period: January 2022 to December 2024

Region: Queensland (QLD)

Features Engineered:

lagged_RRP, price_change_pct, demand_error

hour_of_day, day_of_week

Weather: TEMPERATURE, RAINFALL, SOLAR_RADIATION

All features normalized using MinMaxScaler

Models Used:

Isolation Forest: Detects anomalies based on feature-space rarity

LSTM Autoencoder: Detects anomalies from temporal reconstruction error in time series

Output Highlights:

High-confidence anomalies detected by both models

Temporal pattern clustering observed during weekday mornings and weekend evenings

Environmental factors like temperature showed strong correlation with pricing anomalies


Author:
Varun Vikas Jaiswal
Student ID: N11736089
Queensland University of Technology
IFN695 - Minor Project
