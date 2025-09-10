Comparison of Linear Regression and Random Forest Regression models when analyzing YouTube Data to make view predictions.
Created by John Stewart
09/09/2025

CS4680 Assignment 1:

Determining whether a video is considered “Trending” on YouTube:

Target Variable: Views

Features: 'category_id', 'publish_hour', 'publish_weekday', 'num_tags',
            'likes', 'dislikes', 'comment_count', 'description_len'

Dataset: 
https://www.kaggle.com/datasets/datasnaek/youtube-new/data

Data used: CAvideos.csv
Size: 45803 entries

Model Used: 
Linear Regression:
	Assumes relationship between features and target are linear
	Easy to interpret
	Trains quickly
	Sensitive to outliers

Random Forest Regression:
	Can handle non-linear and more complex interactions
	Handles outliers well
	More difficult to interpret than linear


Analysis:
	The Linear Regression model was simpler, but seems to have less accurate assumptions. Most notably, it did not handle outliers well. For example, one video had 17,340 views, but the linear regression model predicted over 169 thousand. The random forest regression model, on the other hand, predicted only 50 thousand views, which is much closer to the actual number. This remained true for most entries. 
	The Mean Absolute Error was significantly lower for the Random Forest Regression model, and the Coefficient of Determination(R^2) was closer to 1. This means that the Random Forest Regression model was a better choice for predictions with this dataset. The predictions were much closer to the real values.
	Both models were suitable for the task, but the RFR model proved to be superior by a surprising margin.


