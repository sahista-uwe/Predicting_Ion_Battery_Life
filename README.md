# Predicting_Ion_Battery_Life

# Battery Life Prediction - Advanced Feature Engineering

## Project Overview
This project focuses on predicting the Remaining Useful Life (RUL) of lithium-ion batteries using advanced feature engineering techniques on battery cycle data. The data includes electrical, thermal, and impedance measurements recorded over thousands of charge-discharge cycles.

## Dataset
- Approximately 7,565 CSV files with alternating measurement types:
  - Voltage, Current, Temperature, Load, Time
  - Sense Current, Battery Current, Current Ratio, Battery Impedance, Rectified Impedance
- Metadata CSV containing columns such as:
  - `Cycle`, `Capacity`, `Re`, `Rct`, `RUL`, `Type`, `Start_time`, `Ambient_temperature`, `Battery_id`, `Test_id`, `UID`, `Filename`

## Goal
Predict battery Remaining Useful Life (RUL) before the capacity falls below 80% of initial capacity.

---

https://www.kaggle.com/datasets/patrickfleith/nasa-battery-dataset
