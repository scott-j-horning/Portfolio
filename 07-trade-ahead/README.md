# EasyVisa — OFLC case-status classification

Ensemble classification of Office of Foreign Labor Certification (OFLC) visa applications.  
Target: `case_status` (Certified / Denied).

## Approach
- Exploratory data analysis and preprocessing
- Bagging: Decision Tree, Bagging Classifier, Random Forest
- Boosting: AdaBoost, Gradient Boosting (XGBoost optional)
- Hyperparameter tuning and stacking
- Feature importance and actionable recommendations

## Key drivers
- `education_of_employee` (High School is the strongest negative signal)
- `has_job_experience`
- `prevailing_wage`

## Result
Strongest single models (base Gradient Boosting, base AdaBoost, tuned Random Forest) reach test F1 ≈ 0.82.  
Stacking ties these models. A single Gradient Boosting model is sufficient for deployment.

Dataset omitted from this repository.