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
notebook |- Sparkify.ipynb, a jupyter notebook that contains the data analysis and modeling steps. 
  
data |- mini_sparkify_event_data.json.zip, a compressed version of the mini dataset, which is a subset of the full 12GB dataset. 

## Instructions:
Clone the repository, decompress the dataset and save it in the same folder as the notebook, run the notebook.

## Results:
Predicting churn has involved data exploration in order to observe user behaviour with Sparkify, extracting promising features, and machine learning modelling. After considering three machine learning algorithms, Random Forest Classifier was selected as the winning model. The final evaluation metrics are F1 score: 0.727358 and accuracy: 0.764706 and the best parameters were maxDepth: 10 and numTrees: 10. In terms of feature importance, the ‘days since registration’ feature, and the ‘thumbs down’, ‘add friends’ and ‘roll adverts’ actions are the most important when predicting churn.

The solution and findings of this project are presented in this blog post:
https://medium.com/@irene.kolaiti/sparkify-should-i-stay-or-should-i-churn-80bcd83020c9

## Considerations:
This mini dataset that was used to train the model is imbalanced, the churn label has too few examples of the minority class (churn = 1). 

## Acknowledgments:
Thank you to Udacity for designing this project.
