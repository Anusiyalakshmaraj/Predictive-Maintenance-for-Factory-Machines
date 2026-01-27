# 🏭 Predictive Maintenance for Factory Machines

## 📌 Project Overview

In modern factories, machines are expected to run continuously without failure. Unexpected breakdowns can cause production delays, financial loss, and safety risks.  
This project focuses on predicting **when a machine is likely to fail** so that maintenance can be done in advance. This approach is called **Predictive Maintenance**.

The goal of this project is to estimate the **Remaining Useful Life (RUL)** of machines using sensor data collected over time, helping industries reduce downtime and maintenance costs.

---

## 🎯 Objective

- Analyze machine sensor data collected over operating cycles  
- Detect performance degradation trends  
- Estimate how long each machine can continue to operate safely  
- Support early maintenance decisions before actual failure occurs  

---

## 📊 Dataset Description

The dataset contains:

- Multiple machines (engines)  
- Repeated measurements over time (cycles)  
- Several sensor readings for each machine  
- Operational settings affecting performance  

Each row represents one machine at one time cycle with its sensor values.

---

## 🛠️ Project Workflow

### 1. Data Loading
- Load training sensor data  
- Inspect structure and basic statistics  

### 2. Data Cleaning
- Handle missing values  
- Remove sensors with very low variation  
- Keep a raw copy for comparison  

### 3. Data Normalization
- Scale sensor values to maintain consistency  
- Improve model learning performance  

### 4. Exploratory Analysis
- Visualize sensor drift over cycles  
- Observe degradation patterns  

### 5. Feature Engineering
- Compute Remaining Useful Life (RUL) for each machine  
  **RUL = Max Cycle of Engine − Current Cycle**  
- Create degradation-related features  
- Normalize cycle position for each engine  

### 6. Rolling Window Features
- Rolling Mean  
- Rolling Standard Deviation  
These features help capture recent behavior trends of sensors.

---

## 📈 Key Concepts Used

- Time-series based machine monitoring  
- Sensor degradation analysis  
- Remaining Useful Life (RUL) estimation  
- Rolling statistical features  
- Data normalization and preprocessing  

---

## ✅ Outcome

The processed dataset becomes suitable for building machine learning or deep learning models that can:

- Predict how close a machine is to failure  
- Identify risky machines early  
- Help schedule maintenance efficiently  

This system can significantly reduce unexpected breakdowns and improve factory productivity.

---

## 🚀 Future Improvements

- Apply Machine Learning models (Random Forest, XGBoost, etc.)  
- Try Deep Learning models (LSTM for time-series prediction)  
- Compare model performance using RMSE or MAE  
- Build a simple dashboard for maintenance alerts  

---
