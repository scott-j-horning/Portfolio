# ReneWind — Generator Failure Prediction

Predictive-maintenance classification for wind-turbine generators.  
Ciphered sensor data (V1–V40) + binary Target (1 = failure).

## Goal
Identify failures early enough that a repair can be performed instead of a full replacement.  
Cost order: False Negative (replacement) > True Positive (repair) > False Positive (inspection).

## Approach
- Custom cost-ratio metric (`Minimum_Vs_Model_cost`) used for model selection and tuning.
- Seven algorithms evaluated on original, SMOTE-oversampled, and randomly undersampled training data.
- Strongest models tuned with RandomizedSearchCV.
- Final model: tuned XGBoost.
- Production pipeline: median imputation + tuned XGBoost.

## Hold-out result (Test set)
- Minimum_Vs_Model_cost ≈ 0.77  
- Recall (failure class) ≈ 0.83  
- Maintenance cost ≈ 1.31× theoretical minimum.

## Top sensors
V18, V36, V39, V3, V26, V14.

## Files
- `notebook.ipynb` — full analysis
- Datasets omitted from this repository.