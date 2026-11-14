# MediBuddy Insurance Charges Analysis

## Project overview
This project analyzes recorded insurance charges across age, BMI, sex, smoking status, region, and number of children. It also compares regression models that predict charges.

## Data
The two assignment workbooks contain 1,338 policy records. They are joined on `Policy no.` and checked for missing values and duplicate policy numbers.

The workbooks are not included in this public repository. Download them from the course materials and place them in a local `data` folder beside the notebook:

- `Medibuddy insurance data personal details (1) (2).xlsx`
- `Medibuddy Insurance Data Price (1) (2).xlsx`

## Findings
- Mean recorded charge: ₹13,270.42; median: ₹9,382.03.
- Smoking status showed a strong difference in charge distributions (Mann–Whitney p < 0.001).
- The gender (p = 0.729) and regional (p = 0.192) tests did not show clear distribution differences.
- Charges generally increased across age groups. The BMI 30+ group had the highest average charge.
- The BMI and smoking comparison showed especially high charges among smokers with BMI 30+; the smallest BMI group had very few smokers.

These are associations in this dataset, not evidence of causation or a basis by themselves for setting policy terms.

## Model results
An 80/20 train/test split and five-fold cross-validation were used. The tuned Random Forest had a cross-validation MAE of ₹2,505.88. On the held-out test set, it achieved MAE ₹2,388.31, RMSE ₹4,401.78, and R² 0.864. A log-linear model had cross-validation MAE ₹4,242.21.

## Run the notebook
Install the required packages:

`pip install pandas openpyxl numpy scipy scikit-learn matplotlib seaborn jupyter`

Open `MediBuddy_Insurance_Analysis (1).ipynb` in Jupyter. The notebook reads the two workbooks from the local `data` folder.
