# 🔋 EV Adoption Forecasting using Machine Learning

## 📌 Problem Statement
As electric vehicle (EV) adoption surges, urban planners and policymakers must anticipate infrastructure needs—especially for charging stations. Inadequate planning can lead to bottlenecks, congestion, and reduced user satisfaction.

**🎯 Goal:**  
Forecast future EV adoption across Washington State counties using historical registration data. The prediction helps inform smarter infrastructure deployment and long-term energy planning.

---

## 📊 Dataset Overview

- **Source:** [Kaggle - EV Population Size 2024](https://www.kaggle.com/datasets/sahirmaharajj/electric-vehicle-population-size-2024)
- **Timeframe:** January 2017 – February 2024
- **Key Features:**
  - `County`, `State`
  - `Vehicle Type` (e.g., Passenger, Truck)
  - `EV Type`: BEV (Battery EV), PHEV (Plug-in Hybrid EV)
  - `% EVs`, `Total Vehicles`

---

## 🔧 Workflow Summary

### 1️⃣ Data Cleaning
- Parsed `Date` column to datetime format.
- Removed or imputed missing values in `County` and `State`.
- Converted EV-related numeric columns from string to integers.

### 2️⃣ Feature Engineering
- Extracted `Year` and `Month` from date.
- Encoded categorical features (e.g., `County`, `Vehicle Primary Use`).

### 3️⃣ Model Building
- **Model Used:** Random Forest Regressor
- **Features:** `Year`, `Month`, `Vehicle Use`, `County`
- **Target:** Total EVs

### 4️⃣ Forecasting
- Generated EV adoption predictions from **2024 to 2026**.
- Trends indicate consistent year-on-year growth.

---

## 📈 Results

- Model achieved acceptable accuracy on validation data.
- EV adoption projected to **increase steadily** in most counties.
- Urban counties showed significantly higher growth rates.

---

## 📂 Files Included

| File Name | Description |
|-----------|-------------|
| `EV_Adoption_Forecasting.ipynb` | Jupyter Notebook with full pipeline |
| `preprocessed_ev_data.csv` | Cleaned & feature-engineered dataset |
| `forecasting_ev_model.pkl` | Trained Random Forest model |

---

## 🚀 Future Improvements

- Try **XGBoost**, **Prophet**, or **LSTM** models for time-series enhancements.
- Include external data (e.g., fuel prices, policy incentives).
- Use **geospatial clustering** to assist charging station deployment.

---

## 👤 Author

**Varsha Tiwari**  
