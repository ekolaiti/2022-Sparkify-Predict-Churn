# 2022-Sparkify-Predict-Churn

## Sparkify Predicting Customer Churn

## Description: 
Sparkify is a made-up music app used by Udacity to simulate a music streaming platform. The users of Sparkify can use either the 'free' or the 'paid' version to listen to songs. Every time a user interacts with a platform they generate data that are recorded to a log file. This includes actions such as playing a song, rating a song using a 'thumbs up' or 'thumbs down', navigating through the platform or logging out.

The aim of the project is to predict whether a customer is at risk of 'churning', which is when a user is about to cancel their subscription and stop using the platform. By identifying the users that are about to churn, the platform can offer incentives, such as discounts, to increase retention. 

For this project a subset of the full dataset is manipulated using Apache Spark in order to engineer features for predicting customer churn. The Spark MLlib library is used to build a machine learning model that can work with large datasets, making this project a prototype for applying machine learning techniques to Big Data. In the mini dataset the users that churned are a fairly small subset, therefore the F1 score is chosen as the metric to optimise the model.

## Libraries:
pyspark sql
pyspark mllib
numpy
pandas
matplotlib
searborn
datetime

## Files:
This repository includes besides this README.md the following files:
notebook |- Sparkify.ipynb, a jupyter notebook that contains the data analysis and modeling steps

data |- mini_sparkify_event_data.json, a mini dataset which is a subset of the full 12GB dataset

## Instructions:
Clone the repository and run the jupyter notebook

## Results:
I used the ... algorithm and it returned the following best parameters: {'moc__estimator__learning_rate': 1, 'moc__estimator__n_estimators': 100}
The findings of this data analysis are presented in this blog post:
https://medium.com/@irene.kolaiti/its-where-you-live-not-what-you-know-5ed4b8c62ec3

## Considerations:
This mini dataset that was used to train the model is imbalanced, the churn label has too few examples of the minority class (churn = 1). 

## Acknowledgments:
Thank you to Udacity for designing this project.
