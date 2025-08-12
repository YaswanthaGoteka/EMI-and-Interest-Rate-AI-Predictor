# EMI-and-Interest-Rate-AI-Predictor
This script loads and cleans loan data, encodes categorical fields, and trains two models: an XGBoost regressor to predict monthly EMI, interest rate, and loan term, and a Random Forest classifier to predict loan approval. It evaluates performance and lets users input details to get real-time loan predictions and approval probability.

Dataset (.csv):
- Arif Miah · Personal Finance ML Dataset from Kaggle

Imports:
- pandas (read data)
- LabelEncoder (encode data to train)
- train_test_split (training and testing model)
- RandomForestClassifier (Model used to predict EMI, Interest Rate, and Loan Term)
- mean_squared_error, r2_score, mean_absolute_error, accuracy_score (evaluation methods to test accurcy of model)
- XGBRegressor
- MultiOutputRegressor

## Example Output:

~~~
📈 Regression Model Evaluation:
🔹 MSE: 0.42
🔹 R²: 0.91
🔹 MAE: 0.15
✅ Estimated Accuracy: 97.05%

📊 Classification Model Evaluation:
✅ Accuracy: 100%

--- Enter Loan Application Details ---
age (['18-25', '26-35', '36-45', '46-55', '56+']): 34
gender (['Female', 'Male', 'Other']): male
education_level (['High School', 'Bachelor', 'Master', 'PhD', 'Unknown']): bachelor
employment_status (['Employed', 'Self-employed', 'Student', 'Unemployed', 'Unknown']): employed
job_title (['Engineer', 'Manager', 'Accountant', 'Driver', 'Doctor', 'Unknown']): engineer
monthly_income_usd: 5500
monthly_expenses_usd: 2000
savings_usd: 15000
loan_type (['Personal', 'Mortgage', 'Auto', 'Education', 'Unknown']): personal
loan_amount_usd: 15000
credit_score: 720
region (['North', 'South', 'East', 'West', 'Unknown']): north

📌 Predicted Loan Details:
💵 Monthly EMI: $1921.05
📈 Interest Rate: 17.64%
📅 Loan Term: 36 months
✅ Approval Probability: 97.67%
~~~


## This is a fined a model from scratch.
## Proof:Training from scratch means you initialize a model with 
## random weights (or a fresh, untrained instance) and train it entirely 
## on your dataset from the beginning. No prior knowledge is used.

## I created most of this with my own knowledge but I also used AI (ChatGPT) 
## to debug and make it better like adding 
## the Approval Probability for the output. Otherwise I have done everything Myself :) 
