**Project Overview**

This project involves analyzing the Churn Modeling dataset to gain insights into customer behavior and predict customer churn using a machine learning model. The analysis includes data preprocessing, exploratory data analysis, handling outliers, balancing the dataset, and building a predictive model using the K-Nearest Neighbors (KNN) algorithm.

**Introduction**
Customer churn is a critical issue for businesses, especially in the banking sector, where retaining customers is essential for sustained growth. This project aims to predict whether a customer will leave the bank based on various demographic and financial features. By building a predictive model, the bank can identify potential churners and take proactive measures to retain them.

**Dataset Description**
The Churn Modeling dataset contains information about customers of a bank, including demographic, financial, and transactional data. The target variable is Exited, which indicates whether a customer has left the bank. The dataset includes the following features:

RowNumber: Row index

CustomerId: Unique identifier for each customer

CreditScore: Credit score of the customer

Geography: Country of residence

Gender: Gender of the customer

Age: Age of the customer

Tenure: Number of years with the bank

Balance: Account balance

NumOfProducts: Number of products the customer has with the bank

HasCrCard: Indicates if the customer has a credit card

IsActiveMember: Indicates if the customer is an active member

EstimatedSalary: Estimated salary of the customer

Exited: Indicates if the customer has exited the bank (target variable)

**Data Preprocessing**

**Loading Dataset**

The dataset is loaded using the Pandas library.

**Handling Missing Values**

There are no missing values in the dataset, which ensures that all records are complete and ready for analysis.

**Dropping Unnecessary Columns**

The Surname column is dropped as it is not useful for predictive modeling.

**Removing Duplicates**

Duplicate records are removed to ensure the dataset is clean and free from redundancy.

**Converting Categorical to Numerical**

Categorical columns such as Geography and Gender are converted to numerical values to facilitate machine learning algorithms.

**Standardizing Numerical Features**

Numerical features are standardized to ensure they have a mean of 0 and a standard deviation of 1. This step is crucial for algorithms like KNN, which are sensitive to the scale of input data.

**Exploratory Data Analysis (EDA)**

Histograms for Numerical Columns

Histograms are plotted for numerical columns to visualize their distributions. Key insights include:

CreditScore: Normally distributed with a peak around the center.

Geography: Categorical distribution showing different countries.

Gender: Binary distribution representing male and female.

Age: Distribution helping to understand the age demographics.

Tenure: Spread indicating how long customers have been with the bank.

Balance: Right-skewed distribution showing most customers have a lower balance.

NumOfProducts: Distribution indicating the number of products each customer has.

HasCrCard: Binary distribution of credit card ownership.

IsActiveMember: Binary distribution of active members.

EstimatedSalary: Roughly uniform distribution of salaries.

**Outlier Detection and Handling**

Outliers are detected and handled using the Interquartile Range (IQR) method. Box plots are used to visualize outliers before and after cleaning. Outliers in columns such as CreditScore, Age, and NumOfProducts are identified and removed to improve model performance.

**Balancing the Dataset**

The dataset is imbalanced with a higher number of non-churners compared to churners. To address this, the Synthetic Minority Over-sampling Technique (SMOTE) is used to balance the target variable. This technique generates synthetic samples to balance the class distribution.

**Model Building**

The dataset is split into training and testing sets. The K-Nearest Neighbors (KNN) algorithm is used for modeling. KNN is chosen for its simplicity and effectiveness in classification tasks. The model is trained on the training set and predictions are made on the test set.

**Model Evaluation**

The model's performance is evaluated using precision, recall, and F1 score. These metrics provide insights into the model's accuracy in predicting customer churn. The precision score, which measures the accuracy of positive predictions, is found to be 23%.

**Conclusion**

This project demonstrates the process of analyzing customer churn data, handling outliers, balancing the dataset, and building a predictive model. While the KNN model achieves a precision score of 23%, further tuning and exploration of other algorithms may be needed to improve performance. The insights gained from this analysis can help the bank develop strategies to retain customers and reduce churn.
