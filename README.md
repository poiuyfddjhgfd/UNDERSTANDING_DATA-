# UNDERSTANDING_DATA-
This Jupyter Notebook understandingyourdata.ipynb provides a comprehensive initial exploration of the train.csv dataset, likely from a Titanic survival prediction challenge.

Key Steps and Observations:
Data Loading: The dataset is loaded into a Pandas DataFrame.
`
Data Size: The dataset contains 891 rows and 12 columns, indicating a moderately sized dataset.
`
Data Glimpse: A random sample of 10 rows is displayed using df.sample(10), offering a quick look at the data structure and values.
`
Data Types: df.info() reveals the data types for each column, including int64, float64, and object. It also highlights the number of non-null values.
`
Missing Values: df.isnull().sum() identifies the presence of missing values. Notably, 'Age' has 177 missing values, 'Cabin' has a significant 687 missing values, and 'Embarked' has 2 missing values.
`
Descriptive Statistics: df.describe() provides a statistical summary of the numerical columns, including count, mean, standard deviation, min, max, and quartiles. This helps understand the distribution and spread of numerical features.
`
Duplicate Values: df.duplicated().sum() confirms that there are no duplicate rows in the dataset.
`
Correlation with Survival: df.corr(numeric_only=True)['Survived'] calculates the correlation of numerical columns with the 'Survived' column. This is a crucial step for identifying features that might be good predictors of survival. For instance, 'Pclass' shows a negative correlation (higher class, higher survival), while 'Fare' shows a positive correlation (higher fare, higher survival).
`
Overall: This notebook effectively performs an initial exploratory data analysis (EDA), providing essential insights into the dataset's size, structure, data types, missing values, descriptive statistics, and preliminary correlations. This forms a solid foundation for further data cleaning, preprocessing, and model building.
