📊 Customer Churn Prediction
This project aims to analyze customer churn in a telecommunications company and build predictive models to identify customers who are at risk of leaving the service. The final goal is to generate actionable insights and improve customer retention.

📁 Dataset
Name: Telco_Customer_Churn_Dataset.csv

Description: Contains information about telecom customers including services they use, account information, demographics, and whether they have churned.

Target Variable: Churn (Yes/No)

✅ Tasks Breakdown
🔹 Task 1: Data Loading & Initial Inspection
Loaded the CSV file using pandas.

Checked for null values and data types.

Displayed the top rows to understand the structure of the dataset.

🔹 Task 2: Data Preprocessing
Replaced blank strings and NaN values.

Converted TotalCharges to numeric.

Dropped irrelevant columns like customerID.

Handled null values (e.g., in TotalCharges).

Converted all categorical variables into numerical using:

Label Encoding (for binary columns)

OneHotEncoding (for multiclass categorical columns)

🔹 Task 3: Exploratory Data Analysis (EDA)
Visualized distributions of target and input features.

Checked class imbalance in the target (Churn).

Analyzed correlation between numerical variables.

Generated sample graphs and included dataset images in the report.

🔹 Task 4: Feature Selection
Used SelectKBest and chi2 to select top features influencing churn.

Reduced dimensionality to prevent overfitting.

🔹 Task 5: Train-Test Split
Used train_test_split from sklearn to divide data:

python
Copy code
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, stratify=y, random_state=42
)
🔹 Task 6: Model Building
Used RandomForestClassifier as the primary model:

python
Copy code
from sklearn.ensemble import RandomForestClassifier
rf_model = RandomForestClassifier(n_estimators=100, random_state=42)
rf_model.fit(X_train, y_train)
🔹 Task 7: Evaluation
Evaluated using:

Accuracy

Precision

Recall

F1 Score

ROC-AUC Score

Sample results:

yaml
Copy code
✅ Evaluation Results:
Accuracy: 0.7587
Precision: 0.5541
Recall: 0.4652
F1 Score: 0.5058
ROC-AUC Score: 0.7848

📄 Classification Report:
              precision    recall  f1-score   support
          0       0.82      0.86      0.84      1035
          1       0.55      0.47      0.51       374
📝 Final Report
A complete Word document is generated summarizing:

Project overview

Data insights

Preprocessing steps

Feature selection

Model building and evaluation

Dataset snippets and plots
