# Machine Learning steps

## Introduction
- Define the problem -> Build dataset -> Train model -> Evaluate model -> Use model

## Define the problem
- Define the problem in a way that ML algorithms can be applied
  - Unsupervised learning
    - clustering
    - ...
  - Supervised learning
    - Regression
    - Classification
    - ...
  - Reinforcement learning

## Build a dataset
1. Collect data: [Q] does the data match the ML task?
2. Inspect data: [Q] does it have outliers/missing values / right format? How to handle/preprocess?
3. Summary statistics: [Q] does data has a trait/trend? How is data structured/distributed (are the assumptions for model correct)? Min/max/mean/median?
4. Visualize data: [Q] how to visualize to raise data understanding / tell story?

## Model training
- Split dataset -> train + test + validation set
- Model parameters (or weights in DL) -> define how the model behave
- Loss function -> codify how close the model behaves as expected
- Many models have to be tested, selected and "mixed" to find the best solution

## Model evaluation
- Based on a metric
- Accuracy, log loss, F1 score, etc.
- Examples: some metrics for linear regression
  - MSE / RMSE (mean square error / root mean square error): 
    - MSE = $\frac{1}{N} * \sum_{i=0}^{N-1}{(y_{i} - f_{i})^{2}}$ 
    - RMSE = $\sqrt{MSE}$
  - MAE (mean absolute error): $\frac{1}{N} * \sum_{i=0}^{N-1}{|y_{i} - f_{i}|}$
  - $R^2$ / adjusted-$R^2$ (or coefficient determination): represents how well the regression fits the data
    - $R^2$ = $1 - \frac{(y_{i} - f_{i})^2}{(y_{i} - \bar{y})^2}$, with some cases specific:
      - $R^2 = 1$ => $y_{i} = f_{i}, \forall i$
      - $R^2 = 0$ => $f_{i} = \bar{y} \forall i$
    - adjusted-$R^2$ = 1 - $\frac{(y_{i} - f_{i})^2 / (N - p - 1)}{(y_{i} - \bar{y})^2 / (N - 1)}$, with p is the number of regressor (number of variables (x) in the regression). This helps to penalize independent variables.
  - When should we use each metric?
    - MSE / RMSE is more meaningful for defining how much our model is wrong. However, it's sensitive to outliers.
    - R-squared / adjusted R-squared gives results in percentage, and it can help to represent how well the model fits with the data. A R-squared too close to 1 may mean that our model is overfitting.
    - MAE is an easy to interpret metric. But it can not penalize large errors, ni show how well model fits.