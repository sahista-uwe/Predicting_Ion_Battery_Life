# Predicting_Ion_Battery_Life



## Project Overview
This project focuses on predicting the Remaining Useful Life (RUL) of lithium-ion batteries using advanced feature engineering techniques on battery cycle data. The data includes electrical, thermal, and impedance measurements recorded over thousands of charge-discharge cycles.

## Dataset
- Approximately 7,565 CSV files with alternating measurement types:
  - Voltage, Current, Temperature, Load, Time
  - Sense Current, Battery Current, Current Ratio, Battery Impedance, Rectified Impedance
- Metadata CSV containing columns such as:
  - `Cycle`, `Capacity`, `Re`, `Rct`, `RUL`, `Type`, `Start_time`, `Ambient_temperature`, `Battery_id`, `Test_id`, `UID`, `Filename`

---

## Data Preprocessing

- Load raw discharge metadata from CSV
- Compute Remaining Useful Life (RUL)
- Filter only valid discharge cycles
- Create target labels for ML models

---

## Visualization

- Capacity vs Cycle plots
- RUL vs Cycle trends
- Voltage, Current, and Temperature profiles

---

## Basic Feature Engineering

### 🔹 Time-Domain Features:
- Voltage/Current/Temperature Mean
- Duration of each cycle
- Capacity ratio (normalized to first cycle)

### 🔹 Impedance-Domain Features:
- Mean, Std, Max, Min impedance per cycle
- Rate of change in impedance

---

## Advanced Feature Engineering

### 1. **Degradation Trend Features**
- Capacity trend: `.diff()` and normalized rate
- Current trend
- Moving averages (mean/EMA)
- Features from both time & impedance domains

### 2. **Lag Features**
- Lag values of voltage, impedance, capacity, etc.

### 3. **Smoothed & Delta Features**
- Rolling mean, std, min, max
- Exponential Moving Average (EMA)
- Cycle-to-cycle deltas (change in voltage, capacity)
- Trend direction (delta normalized to mean)

### 4. **Power & Efficiency Features**
- Instantaneous power (V * I)
- Energy per cycle (power × duration)
- Cumulative energy delivered
- Efficiency metrics (e.g., energy per temperature)
- Capacity degradation metrics

### 5. **Interaction Features**
- Health index (combined voltage, current, temp, impedance)
- Cross-domain ratios:
  - Capacity/Impedance
  - Power/Temperature
  - Voltage/Impedance
  - Capacity per Cycle Impedance

---


## Goal
Predict battery Remaining Useful Life (RUL) before the capacity falls below 80% of initial capacity.

---

https://www.kaggle.com/datasets/patrickfleith/nasa-battery-dataset
