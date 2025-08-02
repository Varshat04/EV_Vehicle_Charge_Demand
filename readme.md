# 🔋 EV Adoption Forecasting using Machine Learning

## 📌 Problem Statement

As electric vehicle (EV) adoption rapidly increases, planners and policymakers must forecast infrastructure demands—especially for EV charging stations. Without proper forecasting, cities may face overloaded infrastructure, low user satisfaction, and inefficient planning.

**🎯 Goal:**  
To predict future EV adoption across Washington State counties using historical registration data, enabling smarter EV infrastructure deployment and long-term policy decisions.

---

## 📊 Dataset Overview

- **Source:** [Kaggle - EV Population Size 2024](https://www.kaggle.com/datasets/sahirmaharajj/electric-vehicle-population-size-2024)
- **Period Covered:** January 2017 – February 2024
- **Key Features:**
  - `County`, `State`
  - `Vehicle Type` (Passenger, Truck)
  - `EV Type`: BEV (Battery Electric Vehicle), PHEV (Plug-in Hybrid Electric Vehicle)
  - `% EVs`, `Total Vehicles`

---

## 🔧 Workflow Summary

### 1️⃣ Data Cleaning
- Converted `Date` to datetime format.
- Handled missing values in `County` and `State`.
- Cleaned and converted numeric EV columns.

### 2️⃣ Feature Engineering
- Generated lag, rolling mean, and percent change features.
- Encoded categorical variables (`County`, `Vehicle Use`) for modeling.
- Created a time progression variable (`months_since_start`).

### 3️⃣ Model Building
- **Model Used:** Random Forest Regressor
- **Features Used in Model:**
  - `months_since_start`, `county_encoded`
  - `ev_total_lag1`, `ev_total_lag2`, `ev_total_lag3`
  - `ev_total_roll_mean_3`, `ev_total_pct_change_1`, `ev_total_pct_change_3`
  - `ev_growth_slope`
- **Target Variable:** `Electric Vehicle (EV) Total`

### 4️⃣ Forecasting
- Forecasted county-wise EV adoption for the next **36 months (2024–2026)**.
- Integrated results into an interactive Streamlit dashboard.

---

## 📈 Results

- The model forecasts a steady growth in EV adoption across most counties.
- Urban and high-density counties show steeper adoption curves.
- Visual dashboard enables comparison across counties with predicted growth percentages.

---

## 🚀 Streamlit Web App

An interactive dashboard was built using **Streamlit** to visualize and explore EV adoption trends by county.

### 🎯 Key Features:
- Forecast EV totals and cumulative growth for any selected county.
- Compare EV adoption trends across up to 3 counties.
- Visual summary of 3-year projected EV growth with intuitive charts.

📸 ![Dashboard Preview](ev-car-factory.jpg)

To run locally:
```bash
streamlit run app.py
