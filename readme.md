# 🔋 EV Adoption Forecasting using Machine Learning

## 📌 Problem Statement
As electric vehicle (EV) adoption surges, planners need to anticipate infrastructure needs, especially for charging stations. Inadequate planning may result in bottlenecks and low user satisfaction.

**Goal:** Forecast future EV adoption based on historical registration data across Washington State counties using a regression model.

---

## 📊 Dataset

- **Source:** [Kaggle](https://www.kaggle.com/datasets/sahirmaharajj/electric-vehicle-population-size-2024)
- **Period:** Jan 2017 – Feb 2024
- **Key Features:**
  - County, State, Vehicle Type (Passenger/Truck)
  - EV Type: BEV, PHEV
  - Percent of EVs
  - Total Vehicles

---

## 🔧 Workflow

### 1. Data Cleaning
- Parsed `Date` column to datetime.
- Handled missing values in `County` and `State`.
- Converted EV count columns from strings to integers.

### 2. Feature Engineering
- Extracted `Year`, `Month` from date.
- Encoded categorical variables like `Vehicle Primary Use` and `County`.

### 3. Modeling
- Trained a **Random Forest Regressor** on:
  - Features: Year, Month, Vehicle Use, County
  - Target: Total EVs
- Evaluated with MAE, RMSE, and R² metrics.

### 4. Forecasting
- Predicted EV adoption for 2024–2026 based on past trends.

---

## 📈 Results

- Forecast shows steady growth in EV registrations.
- Model performed well with acceptable error margins.

---

## 📂 Files Included

- `EV_Adoption_Forecasting.ipynb` - Main notebook

---

## 🚀 Future Improvements

- Use XGBoost or LSTM models for better performance.
- Include economic and policy data as external features.
- Integrate geospatial analysis for charging station planning.

---

## 👤 Author

Varsha Tiwari
