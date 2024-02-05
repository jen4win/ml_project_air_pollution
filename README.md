# ZINDI AIR POLLUTION CHALLENGE

Link to the challenge and data: [Air Pollution Challenge](https://zindi.africa/competitions/zindiweekendz-learning-urban-air-pollution-challenge/data
).


## Context and Objective
This challenge provides the contributors with data of different sources to predict the air quality by PM2.5 particulate matter concentration for different cities on a daily basis. PM2.5 are very harmful air pollutants and are usually measured by ground-based sensors. To overcome the need of these ground-based sensors, the challenge aims to get a precise prediction. Therefore, data of the Global Forecast System and the Sentinel 5P satellite of three months are included.

## Stacking of Heterogeneous Weak Learners and XGBoost
The final trained Model can be found in the `prediction_model` folder.
This repository contains an implementation of stacking, ensemble learning technique that combines the predictions of multiple base models (weak learners) to improve predictive performance. In this implementation, stacking is combined with XGBoost to create a robust predictive model. The stacking ensemble consists of three base estimators and one final estimator:

**Base Estimators:**\
Linear Regression\
K-Nearest Neighbors Regression\
Random Forest Regression

**Final Estimator:**\
XGBoost Regressor

**RMSE**\
The final evaluation metric is RMSE. In the `model_test` folder, we reached following RMSE:\
train: 30.77\
test: 31.93

## Usage
• The training of the model is in `main.ipynb`. \
• The submitted results of the models are saved in the `submission.csv`\
• For further visualisations of the data run `analyses_visualisation.ipynb`

**`Note`**: Ensure that the downloaded data from the challenge is stored in the data folder and create the necessary environment with installed requirements.

```bash
pyenv local 3.11.3
python -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```
## References
[Scikit-learn Documentation: StackingRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.StackingRegressor.html)\
[XGBoost Documentation](https://xgboost.readthedocs.io/en/stable/)

## Contributors
Marie Gondeck \
Jennifer Winkler\
Shashank Kumar