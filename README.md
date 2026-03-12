# WA_Fn-UseC_-Telco-Customer-Churn-Project
📌 Project Overview
This project aims to build a machine learning model to predict which customers are likely to cancel their telecommunications subscriptions. The goal is to provide the company with a reliable "early warning system," allowing them to take proactive retention steps to minimize revenue loss.

🛠 The Pipeline
1. Exploratory Data Analysis (EDA) & Visualization
Analyzed customer behavior and identified the strongest drivers of churn.

Key Finding: Customers on "Month-to-month" contracts and those with short "tenure" were significantly more likely to leave the service.

2. Data Cleaning & Preprocessing
Handled missing values in the TotalCharges column.

Performed Encoding to convert categorical text data into numerical formats.

Applied Feature Scaling to ensure the mathematical models interpret the data ranges accurately.

3. Feature Engineering
Developed a new feature called TotalServices to quantify the depth of a customer's engagement by aggregating all subscribed services.

4. Handling Imbalance
Since the majority of customers do not churn, the dataset was highly imbalanced.

To address this, I utilized the Class Weights property (scale_pos_weight) within XGBoost, forcing the model to prioritize learning the patterns of the minority class (churners).

5. Modeling & Hyperparameter Tuning
Tested and compared multiple algorithms, including Logistic Regression and Random Forest.

Optimized the final XGBoost model using GridSearchCV to find the most effective parameters for this specific dataset.

📈 Results & Evaluation
Final Model: XGBoost.

Primary Metric: Recall (Sensitivity).

Final Performance: Achieved a Recall of 0.79.

Business Logic: I specifically prioritized Recall over Accuracy. In the telco industry, the cost of losing a customer is far higher than the cost of offering a retention promotion to someone who might not have left. Capturing nearly 80% of potential churners provides a significant strategic advantage.

📁 Project Structure
final_churn_model_xgb.pkl: The serialized final model ready for inference.

data_scaler.pkl: The fitted scaler used to normalize new incoming data.

Copy_testtttt_of_WA_Fn_UseC__Telco_Customer_Churn_Project.ipynb: The complete Python notebook containing the full analysis and code.

I am proud of my first projects and excited for what's coming next!
