**Project Overview**

This project involves analyzing the Heart Disease dataset to understand the factors contributing to heart disease and building a predictive model to classify individuals as having heart disease or not. The analysis includes data preprocessing, exploratory data analysis, handling outliers, balancing the dataset, and building a predictive model using the K-Nearest Neighbors (KNN) algorithm.

**Introduction**

Heart disease is a leading cause of death globally, and early detection is crucial for effective treatment. This project aims to preprocess the Heart Disease dataset, perform exploratory data analysis, handle outliers, balance the dataset, and build a predictive model using the K-Nearest Neighbors (KNN) algorithm to classify individuals based on their likelihood of having heart disease.

**Dataset Description**

The dataset contains medical information about individuals, with the target variable indicating the presence of heart disease. The features include:

age: Age of the individual

sex: Gender of the individual

cp: Chest pain type

trestbps: Resting blood pressure

chol: Serum cholesterol in mg/dl

fbs: Fasting blood sugar > 120 mg/dl

restecg: Resting electrocardiographic results

thalach: Maximum heart rate achieved

exang: Exercise-induced angina

oldpeak: ST depression induced by exercise relative to rest

slope: Slope of the peak exercise ST segment

ca: Number of major vessels colored by fluoroscopy

thal: Thalassemia

target: Presence of heart disease (target variable)

**Data Preprocessing**

**Loading Dataset**

The dataset is loaded using the Pandas library.

**Handling Missing Values**

There are no missing values in the dataset, ensuring all records are complete and ready for analysis.

**Removing Duplicates**

Duplicate records are removed to ensure the dataset is clean and free from redundancy.

**Standardizing Numerical Features**

Numerical features such as age, trestbps, chol, thalach, and oldpeak are standardized to ensure they have a mean of 0 and a standard deviation of 1. This step is crucial for algorithms like KNN, which are sensitive to the scale of input data.

**Exploratory Data Analysis (EDA)**

**Target Variable Distribution**

A count plot is used to visualize the distribution of the target variable, showing that the dataset is imbalanced with more samples indicating the presence of heart disease.

**Pairwise Relationships**

A pair plot is used to visualize the relationships between features, highlighting potential correlations and separations between classes.

**Correlation Matrix**

A heatmap of the correlation matrix is used to visualize the relationships between numerical features. Key insights include:

thalach (maximum heart rate) has a strong negative correlation with exang (exercise-induced angina).

age and thalach show a moderate negative correlation.

cp (chest pain type) shows a moderate positive correlation with target.

**Outlier Detection and Handling**

Outliers are detected and handled using the Interquartile Range (IQR) method. Box plots are used to visualize outliers before and after cleaning. Significant outliers in columns such as trestbps, chol, thalach, and oldpeak are identified and removed to improve model performance.

**Balancing the Dataset**

The dataset is imbalanced with a higher number of samples indicating the presence of heart disease. The Synthetic Minority Over-sampling Technique (SMOTE) is used to balance the target variable, generating synthetic samples to balance the class distribution.

**Model Building**

The dataset is split into training and testing sets. The K-Nearest Neighbors (KNN) algorithm is used for modeling due to its simplicity and effectiveness in classification tasks. The model is trained on the training set and predictions are made on the test set.

**Model Evaluation**

The model's performance is evaluated using precision, recall, and F1 score. These metrics provide insights into the model's accuracy in predicting heart disease. The recall score, which measures the accuracy of detecting true positives, is found to be 90%.

**Conclusion**

This project demonstrates the process of analyzing the Heart Disease dataset, handling outliers, balancing the dataset, and building a predictive model. The KNN model achieves a recall score of 90%, indicating its effectiveness in classifying heart disease. The insights gained from this analysis can help in understanding the factors contributing to heart disease and developing strategies for early detection and treatment.
