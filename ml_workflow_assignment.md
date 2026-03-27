You are a junior data analyst at a retail company. Your manager hands you a dataset of past customer orders and asks you to build a model that predicts whether a customer will make a repeat purchase within 30 days.

The dataset contains the following columns:

Column	Description
customer_id	Unique customer identifier
order_count_last_90d	Number of orders placed in the last 90 days
avg_order_value	Average order value in INR
days_since_last_order	Days elapsed since the customer's most recent order
repeat_purchase_flag	1 if the customer made a repeat purchase within 30 days, 0 otherwise
discount_used_on_repeat_order	Discount applied on the repeat purchase order

**Task 1**  
Identify which column in the dataset is the label, and which column, if included as a feature, would introduce data leakage. For each, write one sentence justifying your choice.

- **Label**: repeat_purchase_flag - This column indicates the target outcome we are trying to predict, whether a customer will make a repeat purchase within 30 days.
- **Data Leakage**: discount_used_on_repeat_order - Including this as a feature would leak information about the future repeat purchase, as the discount is only applied if the repeat purchase occurs, making the model unfairly aware of the target variable.

**Task 2**  
Your manager skips straight to training a gradient boosting model. Suggest two steps from the complete ML workflow that should have been completed first, and briefly explain why each step matters before jumping to a complex model.

1. **Exploratory Data Analysis (EDA)**: This step involves analyzing the dataset to understand distributions, identify patterns, detect outliers, and check for correlations, which is crucial to ensure the data is suitable for modeling and to inform feature engineering.
2. **Data Preprocessing and Cleaning**: This includes handling missing values, encoding categorical variables, scaling features, and removing irrelevant columns, as it prepares the data for training and prevents issues like biased models or poor performance due to unclean data.
