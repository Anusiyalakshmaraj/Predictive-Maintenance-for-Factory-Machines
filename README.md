# 🏭 Predictive Maintenance for Factory Machines

## Problem Statement
Unexpected machine failures in factories can lead to production downtime, increased maintenance costs, and safety risks. The objective of this project is to predict how long a machine can continue operating before failure. By estimating the **Remaining Useful Life (RUL)** of machines in advance, maintenance can be planned proactively instead of reacting after breakdowns occur.

This project uses historical sensor data collected from factory machines to forecast degradation trends and remaining operational life.

---

## Objective

- Analyze machine sensor data collected over operating cycles  
- Detect performance degradation trends  
- Estimate how long each machine can continue to operate safely  
- Support early maintenance decisions before actual failure occurs  

---

## Tools and Technologies Used
- **Programming Language:** Python  
- **Libraries:**  
  - Pandas, NumPy (data processing)  
  - Matplotlib (visualization)  
  - Scikit-learn (machine learning models and evaluation)  
  - XGBoost (advanced regression modeling)  
- **Dataset:** NASA Turbofan Engine Degradation Dataset (FD001)
  ---
## Dataset Description

The dataset contains:

- Multiple machines (engines)  
- Repeated measurements over time (cycles)  
- Several sensor readings for each machine  
- Operational settings affecting performance  

Each row represents one machine at one time cycle with its sensor values.

---

## Methodology

### 1. Data Loading and Understanding
- Loaded training and testing datasets containing machine cycle information and sensor readings.
- Assigned meaningful column names based on official dataset documentation.
- Verified the number of machines and ensured cycle continuity for time-series consistency.

### 2. Data Cleaning and Preparation
- Checked for missing cycles to confirm complete operational histories.
- Removed low-variance sensors that contribute little to degradation prediction.
- Standardized sensor values to ensure consistent feature scaling.

### 3. Exploratory Analysis and Visualization
- Visualized sensor trends across machine cycles to observe degradation behavior.
- Compared sensor values before and after normalization.
- Analyzed sensor drift and operational patterns for individual machines.

### 4. Feature Engineering
- Computed **Remaining Useful Life (RUL)** for each machine cycle.
- Created degradation-based features such as:
  - Normalized cycle position  
  - Rolling mean and rolling standard deviation  
  - Sensor change rates (deltas)  
- Designed a **health index** to represent overall machine degradation.
- Handled missing values introduced during rolling calculations.

### 5. Model Development
- Split data into training and validation sets based on machine identifiers.
- Trained multiple regression models:
  - Random Forest Regressor  
  - Gradient Boosting Regressor  
  - XGBoost Regressor  

### 6. Model Evaluation and Comparison
- Evaluated models using **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)**.
- Visualized actual vs predicted RUL values.
- Compared model predictions at the individual machine level.
- Identified key features influencing degradation prediction.

### 7. Final Testing and Prediction
- Generated RUL predictions for unseen test machines.
- Compared predicted RUL values with true remaining life values.
- Saved final predictions in CSV format for deployment or analysis.

---

## Results
- Accurate prediction of machine Remaining Useful Life (RUL).
- Random Forest model demonstrated strong and stable performance.
- Time-series feature engineering significantly improved prediction accuracy.
- Final output file generated:  
  **`FD001_RUL_predictions.csv`**

---

## Key Learnings and Conclusion
- Predictive maintenance benefits greatly from time-series and degradation-based features.
- Sensor trend analysis provides more insight than raw sensor values alone.
- Machine-level data splitting improves real-world reliability.
- Ensemble models are effective for complex regression tasks like RUL prediction.
- This project demonstrates how data-driven maintenance can reduce downtime and improve factory efficiency.

---
