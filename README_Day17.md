# Day 17 — Advanced Anomaly / Forecast Model

## Work completed
- Tested Gradient Boosting as a stronger, proportionate forecasting candidate against the Day 16 Random Forest baseline.
- Target: next-row pH using current and past sensor observations.
- Used chronological 70/15/15 train/validation/test split.
- Used training-fitted median imputation in sklearn pipelines.
- Selected candidate using validation RMSE and saved it as `candidate_forecast_model.joblib`.
- Saved metrics, chronological split, test predictions, and plots in `day17_outputs/`.

## Results
                      model  validation_MAE  validation_RMSE  test_MAE  test_RMSE
     Random Forest baseline        1.291703         1.611574  1.497310   1.910017
Gradient Boosting candidate        1.285784         1.601120  1.500746   1.920035

Selected candidate by validation RMSE: **Gradient Boosting candidate**.

## Important limitation
The input table is a static water-potability dataset with synthetic timestamps. These experiments validate code and workflow only; they do not establish real underwater sensor forecasting performance. The small dataset does not justify a deep sequence model yet.

## Run
Install `pandas numpy matplotlib scikit-learn joblib jupyter`, then open `Day17_Advanced_Forecast_Model.ipynb` in Jupyter/Colab. Keep the CSV in the same directory.
