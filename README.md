# Curve-Fitting Project

## Project Overview
This project investigates curve-fitting models applied to two distinct datasets: Wine Quality (red and white variants) and Air Quality (UCI repository). The objective is to compare the performance of Generalized Linear Models (GLM) and Generalized Additive Models (GAM) in predicting a continuous response variable using relevant physicochemical or environmental predictors.

## Datasets Included
1. **Wine Quality - Red Wine**  
   - Source: [Red Wine Quality Dataset (Kaggle)](https://www.kaggle.com/datasets/uciml/red-wine-quality-cortez-et-al-2009)  
   - Response Variable: Wine quality rating (0-10 scale)  
   - Predictors: Chemical and physicochemical attributes such as acidity, residual sugar, pH, alcohol content, etc.

2. **Wine Quality - White Wine**  
   - Source: Publicly available white wine quality dataset (similar structure to red wine)  
   - Response Variable and Predictors analogous to red wine dataset  

3. **Air Quality (UCI Machine Learning Repository)**  
   - Source: [UCI ML Air Quality Dataset (Kaggle)](https://www.kaggle.com/datasets/nishantbhadauria/datasetucimlairquality)  
   - Response Variable: Ozone sensor measurement (PT08_S5_O3)  
   - Predictors: Environmental factors like temperature, relative humidity, CO concentration, NOx levels, etc.  
   - Contains missing and invalid data values handled during preprocessing

## Data Preprocessing
- Missing and invalid values (e.g., -200 in Air Quality dataset) were replaced or removed.  
- Data cleaning and validation were performed separately for each dataset.  
- Exploratory data analysis was conducted to understand features and distributions.

## Modeling Approach
- GLM and GAM models were fit using identical predictors and response variables for each dataset.  
- GAM models allow non-linear relationships through spline smoothing and showed better fit.  
- Models were evaluated with Root Mean Squared Error (RMSE) and diagnostic plots.  
- Side-by-side plots for observed vs predicted, residuals, and diagnostics were used to compare performance.

## Results Summary
- GAM consistently outperformed GLM in predictive accuracy as reflected by lower RMSE values.  
- RMSE magnitudes reflect the natural variability and units of the response variables.  
- Diagnostic plots confirmed GAM’s superior ability to model complex relationships.

## References and Further Reading
- Air Quality Prediction Using Machine Learning [PDF](https://www.researchgate.net/publication/394490744_Air_Quality_Prediction_Using_Machine_Learning)  
- Machine learning-based predictive modelling for the enhancement of wine quality | Scientific Reports  
  (https://www.nature.com/articles/s41598-023-44111-9#data-availability)

## Project Structure
- `data/`: Contains original datasets  
- `notebooks/`: Jupyter notebooks for data cleaning, modeling, and visualization  
- `scripts/`: Python scripts implementing GLM and GAM with diagnostics  
- `outputs/`: Figures and evaluation results  

## Usage
1. Install required Python packages: pandas, numpy, matplotlib, seaborn, statsmodels, scikit-learn, pygam  
2. Place datasets in the `data/` folder.  
3. Run notebooks or scripts to reproduce analysis and figures.  
4. Review outputs in the `outputs/` folder.

## Future Work
- Include cross-validation and hyperparameter tuning  
- Extend to classification for wine quality categories  
- Experiment with other machine learning methods  

## License
Specify licensing here based on dataset and code use.

## Acknowledgments
- Wine Quality and Air Quality datasets: UCI Machine Learning Repository and Kaggle  
- Python packages: Statsmodels, PyGAM, scikit-learn, pandas, seaborn  
