# Insurance Charges: EDA & Prediction

Exploratory data analysis and a linear regression model to predict individual medical insurance charges from personal factors such as age, BMI, smoking status, number of children and region.

## Dataset
1,338 records (1,337 after removing one duplicate) with: `age`, `sex`, `bmi`, `children`, `smoker`, `region` and the target `charges`.

> Add `insurance.csv` to the repository (the dataset is the public "Medical Cost Personal" dataset on Kaggle).

## What I Did
1. **EDA:** distributions, count plots, boxplots (outlier check) and a correlation heatmap
2. **Cleaning & preprocessing:** removed duplicates, encoded `sex` and `smoker`, one-hot encoded `region`
3. **Feature engineering:** BMI categories (Underweight / Normal / Overweight / Obese), scaling of numeric features
4. **Feature selection:** Pearson correlation for numeric features and chi-square tests for categorical features
5. **Modelling:** Linear Regression with an 80/20 train-test split, evaluated with R² and adjusted R²

## Key Results
- **Smoking status is by far the strongest driver of charges** (correlation ≈ 0.79)
- Age (≈ 0.30) and obesity (≈ 0.20) are the next most related factors
- Linear Regression achieves an **R² of about 0.80** on the test set

## Tech Stack
Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, Scikit-learn, Jupyter Notebook


## How to Run
```bash
git clone https://github.com/Mustafabbas621/Insurance-Project
cd insurance-charges-prediction
pip install numpy pandas matplotlib seaborn scipy scikit-learn jupyter
jupyter notebook Insurance_Project.ipynb
```

## By Mustafa Abbas Ali
