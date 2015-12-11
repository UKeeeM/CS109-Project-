---
layout: page
title: Model
nav-label: Model
permalink: /model/
---

In our model, we attempted to first answer the question of whether we could predict the sucess of a reddit comment. Then the next question was whether we could use data to find the most well liked comment that is most clsoely related to an article in question. That turned out to be easier to model and implement, and you can check out the extension page to see it implemented. 


1.) First step of the modeling process was Upvote Normalization. we normalized our upvotes to the interval [0,1] using this method to rescale the values. The reason for this was due to the extream variance in the number of upvotes that reddit comments recieved. 

*ADDITION SUBTRACTION MATH EQUATION HERE

2.) Second step was to add in additional features, or charecteristics of the comments. We added in more features such as, number of words in comment, number of charecters in comments, tokenized representation of the words, bag of word representation, and more.

3.) This step, we created a baseline model of what the accuracy is when one simply classify every commemnt as good vs classfying every comment as bad. Unsurprisingly, and as expected, the accuracy when one assumes every comment is good is 5%. This is due to the majority of reddit comments simply being "bad" and not recieving any meaningful number of upvotes. When one assumes every comment is bad, it is 95% accurate. This is the measure that we are trying to beat. 

<div>
<img img width="664" alt="baseline" src="../images/baseline.png"> 
</div>

3.)Classification: We classified the current comments into good or bad comment so that we may be able to predict whether a comment will be good or not. One of the more recommended approach was through the usages of the Naive Bayes Classifier.   It is a simple probabilistic classifiers that applys Bayes' theorem with a strong naive assumption that all the features are independent of each other. We fit the Tokenized sentences data using a TfidfVectorizer to offset certain words taht appear very frequently, which are not stopwords (such as people) from skewing the results

* ADD THE MATH EQUATION HERE

4.) We fit the data and cross validated and checked to see our accruacy and calibration graph, as well as generate a list of words to use and avoid if one wnats to do well on reddit.

<div>
<img img width="664" alt="baseline" src="../images/new_graph.png"> 
</div>

<div>
<img img width="664" alt="baseline" src="../images/word.png"> 
</div>


The results show that there wasn't much improvement from the baseline. One explanation is that there are simply too many factors that I am not accounting for. Also that the choice of words do not have much predictive power as to how well liked the comment will be on reddit in general
![acc](https://cloud.githubusercontent.com/assets/5473875/11735072/38719040-9f8b-11e5-809b-f8849863b4d8.PNG)


5.) We can try this analysis again on a more limited scoped subreddit, such as /r/Conservative.
The data showed improvement of around 2~3% from the baseline, and produced a new set of words that can produce good results.

<div>
<img img width="664" alt="baseline" src="../images/conservativegraph.png"> 
</div>

<div>
<img img width="664" alt="baseline" src="../images/conservativeword.png"> 
</div>


<b>Prediction</b>
We do the predictions through a Google Chrome Extension that we created. More detials regarding prediciton can be found
(<a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Prediction%20Data%20Factory.ipynb">here, (Predictions)</a>)
<div>
<img img width="664" alt="baseline" src="../images/expertzoom.png"> 
</div>

