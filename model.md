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

<Add image of the baseline model> 

3.)Classification: We classified the current comments into good or bad comment so that we may be able to predict whether a comment will be good or not. One of the more recommended approach was through the usages of the Naive Bayes Classifier.   It is a simple probabilistic classifiers that applys Bayes' theorem with a strong naive assumption that all the features are independent of each other. 

* ADD THE MATH EQUATION HERE
* 
4.) We fit the data and cross validated and checked to see our accruacy and calibration graph, as well as generate a list of words to use and avoid if one wnats to do well on reddit.
<Add the graph >

The results show that there wasn't much improvement from the baseline. One explanation is that there are simply too many factors that I am not accounting for. Also that the choice of words do not have much predictive power as to how well liked the comment will be on reddit in general

5.) We can try this analysis again on a more limited scoped subreddit, such as R/Conservative.
The data showed improvement of around 2~3% from the baseline, and produced a new set of words that can produce good results.

<add the graph here>

More modelling is done on the extention github for how we found the simliarity between articles and comments.
