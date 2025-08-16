# 🌾 Crop Yield Prediction (1997–2023)

## 📌 Brief Description
This project analyzes and predicts agricultural crop yields in India using historical data (1997–2020) and forecasts up to 2023.  
Leveraging **Prophet time series models** with climatic and input-related regressors, it provides insights into **season-wise yield trends, top & bottom performing states, and policy implications**.  

---

## 📂 Repository Contents
- **Crop Yield Prediction.ipynb** → Main Python notebook containing data cleaning, feature engineering, time series forecasting, and evaluation.  
- **Cleaned_Crops_data.csv** → Cleaned dataset used for Power BI dashboard (2010–2017).  
- **Reports/**  
  - *Prediction Report* (Methodology, results, insights)  
  - *Crops Data Report* (2010–2017 dataset analysis)  
  - *Statistical Awareness Report* (answers to questionnaire & dashboard overview)  
- **Power BI Dashboard** → Interactive dashboard for state & crop-level analysis.  

---

## ⚙️ Data Preparation & Cleaning
1. Removed duplicate rows and standardized column names.  
2. Filtered out entries where `Area`, `Production`, or `Yield` = 0.  
3. Converted `Crop_Year` into proper datetime format.  
4. Handled missing values in regressors (`Rainfall`, `Fertilizer`, `Pesticide`) using state-wise means.  
5. Assigned **seasonal ranges** (Kharif, Rabi, Summer, Autumn, Winter, Whole Year).  

---

## 📊 Methodology
- **Feature Engineering:** Lag features, rolling averages, YoY changes, and sudden yield spike indicators.  
- **Modeling:** Trained **Prophet** models separately for Rice, Wheat, and Pulses.  
- **Regressors Used:**  
  - Area & Production  
  - Annual Rainfall  
  - Fertilizer & Pesticide usage  
  - Lagged yield variables (`Yield_Lag1`, `Yield_Lag2`, etc.)  
- **Cross Validation:** To assess forecasting accuracy.  
- **Autocorrelation Analysis:** Identified seasonality patterns.  

---

## 🔮 Forecasting
- Predicted yields for **2015–2023**, keeping **actuals fixed until 2020**.  
- Forecasts for **2021–2023** extend using historical averages for regressors.  
- Compared **Actual vs Predicted yields** (2015–2020) for validation.  
- Identified **Top 5 and Bottom 5 states** by mean predicted yields.  

---

## 📈 Key Insights
- Climatic factors (rainfall) and input usage (fertilizer, pesticide) strongly influence yield variations.  
- Punjab, Delhi, and Haryana consistently perform as **high-yield states**, while Chhattisgarh, Odisha, and Assam show **lower yields**.  
- Policy strategies like **better irrigation, input optimization, and region-specific support** can help bridge yield gaps.  

---
