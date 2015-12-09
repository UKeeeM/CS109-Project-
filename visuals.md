---
layout: page
title: Visuals
nav-label: Visuals
permalink: /visuals/
---

##EDA Visuals

<table>
<tr>
<td><h3>reddit Comment Up Votes</h3><img img width="464" alt="commenthist" src="../images/commenthist.png"></td><td><h3>Article Comment Up Votes</h3><img img width="464" alt="articlehist" src="../images/articlehist.png"></td>
</tr>
</table>

As we see here, the reddit comment up votes are very much skewed to the right with most of the comments recieving few up votes. On the other hand, the article comments are a lot lest skewed than the reddit comments, and there are several peaks in the data that can be seen in the histogram. This suggests that the reddit comments and article comments are distributed quite differently when it comes to up votes.

<table>
<tr>
<td><h3>Subreddits</h3><img img width="464" alt="commentbar" src="../images/commentbar.png"></td><td><h3>Article Categories</h3><img img width="464" alt="articlebar" src="../images/articlebar.png"></td>
</tr>
</table>

Here we see that the subreddits from the reddit comments have similar categories as the ones found in the articles. The rankings are slightly different with news being the highest category from the reddit comments and science being the highest category from the article comments. However, in general the two data set show similar subreddits.

<div>
  <h3>Similarities in Key Words </h3>
  <img img width="564" alt="keywordbar" src="../images/keywordbar.png">
</div>

Here we looked at how strong the similarity was between key words of reddit comments and article comments. It can be seen from the histogram that the similarity score is not very high with the majority concentrated on the lower end. This suggests that it may be difficult to rely on key word similarity for our model. However, there are some similarities that fall within the 0.4 to 0.6 range, and these may be the data points that we would want to analyze further in our predition model.

##Word Clouds

<table>
<tr>
<td><h3>Overall reddit Comments</h3><img alt="commenthist" src="../images/reddit.png"></td><td><h3>reddit Comments: 100 & Up</h3><img alt="articlehist" src="../images/reddit100.png"></td>
</tr>
</table>

Here we see a comparison of word clouds between reddit comments overall and the reddit comments who recieved an up vote of 100 or more. Between the two word clouds we can see that common words that show up in overall reddit comments do not differ much from the comments that recieved higher up votes. Thus suggesting that highly rated comments share similar key words as the overall comments.

<div>
<table>
<tr>
<td>CANADA POLITICS<img img width="264" alt="canadapolitics" src="../images/CanadaPolitics wordcloud.png"></td><td>CONSERVATIVE<img img width="264" alt="conservative" src="../images/Conservative wordcloud.png"></td><td>DOCUMENTARIES<img img width="264" alt="documentaries" src="../images/Documentaries wordcloud.png"></td>
</tr>
</div>
<div>
<tr>
<td>FOOD<img img width="264" alt="food" src="../images/food wordcloud.png"></td><td>GADGETS<img img width="264" alt="gadgets" src="../images/gadgets wordcloud.png"></td><td>INTERNET IS BEAUTIFUL<img img width="264" alt="internetisbeautiful" src="../images/InternetIsBeautiful wordcloud.png"></td>
</tr>
</table>
</div>
