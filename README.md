# Income Prediction with Random Forest

This project develops a **Random Forest Regression** model to estimate customers' annual income based on their transaction and demographic data.  

## 📌 Project Overview
- **Objective:** Predict `annual_salary` using customer and transaction features.  
- **Algorithm:** Random Forest Regressor  
- **Dataset Size:** ~12K rows, 28+ columns  
- **Target Variable:** `annual_salary`  

## ⚙️ Preprocessing Steps
1. Performed descriptive statistics.  
2. Feature Engineering:
   - `payment_period_mean_by_bin_age`, `payment_period_max_by_bin_age`  
   - `amount_mean_by_txn_description`, `amount_max_by_txn_description`  
   - `balance_mean_by_merchant_suburb`, `balance_max_by_merchant_suburb`  
3. Dropped high-cardinality columns (unique values > 10).  
4. Handled missing values using `mode()` for categorical and `mean()` for numerical features.  
5. Applied `LabelEncoder()` for categorical variables.  

## 📊 Modeling
- Split dataset into **train/test (80/20)**.  
- Trained multiple Random Forest models:  
  1. Default parameters  
  2. Feature importance-based selection  
  3. Optimized hyperparameters  
- Evaluated with metrics: **MAE, MSE, RMSE, R²**  

## 🛠️ Tech Stack
- Python 3.x  
- Pandas, NumPy  
- Scikit-learn  
- Matplotlib, Seaborn  

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/<your-username>/income-prediction-rf.git
   cd income-prediction-rf
