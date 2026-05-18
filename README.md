<div align="center">

# 🌦️ WEATHER HISTORY EXPLORATORY DATA ANALYSIS  
## 🌍 Climate Pattern Discovery & Atmospheric Insights  
---

</div>

## 📌 Project Overview
This project performs Exploratory Data Analysis (EDA) on a historical weather dataset (96,453 rows, 12 columns) from a UK region. The goal is to uncover atmospheric patterns, seasonal trends, climate behavior, and interconnected relationships between key weather variables while identifying long-term climate trends and recurring atmospheric states.

---

## 🛠️ Technologies & Libraries Used
* **Language:** Python
* **Data Libraries:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn, Plotly
* **Environment:** Jupyter Notebook

---

## 🧹 Data Cleaning & Preprocessing
* **Missing Values:** Removed 517 null records from the precipitation column.
* **Feature Dropping:** Removed the `Cloud Cover` column due to unrealistic/constant values.
* **Anomaly Correction:** Detected >1,000 invalid pressure values recorded as 0 millibars; corrected them using median imputation.
* **Feature Engineering:** Extracted `Year`, `Month`, `Day`, `Hour`, and `Season` from the datetime column.
* **Data Integrity:** Checked for duplicates and ensured consistent data types across all usable features.

---

## 🔍 Analysis Workflow & Key Findings

### 📊 Univariate Analysis (Distributions)
* Temperature follows a natural seasonal bell-curve, while humidity remains consistently high throughout the year.
* Wind speeds are right-skewed (mostly calm-to-moderate); extreme storm events appear less common.
* Precipitation is heavily dominated by rainfall; cloudy/overcast conditions occur most frequently.

### 📉 Bivariate Analysis (Core Correlations)
* **Temperature vs Humidity ($r \approx -0.63$):** Strong negative correlation; warmer air holds more moisture before saturation, leading to drier relative humidity.
* **Humidity vs Visibility ($r \approx -0.37$):** Negative relationship; higher moisture creates fog, haze, and mist, scattering light.
* **Temperature vs Visibility ($r \approx 0.39$):** Positive relationship; warmer conditions reduce condensation, dramatically improving atmospheric clarity.
* **Precipitation Control:** Temperature acts as the absolute physical switch determining precipitation type (Rain vs. Snow).

### 🌐 Multivariate Analysis (Systemic States)
The climate systematically clusters into two major, recurring environmental states:
1. **Warm-Clear-Dry State:** Characterized by higher temperatures, lower relative humidity, excellent visibility, lower pressure tendencies, and rainfall.
2. **Cold-Humid-Foggy State:** Characterized by freezing temperatures, high relative humidity, low visual range, stable high-pressure systems, and snowfall.

---

## 💡 Major Insights
* **Central Driver:** Temperature acts as the master control variable influencing humidity, visibility, and precipitation behavior.
* **Climate Signal:** The region shows signs of gradual warming over time; the average temperature in 2016 was nearly 0.8°C higher than in 2006.
* **Stability:** Wind speed behaves purely as a supporting variable rather than a dominant weather driver, confirming a stable temperate maritime climate.

---

## 🚀 Future Improvements & Next Steps
* **Predictive Modeling:** Deploy time-series forecasting and regression models to predict temperature shifts and visibility drops.
* **Classification Pipeline:** Build a machine learning classification model to predict Rain vs. Snow using atmospheric features.
* **Advanced Integration:** Merge this dataset with regional transport, energy grid consumption, or environmental pollution data to analyze real-world socioeconomic impacts.

---

## ✅ Conclusion

* This project revealed that the region follows a stable temperate maritime climate with predictable seasonal behavior. 
* Temperature emerged as the primary atmospheric driver influencing humidity, visibility, and precipitation type.
* The analysis identified two recurring atmospheric states: warm-clear-dry and cold-humid-foggy conditions.

* The dataset also revealed possible signs of gradual warming over time, supported by an increase in average temperature between 2006 and 2016.
* Overall, the project demonstrates how weather variables interact together as a connected atmospheric system rather than independent measurements.
---

## 📁 Project Structure
```text
Weather-History-EDA/
├── data/
│   └── weatherHistory.csv
├── notebooks/
│   └── Weather_History_EDA.ipynb
├── README.md
└── .gitignore
