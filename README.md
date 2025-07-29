# 🏠 House Prices - Kaggle Regression Challenge

This repository contains my solution for the [House Prices - Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques) competition on Kaggle.
The goal is to predict the final sale price of residential homes in Ames, Iowa using advanced regression models based on 79 explanatory variables.

![Chesterwell_StreetScenes_Additional_MerseaHomes-25-of-31-CHESTERWELL-GROVE-1](https://github.com/user-attachments/assets/5f19550b-d512-4128-aa8e-5a21fa21a6bd)


---

## 🗂️ Project Structure
```

project-root/
├── 🧠 task.ipynb               # Main notebook: full ML pipeline from preprocessing to model predictions
├── 📊 train.csv                # Training data with house features and SalePrice
├── 🧪 test.csv                 # Test data for prediction
├── 📝 sample_submission.csv    # Submission format
├── 🚀 submission.csv           # Submission from LinearRegression
├── 🚀 submission1.csv          # Submission from SGDRegressor
├── 🚀 submission2.csv          # Submission from RandomForestRegressor
└── 📜 README.md                # Project documentation

```

---

## 💻 Technologies Used

- **Language**: Python 3.x  
- **Environment**: Jupyter Notebook

## 📦 Libraries

- `numpy`, `pandas` – Data manipulation  
- `matplotlib`, `seaborn` – Visualization  
- `scikit-learn` – Modeling, preprocessing, evaluation  
- `warnings` – Suppress warning messages

---

## 📊 Dataset Description

Competition: [House Prices – Advanced Regression Techniques](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques)

- `train.csv`: Training data, includes features + target column `SalePrice`
- `test.csv`: Test data without target, used for submission
- `sample_submission.csv`: Format required for Kaggle submission

---

## 🔁 Workflow Summary

The `task.ipynb` notebook implements the following steps:

### 1. 📥 Data Loading & Cleaning
- Loaded training and test datasets using `pandas`.
- Dropped columns with high missing values:
  - `'MiscFeature'`, `'Alley'`, `'Fence'`, `'MasVnrType'`, `'FireplaceQu'`, `'PoolQC'`
- Filled missing values:
  - Fixed values (e.g. `LotFrontage = 60`, `GarageYrBlt = 2005`)
  - Categorical values (e.g. `'GarageCond' = 'TA'`, `'GarageFinish'` = random from valid categories)
- Used `LabelEncoder` for categorical encoding (`object` type columns)


### 2. 🧠 Modeling & Tuning

| Model                  | Tuning Method         | Output File       |
|------------------------|-----------------------|-------------------|
| `LinearRegression`     | None                  | `submission.csv`  |
| `SGDRegressor`         | Pipeline + GridSearchCV | `submission1.csv` |
| `RandomForestRegressor`| Default parameters    | `submission2.csv` |


### 3. 📤 Prediction & Submission

Final predictions were made on the test dataset and saved as:

- `submission.csv` → from Linear Regression  
- `submission1.csv` → from SGD Regressor  
- `submission2.csv` → from Random Forest Regressor

---


## 📈 Next Improvements

- Feature engineering: polynomial features, interaction terms  
- Log transformation of skewed data  
- Model ensembling (stacking or blending)  
- Outlier removal for improved model robustness

---

## ⚙️ Installation

To install required libraries:


