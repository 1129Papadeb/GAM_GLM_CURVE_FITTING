Curve-Fitting Project README
Project Overview
This project investigates curve-fitting models applied to two distinct datasets: Wine Quality (red and white variants) and Air Quality (UCI repository). The objective is to compare the performance of Generalized Linear Models (GLM) and Generalized Additive Models (GAM) in predicting a continuous response variable using relevant physicochemical or environmental predictors.

Datasets Included
Wine Quality - Red Wine

Source: Publicly available wine quality dataset

Response Variable: Wine quality rating (0-10 scale)

Predictors: Chemical and physicochemical attributes such as acidity, residual sugar, pH, alcohol content, etc.

Wine Quality - White Wine

Source: Same as red wine dataset but for white variants

Response Variable and Predictors analogous to red wine dataset

Air Quality (UCI Machine Learning Repository)

Source: UCI Air Quality dataset

Response Variable: Ozone sensor measurement (PT08_S5_O3)

Predictors: Environmental factors like temperature, relative humidity, CO concentration, NOx levels, etc.

Contains missing and invalid data values handled during preprocessing

Data Preprocessing
For Wine Quality datasets, missing data handling and data type validation were applied.

For Air Quality dataset, negative invalid sensor readings coded as -200 were replaced with NaN and removed.

Data was cleaned and prepared separately for each dataset to ensure consistency during modeling.

Exploratory data analysis and correlation checks were performed prior to modeling.

Modeling Approach
Both GLM and GAM models were fit using the same predictors and response for each dataset.

GAMs allow flexible, non-linear relationships through spline smoothing, while GLMs model linear effects.

Models were evaluated based on Root Mean Squared Error (RMSE) and visual diagnostics.

Side-by-side plots for observed vs predicted, residuals, and model diagnostics were generated to compare fits.

Key Findings
GAM consistently outperformed GLM in predictive accuracy measured by RMSE across datasets.

RMSE scales correspond to the natural variability and units of each dataset’s response variable.

Diagnostic plots indicate better fit and handling of non-linear relationships by GAM.

Data transformations and outlier handling were suggested to improve model robustness further.

Code Structure
data/: Folder contains original datasets (winequality-red.csv, winequality-white.csv, AirQualityUCI.csv)

notebooks/: Jupyter notebooks with data cleaning, modeling, and visualization code for both datasets

scripts/: Python scripts implementing GLM and GAM fitting with plotting functions for diagnostics

outputs/: Generated figures and evaluation metrics for model comparisons

How to Run
Install required Python libraries: pandas, numpy, matplotlib, seaborn, statsmodels, scikit-learn, pygam

Ensure dataset CSVs are placed inside the data/ directory.

Run the notebooks or scripts to reproduce data cleaning, model fitting, and plotting workflows.

Review output visualizations and summary metrics in outputs/.

Future Work
Incorporate cross-validation and hyperparameter tuning for GAM smoothness

Extend modeling to classification tasks for wine quality categories

Experiment with other non-linear models like random forests or gradient boosting

Automate preprocessing pipelines for scalability

Acknowledgments
Wine Quality datasets sourced from UCI Machine Learning repository

Air Quality dataset sourced from UCI Machine Learning repository

Models utilize open-source Python libraries: Statsmodels, PyGAM, scikit-learn, pandas, seaborn