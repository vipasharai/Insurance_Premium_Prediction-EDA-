# Medical Insurance Cost Prediction (End-to-End ML Pipeline)

## Business Objective
The objective of this project is to accurately predict the medical insurance costs of individuals based on their health and demographic profile (Age, BMI, Smoking status, Region, etc.). 

## Technologies Used
* **Python** (Pandas, NumPy)
* **Data Visualization** (Matplotlib, Seaborn)
* **Machine Learning** (Scikit-Learn, Linear Regression)
* **MLOps** (Scikit-Learn Pipelines, ColumnTransformer)

## Key Findings (Exploratory Data Analysis)
* **Smoking is the primary cost driver:** Smokers are billed significantly higher than non-smokers, regardless of age.
* **Age vs. Charges:** Insurance costs increase predictably with age, forming three distinct "cost tiers" based on the combination of age, BMI, and smoking status.
* **BMI impact:** High BMI (Obesity) drastically multiplies medical costs, but *only* if the patient is also a smoker. 

## Model Architecture
To prevent data leakage and ensure the model can be deployed into production, a robust Scikit-Learn `Pipeline` was constructed:
1. **Numerical Data:** Handled using `StandardScaler`.
2. **Categorical Data:** Handled using `OneHotEncoder` (dropping the first column to avoid the dummy variable trap).
3. **Algorithm:** `LinearRegression`.

## Results
* **R-Squared ($R^2$):** [0.8019]
* **Mean Absolute Error (MAE):** $[$4,369.76]
<img width="713" height="545" alt="download" src="https://github.com/user-attachments/assets/fa52c3d4-5743-4ee6-ae92-6eee3aa8cc1b" />

<img width="589" height="432" alt="download" src="https://github.com/user-attachments/assets/a8318071-99f4-4891-9d5b-e6f16368dc98" />
<img width="868" height="545" alt="download" src="https://github.com/user-attachments/assets/26f9d1ab-afd5-4c3a-96b9-af9bd3f05840" />
<img width="850" height="545" alt="download" src="https://github.com/user-attachments/assets/4adf7f1a-b6da-45f5-bebd-459de7166513" />
<img width="625" height="526" alt="download" src="https://github.com/user-attachments/assets/ad06dc58-6295-4aad-8b23-93db92f90a29" />




