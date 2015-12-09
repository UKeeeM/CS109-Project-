---
layout: page
title: Visuals
nav-label: Visuals
permalink: /visuals/
---

##EDA Visuals

<div>
  <h3>reddit Comment Upvotes</h3>
  <img img width="564" alt="commenthist" src="../images/commenthist.png">
</div>

<div>
  <h3>Article Comment Upvotes</h3>
  <img img width="564" alt="articlehist" src="../images/articlehist.png">
</div>


As we see here, the reddit comment upvotes are very much skewed to the right with most of the comments recieving few up votes. On the other hand, the article comments are a lot lest skewed than the reddit comments, and there are several peaks in the data that can be seen in the histogram. This suggests that the reddit comments and article comments are distributed quite differently when it comes to upvotes.

<div>
  <h3>Subreddits</h3>
  <img img width="564" alt="commentbar" src="../images/commentbar.png">
</div>

<div>
  <h3>Article Categories</h3>
  <img img width="564" alt="articlebar" src="../images/articlebar.png">
</div>


Here we see that the subreddits from the reddit comments have similar categories as the ones found in the articles. The rankings are slightly different with news being the highest category from the reddit comments and science being the highest category from the article comments. However, in general the two data set show similar subreddits.

<div>
  <h3>Similarities in Key Words </h3>
  <img img width="564" alt="keywordbar" src="../images/keywordbar.png">
</div>

Here we looked at how strong the similarity was between key words of reddit comments and article comments. It can be seen from the histogram that the similarity score is not very high with the majority concentrated on the lower end. This suggests that it may be difficult to rely on key word similarity for our model. However, there are some similarities that fall within the 0.4 to 0.6 range, and these may be the data points that we would want to analyze further in our predition model.
