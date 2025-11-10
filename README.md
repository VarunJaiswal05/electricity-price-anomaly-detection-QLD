Electricity Price Anomaly Detection – Queensland (NEM Market)
==============================================================

This project was developed for IFN695 - Minor Research Project 
at Queensland University of Technology (QUT).

It focuses on detecting electricity price anomalies in Queensland’s 
National Electricity Market (NEM) using two unsupervised learning techniques:
Isolation Forest and LSTM Autoencoder.


--------------------------------------------------------------
OBJECTIVE
--------------------------------------------------------------
To develop a label-free anomaly detection framework that identifies 
electricity price spikes or drops by analyzing historical market and 
weather data.

The project aims to uncover:
- Hidden temporal patterns in pricing anomalies
- Environmental and operational factors influencing price volatility
- Market conditions leading to high-risk events


--------------------------------------------------------------
DATASETS USED
--------------------------------------------------------------
1. AEMO Market Datasets:
   - DISPATCHPRICE: 5-minute dispatch prices
   - DISPATCHREGIONSUM: 5-minute summary of demand, generation, and flow
   - TRADINGPRICE: 30-minute trading prices

2. Bureau of Meteorology (BoM) Weather Data:
   - Temperature
   - Rainfall
   - Solar Radiation

Region: Queensland (QLD)
Time Period: January 2022 – December 2024


--------------------------------------------------------------
FEATURES ENGINEERED
--------------------------------------------------------------
- lagged_RRP: Rolling lag of regional reference price
- price_change_pct: Percentage price change between consecutive intervals
- demand_error: Difference between forecasted and actual demand
- hour_of_day, day_of_week: Temporal context features
- Weather variables: TEMPERATURE, RAINFALL, SOLAR_RADIATION
- All features normalized using MinMaxScaler


--------------------------------------------------------------
MODELS USED
--------------------------------------------------------------
1. Isolation Forest
   - Detects anomalies based on feature-space rarity
   - Effective for multidimensional unsupervised detection

2. LSTM Autoencoder
   - Learns temporal dependencies and reconstruction patterns
   - Flags anomalies based on high reconstruction error


--------------------------------------------------------------
RESULTS & INSIGHTS
--------------------------------------------------------------
- Both models detected overlapping high-confidence anomalies
- Clusters of anomalies observed during:
  • Weekday mornings (peak demand)
  • Weekend evenings (demand drops)
- Environmental variables such as temperature correlated strongly 
  with anomaly intensity and frequency
- The dual-model agreement enhanced interpretability and reliability


--------------------------------------------------------------
CONCLUSIONS
--------------------------------------------------------------
The hybrid unsupervised approach provided a robust way to detect and 
analyze electricity price anomalies without labeled data. The study 
demonstrates that combining feature-space and temporal anomaly detection 
methods (Isolation Forest + LSTM Autoencoder) can yield consistent and 
interpretable anomaly signals for the Queensland NEM market.


--------------------------------------------------------------
AUTHOR INFORMATION
--------------------------------------------------------------
Varun Vikas Jaiswal
Student ID: N11736089
Queensland University of Technology (QUT)
Unit: IFN695 - Minor Research Project
Year: 2025

--------------------------------------------------------------
KEYWORDS
--------------------------------------------------------------
Electricity Pricing, NEM, Queensland, Isolation Forest, 
LSTM Autoencoder, Anomaly Detection, Unsupervised Learning, 
Machine Learning, Energy Analytics, Time Series Analysis
