📉 **Customer Subscription Churn Prediction Using Usage Patterns**

📌 **Project Overview**
Customer churn is a major challenge for subscription-based businesses. Losing customers directly affects revenue, growth, and customer acquisition costs.
This project develops a Machine Learning model to predict whether a customer is likely to churn based on usage behavior, engagement patterns, and subscription details. The goal is to help businesses identify at-risk customers early and take preventive retention actions.

🎯 **Business Objective**
To build a predictive system that:
Identifies customers at high risk of churn


Explains the behavioral reasons behind churn


Supports data-driven customer retention strategies



📂 **Dataset Description**
The dataset includes customer usage and subscription-related features.
| Feature           | Description                                 | Business Relevance                 |
| ----------------- | ------------------------------------------- | ---------------------------------- |
| Usage Hours       | Total time spent on the platform            | Low usage indicates low engagement |
| Last Login Days   | Days since last login                       | High value shows disengagement     |
| Tenure            | Number of months as a customer              | New users churn more often         |
| Payment Failures  | Number of failed transactions               | Billing issues increase churn risk |
| Subscription Type | Type of plan chosen                         | Impacts commitment level           |
| Churn (Target)    | Whether the customer left (1) or stayed (0) | Prediction target                  |


⚙️ Machine Learning Workflow
1️⃣ Data Preprocessing
Data cleaning and validation


Feature selection based on business importance


Train-test split to evaluate model generalization


2️⃣ Model Building
Multiple supervised ML models are considered:
Logistic Regression (baseline model)


K-Nearest Neighbors (KNN)


Random Forest Classifier


3️⃣ Model Evaluation
Models are assessed using:
Accuracy


Precision


Recall


Confusion Matrix


These metrics help balance overall performance with the ability to correctly detect churners.

📈 Model Comparison
| Model               | Accuracy        | Precision | Recall   | Strengths                                         | Limitations                                |
| ------------------- | --------------- | --------- | -------- | ------------------------------------------------- | ------------------------------------------ |
| Logistic Regression | Moderate        | Good      | Moderate | Simple, interpretable baseline                    | Limited with complex non-linear patterns   |
| KNN                 | High (training) | Good      | Good     | Captures local data patterns                      | Sensitive to scaling, prone to overfitting |
| Random Forest       | High            | High      | High     | Handles non-linearity, robust, strong performance | Less interpretable, needs tuning           |


Final Model Choice: Random Forest due to strong ability to model complex customer behavior patterns.

🖼 Confusion Matrix Explanation


|                   | Predicted: Stay      | Predicted: Churn     |
| ----------------- | -------------------- | -------------------- |
| **Actual: Stay**  | True Negatives (TN)  | False Positives (FP) |
| **Actual: Churn** | False Negatives (FN) | True Positives (TP)  |

Business Meaning
True Positives (TP): Correctly identified churners → retention actions possible


True Negatives (TN): Correctly identified loyal users → no unnecessary cost


False Positives (FP): Predicted churn but customer stays → minor extra marketing effort


False Negatives (FN): Missed churners → direct revenue loss 🚨


Priority: Minimize False Negatives to prevent unexpected customer loss.

📊 Key Business Insights
💡 Engagement Drives Retention
Customers with low usage and long inactivity are more likely to churn.
 Action: Re-engagement campaigns and personalized recommendations.
💡 New Customers Are High Risk
Users with short tenure churn more.
 Action: Strong onboarding and early support.
💡 Payment Issues Trigger Churn
Frequent payment failures strongly correlate with churn.
 Action: Improve billing reliability and reminders.
💡 Churn Is Predictable
Churn is driven by behavioral patterns, not random events.
 Action: Use predictive systems for proactive retention.

⚠️ Model Observation: Overfitting

The model shows signs of overfitting — high training performance but reduced performance on unseen data.
Potential Solutions:

Cross-validation


Hyperparameter tuning


Regularization


Feature reduction


This highlights awareness of real-world ML challenges.

☁️ How This Would Work in Production

Step 1: Data Collection

Daily data pulled from:

- App usage logs


- Login systems


- Payment systems


- Subscription databases


Step 2: Feature Engineering

Automated pipelines compute:

- Usage metrics
  
  
- Login frequency
  
  
- Tenure
  
  
- Payment history


Step 3: Prediction System
Customer Data → Feature Processing → ML Model → Churn Risk Score
Each customer receives a probability score indicating churn risk.
Step 4: Business Action Layer
| Risk Level  | Action                                   |
| ----------- | ---------------------------------------- |
| High Risk   | Discounts, special offers, support calls |
| Medium Risk | Engagement emails, tutorials             |
| Low Risk    | No action needed                         |


Step 5: Monitoring & Retraining

Model performance tracking


Periodic retraining with new data


Continuous improvement cycle



🧠 Skills Demonstrated

Data preprocessing


Exploratory data analysis


Supervised ML modeling


Model evaluation techniques


Business insight extraction


Understanding of overfitting


Production-level ML thinking



🚀 Business Impact

If implemented, this system can:

✔ Reduce churn

 ✔ Increase customer retention
 
 ✔ Improve marketing efficiency
 
 ✔ Increase subscription revenue
 
 ✔ Enable proactive decision-making
 

📌 Conclusion
This project demonstrates how machine learning can convert customer usage data into actionable business intelligence. By predicting churn early, organizations can shift from reactive to proactive customer retention strategies.

