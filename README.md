# Customer_Churn_Pediction

Objective: Develop a machine learning model to predict customer churn based on historical
customer data.


Approach:
1. Data Preprocessing:
- Data Loading: Started by loading the provided dataset in CSV format.
- Initial Data Exploration: Performed an initial exploration of the dataset to understand its
structure and characteristics. This included checking the first few rows of the data and obtaining
information about data types and missing values.
- Handling Missing Data: Any rows with missing data were removed from the dataset as a first
step in handling missing values.
- Encoding Categorical Variables: Applied label encoding to the 'gender' and 'location'
categorical variables to convert them into numerical form.
- Splitting Data: Split the data into training and testing sets, with a test set size of 20% for
model evaluation.


2. Feature Engineering:
- Scale: Normalize the numerical features in training and testing sets using StandardScaler
- Feature addition: Calculated a new feature called “Usage_per_month” in the data frame by
dividing the “Total_Usage_GB” column by the “Subscription_Length_Months” column,
representing the average monthly usage of each customer.


3. Model Selection:
- Selected “Random Forest Classifier” as the best model for predicting customer churn. The
decision was based on its ability to handle both categorical and numerical features and its
robustness to overfitting.


4.. Model Evaluation:
- Calculated and displayed the confusion matrix and classification report, which provided
insights into the model's ability to classify churned and non-churned customers. This included
metrics such as accuracy, precision, recall, and F1-score.


5. Model Optimization:
- Implemented k-fold cross-validation with k=5 to more robustly assess the model's
performance. This technique helped us estimate the model's performance on different subsets
of the training data and reduced the risk of overfitting. Also, Implemented hyperparameter
turning with parameters such as number_of_estimators, max_depth, min_samples_split,
min_samples_leaf which improves the accuracy.


6. Model Deployment:
- Uses the Pickle library to save the trained model as a binary file named “model.pkl” allowing
for later use or deploymen
