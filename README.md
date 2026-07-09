# Machine Learning Project-Boston House Price Prediction
An end-to-end regression modeling project predicting real estate valuations with advanced outlier preprocessing

Key Modeling Methodology

1. **Preprocessing & Feature Engineering:**
   * Target variable log-transformation (`MEDV` $\rightarrow$ `MEDV_log`) to normalize target distribution and stabilize variance.
   * Multicollinearity mitigation via correlation analysis and stepwise removal of redundant features (`ZN`, `AGE`, `INDUS`, `TAX`).

2. **Diagnostic & Assumption Checks:**
   * **Normality of Residuals:** Evaluated via residual histograms and Q-Q plots.
   * **Homoscedasticity:** Verified through residual vs. fitted value plots and Goldfeld-Quandt testing.
   * **Linearity:** Confirmed linear relationships between predictors and the log-transformed target.

3. **Validation & Performance:**
   * **10-Fold Cross-Validation:** $R^2 = 0.729 \pm 0.232$, $\text{MSE} = 0.041 \pm 0.023$.
   * Evaluated model generalization using out-of-sample test data (`RMSE`, `MAE`, `MAPE`).
