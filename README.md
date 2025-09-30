# Fantasy Football Running Back Projection

This project explores the use of machine learning to predict fantasy football running back performance based on historical player stats.  
The goal is to compare model-generated projections against ESPN’s preseason rankings and highlight both the strengths and limitations of using data-driven approaches in fantasy football.

---

## Project Overview
- **Objective**: Predict non-rookie, standard scoring (non-PPR) running back rankings.  
- **Dataset**: Kaggle dataset + ESPN preseason rankings.  
- **Methods**:
  - Feature engineering with lagged stats (e.g., previous year’s fantasy points, touches, rolling averages).
  - Model training with Linear Regression and Random Forest.
  - Comparison of model predictions vs. ESPN projections.
  - Styled tables and visualizations to evaluate results.

---

## Features
- **Data Cleaning & Preparation**
  - Processed yearly player stats (fantasy points, rush attempts, receptions, touches).
  - Engineered lag features (previous season stats, rolling averages, missed games).
  - Added player info such as age, years in league, and rookie status.
- **Machine Learning**
  - Trained and compared Linear Regression and Random Forest models.
  - Evaluated accuracy using RMSE and MAE.
- **Visualization**
  - Built styled tables comparing model predictions with ESPN preseason projections.
  - Highlighted players who appeared under- or over-valued relative to projections.

---

## Results
- Both Linear Regression and Random Forest achieved similar performance.  
- The models captured general trends but struggled with:
  - Rookies - no prior data makes them inherently unpredictable.
  - Context-driven outcomes - injuries, coaching schemes, offensive line quality, etc., which were not in the dataset.
  - ESPN has insider knowledge on both of these things, and their data was more accurate in both 2023 and 2024 predictions.

---

## Limitations
Predicting fantasy football is inherently challenging:
- Non-linear, context-driven outcomes – Team scheme, game script, injuries, and competition at the position all affect outcomes but aren’t captured in the dataset.  
- Limited sample size – Only a few hundred RB seasons are available, which makes complex models prone to overfitting.

Here is an example of what the table comparison looks like for 2024:

<img width="581" height="665" alt="Screenshot 2025-09-29 201725" src="https://github.com/user-attachments/assets/3602f430-ed99-40a7-8d41-3f4ff7e3dd6c" />
