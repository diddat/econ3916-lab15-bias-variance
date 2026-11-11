# econ3916-lab15-bias-variance
# The Bias-Variance Tradeoff: Choosing How Flexible a Model Should Be

## Objective
The objective of this lab was to understand how model complexity affects prediction error and how cross-validation can help select a model that performs well on new data.

## Methodology
- Generated simulated nonlinear data with a known true relationship.
- Fitted polynomial regression models with different degrees of complexity.
- Calculated bias squared and variance using 200 different samples.
- Compared training error and held-out error using 2,000 test observations.
- Used 5-fold cross-validation to select the best polynomial degree.
- Applied nested cross-validation to evaluate the model selection process.
- Created a Python function called `kfold_mse()` to calculate cross-validation error for any polynomial degree and number of folds.

## Key Findings
- Bias squared decreased as polynomial degree increased because more flexible models could better approximate the true relationship.
- Variance increased from 0.0180 at degree 5 to 0.0994 at degree 15.
- Training error continued to decrease as model complexity increased, but held-out error was lowest at degree 5.
- 5-fold cross-validation selected degree 4 with a CV MSE of 0.1401.
- Nested cross-validation produced an estimated MSE of 0.2070, showing that the smallest regular CV error can be overly optimistic.
- 10-fold cross-validation produced an MSE of 0.1409 for degree 4 and 0.1457 for degree 5.
- Both 5-fold and 10-fold cross-validation preferred degree 4.

## Conclusion
This lab showed me that more complex models do not always make better predictions. While increasing polynomial degree reduces training error, it can also lead to overfitting and higher prediction error on new data. Cross-validation helps balance model complexity and prediction accuracy.
