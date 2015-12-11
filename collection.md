---
layout: page
title: Collection
nav-label: Collection
permalink: /collection/
---
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