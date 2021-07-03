# Evaluation metric
This is a summary over evaluation metrics used in Machine Learning.

## Classification
- Accuracy: percentage of correct predictions
- Precision / Recall
  - Precision: percentage of correct predictions over **all predictions of the target**. Ex: precision of cancer test kit = percentage of real positive over all positive (predicted by the kit)
  - Recall: percentage of correct predicitions over **actual target values**. Ex: recall of cancer test kit = percentage of real positive (predicted by the kit) over all positive cases
- [ ] Log loss

## Regression
- Metrics mostly used in regression in general, and linear regression in particual:
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

## Clustering
- [ ] Silhouette coefficient