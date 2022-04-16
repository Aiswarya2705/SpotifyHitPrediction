# Spotify Hit Prediction - Project Overview
* Created a model to predict if a track is going to be a hit or not, using the track's various attributes.
* Using data through 2010-2019s from "The Spotify Hit Predictor Dataset" from Kaggle:  https://www.kaggle.com/theoverman/the-spotify-hit-predictor-dataset?select=dataset-of-10s.csv
* Conducted data cleaning and Exploratory Data Analysis, before getting the features ready for model building.
* Logistic Regression, Decision Trees, Random Forest and Support Vector Machines were fitted and compared using AUC ROC curves and scores.
* Used Random Search CV and Grid Search CV to find the optimum parameters for the best model out of the above mentioned four.

##  Resources and Code
**Language**  - Python 3.9.5 <br>
**Packages** - pandas, Numpy, matplotlib , seaborn , plotly, sklearn <br>
**Notebook referred** - https://www.kaggle.com/sarthaktyagi01/spotify-hit-prediction <br>
**Article referred** - https://towardsdatascience.com/what-makes-a-song-likeable-dbfdb7abe404 <br>
**Project Guidelines** - Ken Jee's Data Science Project from Scratch Series (link - https://www.youtube.com/watch?v=MpF9HENQjDo&list=PL2zq7klxX5ASFejJj80ob9ZAnBHdz5O1t) <br>

## Data Cleaning
The data was in a good condition, but the following steps had to be done:  <br>
* Removed duplicate rows <br>
* Removed unnecessary columns <br>

## Exploratory Data Analysis
* Understood how each of the features affect the target variable, by using data visualization tecnhiques and other functions provided by pandas <br>
* Created new features from existing features to get a better idea of the data <br>
* Created a wordcloud showing the top 10 artists who had the most hit songs from 2010 to 2019 <br>
* Created visualizations showing the tracks and artists with the highest values for each attribute of a track like `danceabilty`,`acousticness`,`energy`, etc. <br>

## Model Building
* After splitting the data into train and test sets with a test size of 20%, I tried four different models and used AUC ROC score as the main evaluation metric. It is reliable and it is the measure of the ability of a classifier to distinguish between classes and is used as a summary of the ROC curve. <br>
* __Logistic Regression__ - the first model to try on the data. It is great for binary classification tasks.
* __Decision Trees__ - easy to understand and not much assumptions to be satisfied
* __Random Forest__ - Ensemble method, and hence, might give use better results
* __Support Vector Machines__ - maximum margin hyperplanes

## Model Performance
The higher the AUC, the better the performance of the model at distinguishing between the positive and negative classes. <br>
* AUC score for __Logistic Regression__ : 0.88 <br>
* AUC score for __Decision Trees__ : 0.77 <br>
* AUC score for __Random Forest__ : 0.93 <br>
* AUC score for __Support Vector Machines__ : 0.92 <br>
