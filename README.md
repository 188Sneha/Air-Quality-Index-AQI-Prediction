# 🌫️ Air Quality Index (AQI) Prediction using KNN Regression

This project uses machine learning to predict the **Air Quality Index (AQI)** of Indian cities based on various air pollutant concentrations. The model is built using the **K-Nearest Neighbors (KNN)** regression algorithm and visualized using Seaborn and Matplotlib.

---

## 📂 Dataset

- **File:** `city_day.csv`
- **Source:** Central Pollution Control Board (CPCB), India
- **Columns of interest:** 
  - Pollutants: `PM2.5`, `PM10`, `NO`, `NO2`, `NOx`, `CO`, `SO2`, `O3`, `NH3`, `Benzene`, `Toluene`, `Xylene`
  - Target: `AQI` (Air Quality Index)
  - Others: `City`, `Date`, etc.

---

## 🔧 Project Workflow

1. **Data Loading & Cleaning**
   - Uploads `city_day.csv` in Google Colab.
   - Removes rows with missing AQI values.
   - Fills missing pollutant data with column means.

2. **Feature Engineering**
   - Selects key pollutants as input features.
   - Splits dataset into training (80%) and testing (20%).

3. **Preprocessing**
   - Applies `StandardScaler` to normalize features for KNN.

4. **Modeling**
   - Uses `KNeighborsRegressor` with `n_neighbors=5`.
   - Trains the model and makes predictions.

5. **Evaluation**
   - R² Score and Mean Squared Error (MSE) on train/test data.
   - Visualization of:
     - AQI distribution across cities
     - Residuals (prediction errors)
     - Actual vs Predicted AQI

---

## 🛠️ Requirements

- Python Libraries:
  ```bash
  pandas
  numpy
  matplotlib
  seaborn
  scikit-learn
  scipy
