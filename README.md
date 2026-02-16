# Housing Total Price Prediction

## Project Overview
This project performs **Linear Regression** on a housing/construction dataset to predict the `total_price` of houses. The dataset contains numeric and categorical features related to construction, location, and house specifications.
The goal is to demonstrate **data preprocessing, exploratory data analysis (EDA), and predictive modeling** using Python and scikit-learn.
## Dataset
- **Features**: `location`, `land_area_sqft`, `floors`, `bedrooms`, `bathrooms`, `windows`, `doors`, `cement_bags`, `rcc_structure`, `plumbing`, `electricity`, `land_cost`, `construction_cost`, `material_cost`
- **Target**: `total_price`
- **Number of rows**
- **Data types**: Mostly numeric, with `location` categorical

## Exploratory Data Analysis (EDA)
- Checked for missing values: ✅ None
- Converted `location` column to numeric using **one-hot encoding** (`pd.get_dummies`)
- Visualized distribution of `total_price` (histogram)
- Analyzed correlation among features (heatmap)
- Observed that `total_price` strongly correlates with cost-related features (`land_cost`, `construction_cost`, `material_cost`)

---

## Preprocessing
- Separated features (`X`) and target (`y`)
- Encoded categorical columns
- Split data into **train (80%)** and **test (20%)** sets using `train_test_split`
- No scaling required for Linear Regression in this dataset

## Model
- Model used: **Linear Regression**
- Train R² Score: `1.0`
- Test R² Score: `1.0`
- Observations:
  - Perfect prediction because `total_price` is directly derived from cost columns
  - For realistic prediction, cost columns could be excluded to predict based on house specifications

