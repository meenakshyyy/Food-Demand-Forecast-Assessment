# Food Demand Forecasting

## Project Overview
This project focuses on **demand forecasting** for a **meal delivery company** operating across multiple cities. Accurate forecasting helps fulfillment centers optimize **raw material procurement and staffing** to minimize food wastage and stockouts. The objective is to predict demand for the **next 10 weeks** (Weeks 146-155) using historical data and relevant meal and center attributes.

---

## Dataset
The dataset was provided in the **Genpact Machine Learning Hackathon** hosted by **Analytics Vidhya**.

### Dataset Description
The dataset consists of three primary files:

1. **Weekly Demand Data (`train.csv` & `test.csv`)**
   - Contains historical demand records for different **meal-center combinations**.
   - The target variable is `num_orders` (number of orders for each meal-center pair).

2. **Fulfillment Center Information (`fulfilment_center_info.csv`)**
   - Provides details about **each fulfillment center**, including its location, area, and type.

3. **Meal Information (`meal_info.csv`)**
   - Contains attributes for each meal, including **category** and **cuisine type**.

### Key Features
- **Time-based Features**: Week number (1 to 145 for training, 146-155 for prediction)
- **Center Attributes**: City, region, center type, and area of operation
- **Meal Attributes**: Category, cuisine, pricing details
- **Marketing Indicators**: Email promotions and homepage feature

---

## Technologies Used
This project is implemented in **Python** with the following libraries:

- **Jupyter Notebook** – Data analysis and model development
- **Pandas & NumPy** – Data manipulation and preprocessing
- **Matplotlib & Seaborn** – Data visualization
- **Scikit-Learn (sklearn)** – Machine learning models and evaluation metrics
- **XGBoost & LightGBM** – Advanced boosting models for better accuracy

---

## Installation & Setup Guide

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/meenakshyyy/Food-Demand-Forecast-Assessment.git
cd Food-Demand-Forecast-Assessment
```

### 2️⃣ Install Dependencies
Ensure you have **Python 3.x** installed, then install required libraries:
```bash
pip install pandas numpy scikit-learn seaborn matplotlib xgboost lightgbm
```

### 3️⃣ Running the Jupyter Notebook
To analyze the dataset and train models, launch Jupyter Notebook:
```bash
jupyter notebook
```
Open the file (`Food demad forecasting.ipynb`) and execute the cells sequentially.

---

## Model Performance & Results
We tested multiple machine learning models for demand forecasting, and the results are as follows:

- **Random Forest Regressor**: 64.45
- **Decision Tree Regressor**: 81.06

The **Random Forest Regressor** demonstrated Lowest RMSLE value (best performance), demonstrates superior accuracy in predicting food demand.

---

## Evaluation Metric
The competition evaluates models using **Root Mean Squared Logarithmic Error (RMSLE)**:
```math
RMSLE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (\log(\hat{y}_i + 1) - \log(y_i + 1))^2}
```
where:
- \( y_i \) is the actual demand
- \( \hat{y}_i \) is the predicted demand

The final score is **100 * RMSLE**.

---

## Conclusion
This project aims to enhance **demand forecasting accuracy** for food delivery services. By leveraging **machine learning techniques**, businesses can optimize inventory planning and reduce wastage. Future improvements may include **feature engineering, deep learning approaches, and time series analysis** for better forecasting precision.
