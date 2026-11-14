# MediBuddy Insurance Charges Analysis

## Project overview
This project explores recorded insurance charges by age, BMI, sex, smoking status, region, and number of children. It also compares models for predicting charges.

## Data
The two course workbooks contain 1,338 policies and are joined using `Policy no.`. They are not included in this public repository. Download them from the course resources and place them in a local `data` folder beside the notebook.

## Results

| Model | Evaluation | MAE (INR) | RMSE (INR) | R-squared |
|---|---|---:|---:|---:|
| Mean baseline | 5-fold cross-validation | 9,119.43 | — | — |
| Log-linear regression | 5-fold cross-validation | 4,242.21 | — | — |
| Tuned Random Forest | 5-fold cross-validation | 2,505.88 | — | — |
| Tuned Random Forest | Held-out test set | 2,388.31 | 4,401.78 | 0.864 |

The residual plot shows that the model underpredicts some high-charge cases.

## Findings
Smoking status showed a strong difference in charges (Mann–Whitney p < 0.001). The gender test (p = 0.729) and region test (p = 0.192) did not show clear differences. Charges generally rose across age groups. Smokers in the BMI 30+ group had especially high average charges, but this is an association, not proof of cause.

## Run the notebook
Install packages with `pip install -r requirements.txt`, then start Jupyter and open `MediBuddy_Insurance_Analysis (1).ipynb`. Keep both course workbooks in the local `data` folder.
