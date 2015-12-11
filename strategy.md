---
layout: page
title: Strategy
nav-label: Strategy
permalink: /strategy/
---
<h2>Training Strategy</h2>
The overarching strategy of our application consists of two phases, a prediction phase and a training phase. The training phase results in a parametrized model to predict top comments. The prediction phase uses this model to predict the top comments for a particular article.
<br>
<br>
The following training strategy summarizes the work completed in the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Collection%20Factory.ipynb">**Collection Factory**</a>, the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Feature%20Factory.ipynb">**Feature Factory**</a>, the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/EDA.ipynb">**Exploratory Data Analysis** </a> and the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/model.ipynb">**Model Factory** </a>.

<div>
  <h3>Traing Strategy</h3>
  <img img width="664" alt="trainingstrat" src="../images/TrainingStrat.png">
</div>

<br>
<br>
In order to train our model we need to collect articles tha exist in the reddit verse and the top comments related to that article. The <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Collection%20Factory.ipynb">**Collection Factory**</a> uses the Reddit API to collect a broad range of article and thier associated comments. The <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Feature%20Factory.ipynb">**Feature Factory**</a> uses this data to create features regarding the article content, the comment content and the similarity between them. The features are designed to articulate the relationship between the comments and the interest article. The final features are the result of an iterative process of extraction, exploration and modelling. The majority of the feature exploration occurs in the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/EDA.ipynb"> **EDA notebook**</a>. 

The feature extraction, EDA, modelling cycle is a continuous loop. The best model produced is effectively related to the number of times this cycle is completed.
<br>
<br>

<h2>Prediction Strategy</h2>
The following process identifies our prediction strategy. This process that occurs when we predict the top comments for an interest article. The primary difference between the prediction strategy and the training strategy is the concept of an interest article. This is the article for which we want to identify the top comments. In the training strategy we were looking at the relationship between comments and the article they were discussing. For prediction we look at the relationship between comments and the interest article. 

<img src="../images/PredictionStrat.png">
<br>
The entry to the above process is our front end website or chrome extension. This component accepts the URL of the interest article and identifies the keywords of the article. The keywords are passed to the **Collection Factory** which uses the keywords to find similar articles that exist in the reddit verse. The **Collection Factory** scrapes the similar articles and their respective comment threads. This process ensures that we comments generated from articles similar to the interest article. The articles and comments are then passed to the **Feature Factory**. The difference being we want to look at the relationships between the comments and the interest article opposed to the article they are actually discussing. 
<br>
<br>
The collection and feature extraction steps of the Prediction startegy can be summarized in the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Prediction%20Data%20Factory.ipynb">**Prediction Data Factory**</a>
<br>
<br>
The last step is to pass the completed features to the **Model**. The **Model**  uses the features in a to identify the top comments and return them to the user.
<br>
<br>


