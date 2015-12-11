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
The following training strategy summarizes the work completed in the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Collection%20Factory.ipynb">**Collection Factory**</a>, the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Feature%20Factory.ipynb">**Feature Factory**</a>, the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/EDA.ipynb">**Exploratory Data Analysis** </a> and the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Model.ipynb">**Model Factory** </a>.

<img src="../images/TrainingStrat.png">

<br>
<br>
In order to train our model we need to collect articles tha exist in the reddit verse and the top comments related to that article. The <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Collection%20Factory.ipynb">**Collection Factory**</a> uses the Reddit API to collect a broad range of article and thier associated comments. The <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Feature%20Factory.ipynb">**Feature Factory**</a> uses this data to create features regarding the article content, the comment content and the similarity between them. The features are designed to articulate the relationship between the comments and the interest article. The final features are the result of an iterative process of extraction, exploration and modelling. The majority of the feature exploration occurs in the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/EDA.ipynb"> **EDA notebook**</a>. 

The feature extraction, EDA, modelling cycle is a continuous loop. The best model produced is effectively related to the number of times this cycle is completed.
<br>
<h3>Collection Factory</h3>
The <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Collection%20Factory.ipynb">**Collection Factory**</a> is the mechanism for collecting all of the data required for the application. The factory makes use of the reddit API to identify a broad range of articles similar to those we are expecting to use for prediction. The factory collects the comments related to each particular article and then collects the article itself. 
<br>
<br>
In order to provide the most effective training data the Collection Factory was designed with the following considerations
<br>
* Only collect comments directly in response to an original article post. We restrict our collection to first level responses in an effort to avoid collecting comments not directly related to the original article.
* Collect from specific sub-reddits where the original content is usually an external source ie. r/news, r/TIL
* Avoid sub-reddits where there is no original content like AMA's, or ELI5
* Avoid multi-media subreddits like r/pics, r/videos

<h3>Feature Factory</h3>
The <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Feature%20Factory.ipynb">**Feature Factory**</a> is the mechanism for extracting useful attributes from the comments, the articles and the relationship between them. Some of the features were created at collection time to reduce the amount of data that would be stored; but we expand on those features here. The premise of our application is that the top comments, will be syntactically similar to the articles they are describing. For example, comments and users that use the same language of the article may increase the overall score of that article. The feature factory produces a large variety of these comparisons and we use EDA to determine the ones with the most predictive power.

The features we created are largely bag of word representations of either the full text or keywords of the articles and the comments. One way we can compare these bags of words is to use the cosine similarity. 
<br>
<br>
The cosine similarity, measures the similarity between two bags of words or vectors where A and B represent two vectors.  

$$\frac{A*B}{|A||B|}$$

The cosine distance was chosen because it accounts for the length of the vectors. This is important when we are comparing articles, which tend to be quite long, to comments which can be quite short. 

The downside of using cosine similarity is that is does not account for the global popularity of a term. This means that two vectors with a few rare terms in common is the same as two vectors with a few popular words in common. This is an obvious issue we would like to address by using the term frequency- inverse document frequency weight of each word. 

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


