
# Codveda Technology — Data Science Internship

This repository contains the completed tasks for the Codveda Data Science Internship.
All tasks are implemented in Python using industry-standard data science libraries.

---

## 📁 Repository Structure

Codveda-Data-Science-Internship/
│
├── Codveda_DS_L1T2_L2T1_Housing_Analysis.ipynb  # Main notebook
├── 4__house_Prediction_Data_Set.csv              # Raw dataset
├── cleaned_house_data.csv                        # Cleaned dataset (post outlier removal)
├── cleaned_scaled_house_data.csv                 # Final scaled dataset (model-ready)
└── README.md

---

## 📌 Level 1 — Task 2: Data Cleaning & Preprocessing

**Dataset:** Boston-style Housing Dataset (506 records, 14 features)  
**Goal:** Clean and preprocess raw data to make it suitable for machine learning.

### Steps Performed:
- Loaded raw dataset and assigned meaningful column names
- Checked and confirmed zero missing values
- Visualized distributions using boxplots and histograms
- Removed censored House_Value entries (values >= 50)
- Applied IQR-based outlier removal on Avg_Rooms
- Applied IQR clipping on Crime_Rate, Social_Index, and House_Value
- Log-transformed Crime_Rate to reduce right skew
- Standardized all numerical features using StandardScaler (zero mean, unit variance)
- Saved cleaned and scaled datasets to CSV

### Tools Used:
Python, pandas, numpy, scikit-learn, matplotlib, seaborn

---

## 📌 Level 2 — Task 1: Predictive Modeling (Regression)

**Dataset:** Cleaned Housing Dataset (from Level 1 Task 2)  
**Goal:** Build and evaluate regression models to predict house prices.

### Steps Performed:
- Checked multicollinearity using Variance Inflation Factor (VIF)
- Dropped high VIF features: Crime_Rate_log (VIF 14.47) and Highway_Access (VIF 14.56)
- Final feature set: 10 post-VIF approved predictors
- 80/20 train-test split with random_state=365

### Models Trained & Evaluated:

| Model | MAE | MSE | RMSE | R² |
|---|---|---|---|---|
| Simple Linear Regression (Avg_Rooms only) | 4.03 | 28.80 | 5.37 | 0.3388 |
| Multiple Linear Regression (10 features) | 2.27 | 8.99 | 2.99 | 0.7937 |
| Decision Tree Regressor | 2.99 | 16.05 | 4.06 | 0.6316 |
| Random Forest Regressor | 1.78 | 5.43 | 2.35 | 0.8748 |

### Key Findings:
- Simple regression with one feature explained only 33% of variance — expected baseline
- Multiple regression jumped to 79% after incorporating all 10 features
- Decision Tree underperformed linear regression due to overfitting on training data
- Random Forest achieved the best performance at R² = 0.87 by averaging 100 decision trees, reducing overfitting and handling non-linear relationships

### Tools Used:
Python, pandas, numpy, scikit-learn, matplotlib, seaborn, statsmodels

---

## 🛠️ How to Run

1. Clone the repository
   git clone https://github.com/MaroCoding/Codveda-Data-Science-Internship.git

2. Install dependencies
   pip install pandas numpy scikit-learn matplotlib seaborn statsmodels jupyter

3. Open the notebook
   jupyter notebook Codveda_DS_L1T2_L2T1_Housing_Analysis.ipynb

4. Run all cells top to bottom

---

## 📊 Libraries & Versions

- Python 3.x
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn
- statsmodels

---

## 👤 Author

**MaroCoding**  
Data Science Intern @ Codveda Technology  
https://www.linkedin.com/in/marwan-kandil/

---

## 🏷️ Tags

`#CodvedaJourney` `#CodvedaExperience` `#FutureWithCodveda` `#DataScience` `#MachineLearning` `#Python`
