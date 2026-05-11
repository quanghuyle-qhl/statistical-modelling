# Statistical Modelling for Business Decision-Making
## Project Overview  
**Tools:** Microsoft Excel (Regression, Logistic Regression, Time-Series Modelling)  

**Skills:** Multiple Linear Regression, Logistic Regression, Interaction Effects, Time-Series Forecasting, Model Diagnostics

**Author:** Quang Huy Le
 
This project was completed as lead modeller for Methods9, a simulated analytics consultancy. Five models were developed across five client engagements, each addressing a distinct business problem using appropriate statistical techniques, rigorous model-building processes, and actionable recommendations.
## Models Built
### 1. GroceryPlus — Sales Revenue Prediction (Multiple Linear Regression)
 
**Problem:** Estimate sales revenue for a GroceryPlus store from operational variables.
 
**Approach:** Correlation matrix and scatter plots used to identify predictors and multicollinearity. Insignificant predictors removed iteratively via t-tests across multiple model iterations.
 
**Final Model — 4 Predictors:**
| Predictor | Coefficient | Interpretation |
|---|---|---|
| Wages | 2.15 | +$2.15M revenue per unit increase |
| Advertising Expense | 0.03 | +$0.03M revenue per unit increase |
| Car Spaces | 0.02 | +$0.02M revenue per unit increase |
| Home Delivery | 1.51 | +$1.51M revenue per delivery unit |
 
**Performance:** R² = 0.80, Adjusted R² = 0.79 — strong explanatory power.
  
### 2. BikeMart — Advertising and Promotion Interaction Effect
 
**Problem:** Test whether the number of promotional campaigns moderates the relationship between advertising expenditure and sales.
 
**Approach:** Regression model with interaction term (Advertising × Promotions).
 
**Key Findings:**
- Advertising Spend (coef: 2.52, p=0.02): significant positive effect on sales.
- Promotions alone (coef: -812.98, p=0.12): not independently significant.
- Interaction Term (coef: 2.38, p<0.001): significant — promotions amplify the effect of advertising.
**R² = 0.90** — strong model fit.
 
**Recommendation:** Increase advertising and promotional budgets together for compounding revenue gains; high advertising paired with high promotions generates the strongest returns.
 
### 3. Gadget4U — Headphone Purchase Prediction (Logistic Regression)
 
**Problem:** Predict whether a customer will buy headphones after purchasing a mobile phone.
 
**Final Model — 2 Predictors (after 6 iterations):**
- Annual Income (exp(b) = 0.99): each unit increase decreases purchase odds by 1%.
- Previous Purchases (exp(b) = 1.25): each additional purchase increases odds by 25%.
**Performance:** Overall accuracy 72%, AUC = 0.68. Model is better at predicting non-events; limited sensitivity for positive cases.
 
**Limitation:** Low R² (6–11%) suggests the model does not fully capture customer behaviour. Additional predictors recommended.
 
### 4. CosmeticChain — Store Manager Resignation Prediction (Logistic Regression)
 
**Problem:** Predict the likelihood of a store manager resigning based on age, experience, and gender.
 
**Final Model — 3 Predictors (all significant):**
| Predictor | exp(b) | Interpretation |
|---|---|---|
| Age | 0.88 | Each year older reduces resignation odds by 12.12% |
| Experience | 1.46 | Each year experience increases resignation odds by 45.65% |
| Gender (Male) | 0.38 | Male managers have 62.08% higher odds of resigning than female |
 
**Performance:** Overall accuracy 77%, AUC = 0.86 — good model fit.
 
**Recommendation:** Implement targeted retention strategies for experienced and male managers, including career development programs, mentoring, and improved work-life balance.
 
### 5. MoonlightAle — Pale Ale Production Forecasting (Time-Series)
 
**Problem:** Forecast quarterly Pale Ale production volumes for the next four quarters.
 
**Approach:** Multiplicative time-series model capturing trend and seasonal components (cyclical excluded due to absence of multi-year cycles).
 
**Seasonal Indices:**
- Q1: 3.5% below annual average
- Q2: 3.0% below annual average
- Q3: 18.3% above annual average (peak demand)
- Q4: 11.8% below annual average
**Forecasts:**
| Quarter | Forecast (Litres) |
|---|---|
| 2024-Q2 | 2,073.53 |
| 2024-Q3 | 2,553.60 |
| 2024-Q4 | 1,921.03 |
| 2025-Q1 | 2,121.57 |
 
**Performance:** MAPE = 3.66% — high accuracy and reliability.
## Key Takeaways
 
- Multiple regression with iterative variable selection produces parsimonious, interpretable models.
- Interaction effects reveal that advertising and promotions work best together — a finding invisible to additive models.
- Logistic regression effectively quantifies resignation risk, enabling targeted HR interventions.
- Multiplicative time-series models accurately capture seasonal production patterns with low forecasting error.
