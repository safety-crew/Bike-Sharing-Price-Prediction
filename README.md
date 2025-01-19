# Short Report
#### Key Findings from Exploratory Data Analysis (EDA):
1. The target variable, `count` (total bike rentals), exhibits a right-skewed distribution, indicating that most instances involve fewer bike rentals, with some high-rental outliers.
2. Bike rentals peak during commuting hours (8 AM and 5-6 PM), highlighting rush hour patterns. Rentals are also higher in summer and fall compared to winter.
3. Correlation analysis revealed that:
   - `count` is strongly positively correlated with `registered` users (0.97) and temperature (`temp` and `atemp`).
   - There is a moderate negative correlation with `humidity` (-0.32) and a weaker correlation with `windspeed`.

#### Feature Engineering:
A new binary feature, `rush_hour`, was introduced to capture the impact of peak commuting times (7-9 AM and 4-7 PM) on bike rentals. This feature showed a significant relationship with `count`, as rentals were consistently higher during rush hours. Including this feature improved the model's ability to capture temporal trends in the data.

#### Model Performance:
1. **Metrics**:
   - Mean Absolute Error (MAE): 94.55
   - Root Mean Square Error (RMSE): 127.96
   - R² Score: 0.504

The R² score indicates that the model explains approximately 50.4% of the variance in the target variable. While the model captures general trends in bike rentals, there is room for improvement, particularly in predicting extreme rental counts.

2. **Residuals Analysis**:
   - Residuals are approximately centered around zero, with a slight skewness, indicating variability in prediction accuracy.
   - The model performs moderately well but struggles with extreme cases, as evidenced by the dispersion of residuals and deviations from the diagonal line in the actual vs. predicted scatter plot.

#### Conclusion:
The linear regression model provides a baseline for predicting bike rentals, capturing general trends influenced by temperature, rush hours, and other features. However, the model’s performance indicates potential benefits from further feature engineering and exploration of non-linear methods to enhance prediction accuracy.
