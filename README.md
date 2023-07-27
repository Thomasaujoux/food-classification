# Semi-automatic Multi-Class Classification of food offer in Oqali sectors and families for web-scraped data

## General Presentation

This repository includes the second part of my second-year internship at ENSAE (National School of Statistics and Economic Administration), which I carried out at INRAE (National Research Institute for Agriculture, Food and the Environment) over a 3-month period.

## Planning

The initial planning did not include any hard deadlines, and left room for flexibility. Here are the main stages:
- Study of Oqali and web-scraped data (Descriptive Statistics, Exploratory Data Analysis, NLP, ...),
- feasibility study of the semi-automatic categorization algorithm,
- implementation of the semi-automatic categorization algorithm (Multunomiale Naive Bayes, Logistic Regression, SVM Classifier, Random Forest, ...),
- analysis of the results of the semi-automatic categorization algorithm and optimization (Imbalanced Data Set, Underfitting and Overfitting, ...).

The foreseeable difficulties were :
- The classification will have to take many variables into account;
- The nomenclature for this categorization is very extensive (over 600 families);
- Quite few similar works;
- Available data on ingredients are difficult to manipulate, as there are many instances
many instances, and we sometimes find raw lists of a food's ingredients, sometimes
sometimes undecomposed.
- ...

## Contributions

An algorithm for automatic categorization of Oqali sectors and families had already been developed by the team. It was based on two models (SVM Classifier and Random Forest) and had obtained very satisfactory results for Oqali. 

The aim of this internship was therefore also to test different approaches, improve the algorithm , make it more flexible so that it can be adapted to data retrieved from the Internet, which do not have the same conventions as the Oqali database, based on data that could be analyzed at any time.

The contributions made during this internship were to propose a semi-automatic categorization method offering a complete information processing workflow made up of four modules listed below:
- a data pre-processing algorithm,
- a data vectorization algorithm,
- a data training algorithm,
- a prediction algorithm

## Tools and technologies

Python is an interpreted, multi-paradigm, multi-platform programming language. It has the advantage of custom libraries, such as scikit-learn, widely used in Machine Learning and data categorization. The language has extensive documentation and a large community on the Internet, making it an invaluable resource in case of bugs or questions. The working environment was Visual Studio Code, a free, open source Python distribution dedicated to data science. We used a template called CookieCutter to organize the code according to the stages of our algorithm. scikit-learn is a free Python library for machine learning. Among the methods it offers, we will focus on those for pre-processing, vectorization and classification. In order to share the source code with the rest of the team, the project has been deposited on Git, "a decentralized version management software". 

## Context 

The main goal of the project is to create a "Multi-Class Classification" using different Machine Learning technics.

Classification is a method for analyzing data by grouping data with the most similar characteristics into several classes. In the case of the products we are studying, Oqali classifies them into food sectors and families based on several criteria. There are different types of classification, but we're going to take a closer look at the Multi-class classification.

What does Multi-Class Classification mean ? It is a special case when the target variable can take more than two values but just one at a time.

To do this, we will use the Oqali data to train the model, then we will use this trained model on new data obtained from web-scraping of various famous French supermarkets such as: "Auchan, Franprix, etc ...

To explain the improvements and transformations made during the course, we need to introduce two classic machine learning concepts: bias and variance.
Bias is an error due to wrong assumptions about data whereas variance is linked to the sensitivity of variations and noise in the data.

*Low Bias* is when we have made fewer assumptions in order to build the target function. It will lead to underfit the model
*High Bias* is when we have taken more assumtpions to build the target function.

There are some solutions to reduce bias :
- Use a more complex model
- Increase the number of features
- Reduce Regularization of the model
- Increase the size of the training data

*Low Variance* is when the model is less sensitive to changes in the training data
*High Variance* is when the model is very sensitive to changes in the training data

There are some solutions to reduce variance:
- Cross validation
- Feature selection
- Regularization
- Ensemble methods
- Simplifying the model
- Early stopping

The main goal of a classic Machine Learning project is to have low bias and variance.

### Previous Project


### Enhancement and Extension to Web-scrapping Data

- take different variables into account
- Different data cleansing
- New models adapted
- Changes in NLP
- less bias
The Oqali data are conventional with particular rules and abbreviations, which will lead to models with low bias and variance (around 0.98 precision and 0.97 f1 score) but high bias and variance on new data that don't follow the same rules. Therefore, it is important to create a new convention on the data that can be applied across different websites, which will reduce bias but also variance.

## Taking a step back

## Project hierarchy

## Conclusion

