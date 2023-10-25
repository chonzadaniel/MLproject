# MLproject
A capstone project for Data Scientist Bootcamp Certification.

# Project Scope:
Building the Machine Learning Model.

# Project Problem Statement
A credit card is one of the most used financial products to make online purchases and payments, which should be safe from fraud. Hence, is important that credit card companies recognize fraudulent credit card transactions so that customers are not charged for items they did not purchase.

# Project Objective:
To build a Machine Learning classification model with a Classifier to predict whether a creditcard transaction is fraudulent or not. The project aims at testing the personal skills in Machine Learning Model building aiming at building a classifier with a predictive power with accuracy above 75%.

# Project Methodology:
## To Accomplish the Project Below are the Methodological Steps to Follow:
* Data Collection.
* Exploratory Data Analysis: Analyze and understand the data to identify patterns, relationships, and trends in the data by using Descriptive Statistics and Visualizations.
* Data Cleaning: This might include standardization, handling the missing values and outliers in the data.
* Dealing with Imbalanced data: This data set is highly imbalanced. The data should be balanced using the appropriate methods before moving onto model building.
* Feature Engineering: Create new features or transform the existing features for better performance of the ML Models.
* Model Selection: Choose the most appropriate model that can be used for this project.
* Model Training: Split the data into train & test sets and use the train set to estimate the best model parameters.
* Model Validation: Evaluate the performance of the model on data that was not used during the training process. The goal is to estimate the model's ability to generalize to new, unseen data and to identify any issues with the model, such as overfitting.
* Model Deployment: Model deployment is the process of making a trained machine learning model available for use in a production environment.

# Data and Data Source:
## Data Source:
Creditcard records collected for the two-day transactions in Europe whereby the dataset is provided by KnowledgeHud upGrad as one of the choices among many project concepts learners to consider.

## Nature of Data:
The dataset contains transactions made by credit cards in September 2013 by European cardholders. This dataset presents transactions that occurred in two days, where 492 frauds out of 284,807 transactions were identified.

# Loading of Dataset:
Dataset is loaded by creading a DataFrame 'df' using the Pandas library using the read_csv() method.

## Checking for successful dataset loading using a few methods:
* df.columns.
* df.shape.
* df.sample().
* df.head().
* df.tail().

# Conducting Exploratory Data Analysis (EDA) to see trends and patterns about the dataset features:
## Features pairwise correlation with target 'Class':
* Used sv.analyze() method after importing the library sweetviz as sv.
* Called the stored variable (report) using show_notebook() method.

## Investigating through the DataFrame checking the following:
* Datatypes.
* Detailed DataFrame information using df.info() method where null values are observed (if any).
* Checked for duplicates and unique values.
* Checked for feature values Minimum and Maximum to determine the convenient approach when scaling to within 0 and 1 values using df.describe() method.
* Conducted Time conversion to get the correct time format (from the numeric) to the date-time format using to_datetime() method.
* Visualized the Time column plotting a Histogram to find out the time distribution on transactions.
* Visualized transactions Amount to spot outliers.
* Visualized Transaction Amount vs Target ('Class') using Seaborn library.
* Visualized pairwise correlation across features.
* Visualized the distribution of the Class values using Matplotlib.pyplot as plt (pie chart) to confirm the imbalanced dataset.

# Performing Feature Transformation as Preparation for the Machine Learning Model to Efficiently train:
## Performing Feature Encoding
* Converted Time to binary value 0 and 1 integer datatype after clustering into two
* After all features were in float and integer datatypes, realized all float datatypes were in range above 1 value, hence need for scaling [0 & 1].

## Performing Feature Scaling
Except for Time and Class features, the rest were scaled uning MinMaxScaler() method after importing it from the sklearn.preprocessing library.

## X, y split from df2 (sampled dataset):
Supported by the Numpy Library droped y from the DataFrame using drop() method and storing y as testLabels in the integer datatype format

## Performed X_train, y_train split:
Using train_test_split() method imported from sklearn.model_selection was able to store X_train, y_train, X_test, y_test sets

# Model Selection:
* Given the need for imbalanced dataset handling such that iteration of different approach will be needed trying out to get high model performance metrics, Model predictive power, easy to handle and computation simplist, drove the selection of the Machine Learning Model.
* Long-Short Term Memory (LSTM) Machine Learning, which is a Recurring Neuron Network (RNN) model was preferred over Logistic Regression, Random Forest, and Xgboos models.
* LSTM ability to handle Vanishing Gradient Problem, ability to train efficiently on time series dataset, and with number of epochs flexibility are key LSTM model selection points creteria.
* <img src*https://www.google.com/url?sa=i&url=https%3A%2F%2Fwww.projectpro.io%2Farticle%2Flstm-model%2F832&psig=AOvVaw22T0_Z2YJc5mxvu4TeVhPF&ust=1698322169030000&source=images&cd=vfe&ved=0CBEQjRxqFwoTCIDR2KCVkYIDFQAAAAAdAAAAABAE>
