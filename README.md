🏦 Walmart Weekly Sales Prediction
🌐 Context

Walmart Inc. is a multinational retail giant headquartered in Bentonville, Arkansas. With thousands of stores across the U.S., the company collects a vast amount of transactional and contextual data each week.
To support its marketing and planning efforts, Walmart's team requested a predictive model to estimate weekly sales per store, leveraging both internal and economic indicators.

📊 Business Objective

Build a machine learning model that accurately predicts weekly store sales, enabling Walmart to:

Improve marketing campaign targeting
Forecast demand more precisely
Identify the influence of economic and temporal factors


⚖️ Methodology

Part 1: Exploratory Data Analysis (EDA)

Dataset composed of 136 entries, representing different stores, economic context (CPI, Unemployment), and time variables (Year, Month).

Main features:

Store ID (categorical)
Holiday_Flag (categorical)
Temperature, CPI, Unemployment (numerical)
Year, Month (temporal, traités comme numériques)

Key insights from EDA:

Certain stores significantly outperform others (ex: Store 19)
Unemployment and CPI show moderate correlation with sales
Holidays tend to negatively affect sales in some stores

Part 2: Baseline Model - Linear Regression

Applied preprocessing:

OneHotEncoding for categorical variables
StandardScaler for numerical variables
SimpleImputer for missing values in Year and Month

Performance:

- R² Train: 0.967
- R² Test: 0.951
- RMSE Test: 158,956

✅ Interpretation: the baseline model already performs extremely well, thanks to relevant variables and a simple, interpretable structure.

Part 3: Regularized Models

Ridge (L2):
- R² Test: 0.949 | RMSE: 162,941
- Coefficients slightly shrunk compared to baseline, but no major change in ranking

Lasso (L1):
- R² Test: 0.947 | RMSE: 166,009
- Some features (like CPI or Year) forced close to zero → Lasso performs feature selection

🥇 Results & Business Value

All models confirm that Store ID is the strongest driver of weekly sales
Unemployment, Holiday_Flag, and Temperature are also relevant
With a test R² of 0.951, the baseline model offers reliable predictions

What Walmart Gains:

Better understanding of which stores perform best, and under what conditions
Tools to forecast future performance based on macroeconomic context
Opportunity to target marketing and promotions with more precision

🎓 Recommendation

Given the small dataset (136 observations), the linear regression model remains the best option: it avoids overfitting and is easy to interpret.

For future improvement:

Add features like store size, location type, or promotions
Use more historical data to train models with greater generalization
Explore ensemble methods once dataset size grows (Random Forest, XGBoost)

📈 Conclusion

This predictive model provides Walmart with a clear and actionable tool to understand what drives weekly sales. It also demonstrates how data science can translate business questions into measurable and reliable forecasts.