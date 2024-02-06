# ZINDI AIR POLLUTION CHALLENGE

Link to the challenge and data: [Air Pollution Challenge](https://zindi.africa/competitions/zindiweekendz-learning-urban-air-pollution-challenge/data
).


## Context and Objective
This challenge provides the contributors with data of different sources to predict the air quality by PM2.5 particulate matter concentration for different cities on a daily basis. PM2.5 are very harmful air pollutants and are usually measured by ground-based sensors. To overcome the need of these ground-based sensors, the challenge aims to get a precise prediction. Therefore, data of the Global Forecast System and the Sentinel 5P satellite of three months are included.

## Stacking of Heterogeneous Weak Learners and XGBoost
The two final trained models can be found in the `my_model` folder.
This repository contains an implementation of stacking, ensemble learning technique that combines the predictions of multiple base models (weak learners) to improve predictive performance. In this implementation, stacking is combined with RandomForest to create a robust predictive model. The stacking ensemble consists of three base estimators and one final estimator:

**Base Estimators:**\
Ridge Regression\
K-Nearest Neighbors Regression\
Random Forest Regression

**Final Estimator:**\
Random Forest Regression

**RMSE**\
The final evaluation metric is RMSE. In the first attempt to model this relationship just with a single Random Forest, we achieved the following RMSE:\
train: 15.57\
test: 31.04

## Usage
• The training of the model is in `main.ipynb`. \
• The submitted results of the models are saved in the `submission.csv` and `submission_stacked.csv`\
• For further visualisations of the data have a look at the bottom of `main.ipynb`

**`Note`**: Ensure that the downloaded data from the challenge is stored in the data folder and create the necessary environment with installed requirements.

```bash
pyenv local 3.11.3
python -m venv .venv
source .venv/Scripts/activate
pip install --upgrade pip
pip install -r requirements.txt
```
## References
[Scikit-learn Documentation: StackingRegressor](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.StackingRegressor.html)\

## Contributors
Jennifer Winkler\
Marie Gondeck \
Shashank Kumar