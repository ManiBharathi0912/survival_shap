# Interpretable AI: SHAP Analysis of a Survival Model (Haberman, Colab + Drive)

## Data
- Source: Haberman's Survival Dataset (breast cancer post-surgery).
- CSV loaded from Google Drive: /content/drive/MyDrive/haberman.csv
- Targets: event from Survival_status (2=event, 1=censored); time simulated respecting 5-year cutoff.

## Models and metrics
- CoxPH: Harrell's C-index = 0.604; Integrated Brier Score = 0.138; Mean Brier (quartiles) = 0.145
- XGBoost (survival:cox): Harrell's C-index = 0.602

## SHAP global importance
1. Age: Increasing values associate with lower predicted risk (SHAP trend).
2. Year: Increasing values associate with lower predicted risk (SHAP trend).
3. Nodes: Increasing values associate with higher predicted risk (SHAP trend).

## Artifacts
- SHAP summary: shap_summary.png
- SHAP dependence: shap_dependence_*.png (Age, Year, Nodes)
- Force plots: force_low_risk.html, force_high_risk.html
- Metrics: metrics.json

## Notes
- CoxPH used for robust survival metrics; XGBoost used for SHAP explanations of risk scores.
