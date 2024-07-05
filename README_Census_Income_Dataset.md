**Project Overview**

This project involves analyzing the Census Income dataset to gain insights into the factors affecting income levels and to build a predictive model to classify individuals as having an income above or below $50K. The analysis includes data preprocessing, exploratory data analysis, handling outliers, balancing the dataset, and building a predictive model using the K-Nearest Neighbors (KNN) algorithm.

**Introduction**

The Census Income dataset, also known as the "Adult" dataset, is used to predict whether a person earns over $50K a year based on various attributes. This project aims to preprocess the data, perform exploratory data analysis, handle outliers, balance the dataset, and build a predictive model using the K-Nearest Neighbors (KNN) algorithm to classify income levels.

**Dataset Description**

The dataset contains demographic and employment-related information for individuals. The target variable is income, which indicates whether an individual's income is above or below $50K. The dataset includes the following features:

age: Age of the individual

workclass: Employment type

education.num: Number of years of education

marital.status: Marital status of the individual

occupation: Occupation type

relationship: Relationship status

race: Race of the individual

sex: Gender of the individual

capital.gain: Capital gains

capital.loss: Capital losses

hours.per.week: Hours worked per week

native.country: Country of origin

income: Income level (target variable)

**Data Preprocessing**

**Loading Dataset**

The dataset is loaded using the Pandas library.

**Handling Missing Values**

There are no missing values in the dataset, ensuring all records are complete and ready for analysis.

**Dropping Unnecessary Columns**

The education and fnlwgt columns are dropped as they are not deemed useful for predictive modeling.

**Removing Duplicates**

Duplicate records are removed to ensure the dataset is clean and free from redundancy.

**Converting Categorical to Numerical**

Categorical columns such as workclass, marital.status, occupation, relationship, race, sex, native.country, and income are converted to numerical values to facilitate machine learning algorithms.

**Standardizing Numerical Features**

Numerical features are standardized to ensure they have a mean of 0 and a standard deviation of 1. This step is crucial for algorithms like KNN, which are sensitive to the scale of input data.

**Exploratory Data Analysis (EDA)**

**Missing Values Heatmap**

A heatmap is used to confirm there are no missing values in the dataset.

**Income Distribution**

A bar plot is created to visualize the distribution of income levels, revealing that the dataset is imbalanced with more individuals earning less than $50K.

**Correlation Matrix**

A heatmap of the correlation matrix is used to visualize the relationships between numerical features. Key insights include:

income positively correlates with capital.gain and hours.per.week.

income has a negative correlation with education.num.

**Outlier Detection and Handling**

Outliers are detected and handled using the Interquartile Range (IQR) method. Box plots are used to visualize outliers before and after cleaning. Significant outliers in columns such as age, education.num, capital.gain, capital.loss, and hours.per.week are identified and removed to improve model performance.

**Balancing the Dataset**

The dataset is imbalanced with a higher number of individuals earning less than $50K compared to those earning more. The Synthetic Minority Over-sampling Technique (SMOTE) is used to balance the target variable, generating synthetic samples to balance the class distribution.

**Model Building**

The dataset is split into training and testing sets. The K-Nearest Neighbors (KNN) algorithm is used for modeling due to its simplicity and effectiveness in classification tasks. The model is trained on the training set and predictions are made on the test set.

**Model Evaluation**

The model's performance is evaluated using precision, recall, and F1 score. These metrics provide insights into the model's accuracy in predicting income levels. The precision score, which measures the accuracy of positive predictions, is found to be 90%.

**Conclusion**

This project demonstrates the process of analyzing the Census Income dataset, handling outliers, balancing the dataset, and building a predictive model. The KNN model achieves a precision score of 90%, indicating its effectiveness in classifying income levels. The insights gained from this analysis can help in understanding the factors affecting income and developing strategies to improve income prediction.

