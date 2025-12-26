README (cho GitHub / Portfolio / Kaggle)
Project Title: Car Price Prediction and Key Determinants in the U.S. Market

Objective
  This project aims to help Geely Auto, a Chinese automobile company, understand the key factors influencing car prices in the U.S. market and build a predictive model to estimate car prices based on technical   specifications.

Dataset Overview

  Total records: 205
  Features: 15 numerical, several categorical
  Target: price
  Source: Automobile dataset (UCI repository / Kaggle version)

Data Preprocessing
  Checked and handled missing & duplicated values
  Detected and treated outliers using IQR method
  Encoded categorical variables and scaled numerical ones
  Selected relevant features with strong correlation to price:
  wheelbase, carlength, carwidth, curbweight, enginesize, horsepower

Exploratory Data Analysis (EDA)
  Price distribution is right-skewed with several outliers (luxury cars).
  Larger vehicles (greater width, wheelbase, and length) tend to have higher prices.
  Fuel efficiency (citympg, highwaympg) is negatively correlated with price.
  Most cars are gas-powered, front-wheel drive, and 4-cylinder engines.
Model Selection
Models used:
  Linear Regression
  Random Forest Regressor
  XGBoost Regressor
  LightGBM Regressor
  Gradient Boosting Regressor
  CatBoost Regressor

Training split: 80% train / 20% test

Model Evaluation (Before Tuning)
Model	R²	RMSE
Linear Regression	0.820	3774
Random Forest	0.952	1951
XGBoost	0.931	2336
CatBoost	0.934	2287
Gradient Boosting	0.906	2722
LightGBM	0.808	3897

Best Model: Random Forest Regressor — R² = 0.952, lowest error and highest stability.

After Hyperparameter Tuning

Random Forest maintained strong performance (R² = 0.945).
Gradient Boosting improved significantly (R² = 0.938).
CatBoost became a strong competitor with R² = 0.940.

Feature Importance
Top factors affecting car price:
Enginesize — 60% importance
Curbweight — 30% importance
Horsepower, Wheelbase, Carlength, Carwidth — minor contributors

Engine performance and vehicle weight are the strongest predictors of car price.

Key Insights
Larger, heavier cars with bigger engines cost more.
Fuel-efficient and compact vehicles are in lower price ranges.
Tree-based ensemble models outperform linear models on this dataset.
Conclusion
  Random Forest Regressor delivers the most accurate and reliable car price predictions.
  Gradient Boosting and CatBoost are strong alternatives with excellent generalization.
  The findings help identify core specifications that drive vehicle pricing decisions.
Tools & Libraries
Python, Pandas, NumPy, Matplotlib, Seaborn

Scikit-learn, XGBoost, CatBoost, LightGBM
