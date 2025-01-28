Titanic Dataset Preprocessing

This repository contains a Python script for preprocessing the Titanic dataset, which is often used for machine learning tasks like classification. The script includes various steps such as handling missing values, outlier detection, feature engineering, and encoding categorical variables. The dataset used is the Titanic dataset, which contains information about passengers aboard the Titanic and whether they survived or not.

Steps Performed
Loading Dataset

The Titanic dataset is loaded from a CSV file.
Handling Missing Values

Missing values in the 'Age' column are filled using the median of the column.
Missing values in the 'Embarked' column are filled using the mode (most frequent value) of the column.
Dropping Irrelevant Columns

The 'Cabin' column is dropped since it contains too many missing values.
Checking for Remaining Missing Values

After handling missing values, a check is performed to ensure there are no remaining missing values in the dataset.
Handling Outliers in 'Fare'

The outliers in the 'Fare' column are identified using the Interquartile Range (IQR) method.
Data points outside 1.5 * IQR range are removed.
Convert 'PassengerId' to Categorical

The 'PassengerId' column is converted to a categorical data type.
Normalize Numerical Features

The numerical features ('Age' and 'Fare') are normalized using StandardScaler to have a mean of 0 and a standard deviation of 1.
Feature Engineering: Family Size

A new feature 'FamilySize' is created by adding the 'SibSp' and 'Parch' columns and adding 1 to account for the passenger themselves.
One-Hot Encoding

One-hot encoding is applied to the 'Sex' and 'Embarked' columns. The first category in each column is dropped to avoid multicollinearity.
Dropping Irrelevant Columns

The 'Name', 'Ticket', and 'PassengerId' columns are dropped as they are not needed for the analysis.
Final Dataset
The final dataset consists of the following columns:

Survived: Target variable, indicates whether the passenger survived (1) or not (0)
Pclass: Passenger class (1, 2, or 3)
Age: Normalized age of the passenger
SibSp: Number of siblings/spouses aboard
Parch: Number of parents/children aboard
Fare: Normalized fare paid by the passenger
FamilySize: Total family size (including the passenger)
Sex_male: One-hot encoded feature for male passengers
Embarked_Q: One-hot encoded feature for passengers who boarded at station Q
Embarked_S: One-hot encoded feature for passengers who boarded at station S
How to Run the Code
Install the necessary libraries:
bash
Copy
Edit
pip install pandas numpy seaborn matplotlib scikit-learn
Update the file path for the Titanic dataset CSV in the script.

Run the script to preprocess the dataset.
