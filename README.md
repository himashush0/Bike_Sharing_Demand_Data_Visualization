# 🚲 Bike-Sharing Demand Prediction — Data Visualization Project

A data visualization major project analyzing the **Seoul Bike Sharing Demand**
dataset to understand how weather, day of the week, and time of day affect
bike rental demand.

## 📌 Problem Statement

Bike-Sharing demand is predicting the number of bikes that will be rented from
a Bike-Sharing system at a given time based on weather, day of the week, and
time of day. The purpose is to build a predictive model to accurately forecast
bike rental demand in order to optimize bike allocation and improve the
bike-sharing system's overall efficiency.

This notebook covers the **exploratory data analysis (EDA) and visualization**
phase — the essential groundwork before building a predictive model.

## 📁 Project Files

| File | Description |
|---|---|
| `Bike_Sharing_Demand_Data_Visualization.ipynb` | Main Google Colab notebook with full EDA & visualizations |
| `Bike_Sharing_Demand.csv` | Dataset (8,760 hourly records, Seoul bike-sharing system) |
| `README.md` | This file |

## 📊 Dataset Description

The dataset contains **8,760 hourly records** (one full year) with the
following columns:

| Column | Description |
|---|---|
| Date | Date of record (dd/mm/yyyy) |
| Rented Bike Count | Target variable — number of bikes rented in that hour |
| Hour | Hour of the day (0–23) |
| Temperature(°C) | Air temperature |
| Humidity(%) | Relative humidity |
| Wind speed (m/s) | Wind speed |
| Visibility (10m) | Visibility distance |
| Dew point temperature(°C) | Dew point |
| Solar Radiation (MJ/m2) | Solar radiation |
| Rainfall(mm) | Rainfall amount |
| Snowfall (cm) | Snowfall amount |
| Seasons | Winter / Spring / Summer / Autumn |
| Holiday | Holiday / No Holiday |
| Functioning Day | Whether the system was operational (Yes/No) |

There are no missing values or duplicate rows in the raw data.

## 🚀 How to Run (Google Colab)

1. Go to [Google Colab](https://colab.research.google.com/drive/1BywHsLw3l2eSbO01bWDNkveCpd_K04-W?usp=sharing) and select
   **File → Upload notebook**, then upload
   `Bike_Sharing_Demand_Data_Visualization.ipynb`.
2. Run the cells from top to bottom (**Runtime → Run all**).
3. When you reach the **"Load the Dataset"** cell, a file-upload prompt will
   appear — select `Bike_Sharing_Demand.csv` from your computer.
   - Alternatively, uncomment the Google Drive option in that cell if you'd
     rather store the CSV in your Drive.
4. All charts (Matplotlib, Seaborn, and interactive Plotly) will render
   automatically in the notebook.

No manual package installation is needed — `pandas`, `numpy`, `matplotlib`,
`seaborn`, and `plotly` are pre-installed in Colab.

## 🔍 What the Notebook Covers

1. Data loading & understanding (structure, types, missing values, stats)
2. Feature engineering — Day of Week, Month, Weekend flag
3. Distribution of the target variable (Rented Bike Count)
4. Demand by **time of day** (hourly patterns, weekday vs weekend)
5. Demand by **day of the week**
6. Demand by **season** and **month**
7. Impact of **weather**: temperature, humidity, wind, visibility, rainfall,
   snowfall, solar radiation
8. Holiday and functioning-day effects on demand
9. Correlation heatmap of numerical features
10. Combined Hour × Day-of-Week heatmap
11. Interactive seasonal and time-series charts (Plotly)
12. Key insights summary and conclusion

## 💡 Key Insights

- Demand peaks around **8 AM and 6 PM** on weekdays (commuter pattern) and
  shows a single broader midday peak on weekends (recreational use).
- **Summer** has the highest average demand; **Winter** the lowest.
- **Temperature** is the strongest positive weather driver of demand;
  **Humidity** correlates negatively.
- **Rainfall** and **snowfall** sharply reduce rentals.
- Demand is **lower on holidays** than on regular working days.

## 🛠️ Tech Stack

- Python 3
- pandas, numpy — data handling
- matplotlib, seaborn — static visualizations
- plotly — interactive visualizations
- Google Colab — execution environment

## 📈 Next Steps

Use the insights and engineered features (Hour, Temperature, Humidity, Season,
Day-of-Week, Holiday status) to build a regression/ML model (e.g., Linear
Regression, Random Forest, or XGBoost) to forecast `Rented Bike Count` and
support real-time bike allocation decisions.
