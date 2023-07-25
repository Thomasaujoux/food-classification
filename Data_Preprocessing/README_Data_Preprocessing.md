

# Data Preprocessing

## I) Context

The main goal of the project is to create a "Multi-Class Classification" using different Machine Learning technics. 

What does classification mean ? It is a supervised learning technique that deals with the categorization of a product into deffirent Sectors and Families.
What does Multi-Class Classification mean ? It is a special case when the target variable can take more than two values.

For this, we will use the data set from Oqali to train the model and then use this trained model on new data obtained from web-scraping from different famous french supermarkets like : "Auchan", "Franprix", etc ...

The data from Oqali is conventional with particular rules and abbreviations, this will lead to models with low bias (about 0.98 accuracy and 97 f1 score) but high variance on new data which doesn't follow the sames rules. As a result, it is important to create a new convention on data which can be applied on different websites, this will reduce the bias but also the variance.

In this file we will explore data preprocessing in order to improve the quality of the data and to make it suitable for "Exploratory Data Analysis" or "Multi-Label Classification", we will transform the raw data in a useful and efficient format. 

Data Cleaning :
- Missing Data : Some data are missing in the dataset from Oqali, we will handle this in different ways (Ignore it or Fill the missing values)
- Noisy Data : Some data liked ingredients are too specific thus meaninless for machine learning

Data Transformation : 
The goal is to transform the data in appropriate forms for Machine Learning, this will involved different NLP steps

Data Reduction

## II) Hierarchy

