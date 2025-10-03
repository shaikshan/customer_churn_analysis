# Customer Churn Prediction & Recommendation Prototype

Problem: Identify customers at risk of churn and recommend retention offers.

Approach:
- Data cleaning & EDA (tenure buckets, monthly charges quartiles, contract-level churn).
- Feature engineering: avg_monthly_charge, services_count, tenure buckets.
- Models: Logistic Regression and Random Forest (class_weight balanced).
- Recommendation prototype: rule-based prioritizing heavy-data, long-tenure+churn_prob, low-usage.

Key insights (example to paste after running):
1. Short-tenure (0-3 months) customers show the highest churn.
2. Month-to-month contract customers have higher churn than long-term contracts.
3. Higher monthly charges show some association with churn—cost sensitivity.

Model results (paste actual numbers after evaluation).
Recommended model: Random Forest if it shows higher recall/AUC (preferred to capture churners); else Logistic Regression for interpretability.

Recommendation logic:
- Heavy data -> Upgrade to Unlimited Data Plan
- Long tenure & high churn_prob -> 10% loyalty discount
- Low usage -> Switch to basic plan
- Default -> Free 1-month add-on or personalized discount
