---
layout: page
title: Visuals
nav-label: Visuals
permalink: /visuals/
---

##EDA Visuals

<div>
  <h3>reddit Comment Up Votes</h3>
  <img img width="664" alt="commenthist" src="../images/commenthist.png">
</div>

<div>
  <h3>Article Comment Up Votes</h3>
  <img img width="664" alt="newarticlehist" src="../images/newarticlehist.png">
</div>

As we see here, the reddit comment up votes are very much skewed to the right with most of the comments recieving few up votes. On the other hand, the article comments are a lot lest skewed than the reddit comments, and there are several peaks in the data that can be seen in the histogram. This suggests that the reddit comments and article comments are distributed quite differently when it comes to up votes. Furthermore, it is interesting to note that the 95th percentile cut off is a lot higher for the article comments than for the reddit comments as the reddit comments 95th percentile cut off is at 119 upvotes, and the article comments is at 6367.6 up votes.

<div>
  <h3>Percent of 95th Percentile & Above reddit Comments vs Time</h3>
  <img img width="664" alt="perhourreddit" src="../images/perhourreddit.png">
</div>

It is seen here that during the hours between 60 and 70 we have the highest percentage of reddit comments posted from the 95th percentile, thus suggesting that there may be a time of the day where more comments are likely to get up votes than other times. It is also interesting to note that the curve shown above is roughly a very pointy bell curve with the two ends having some of the lowest percentage of 95th percentile comments.

<div>
  <h3>Percent of 95th Percentile & Above Article Comments vs Time</h3>
  <img img width="664" alt="perhourarticle" src="../images/perhourarticle.png">
</div>

Here for the article comments, it can be seen that no apparent correlation exist between percentage of comments in the 95th percentile and above and the time in which the comments were posted. Thus, suggesting that the up votes for popular article comments are posted quite randomly, unlike what we saw with the overall reddit comments. Although it is interesting to note that the highest percentage of highly voted comments here are mostly posted in the range of 40 to 60, which is similar to that of the reddit comments.

<div>
  <h3>Subreddits</h3>
  <img img width="664" alt="commentbar" src="../images/commentbar.png">
</div>

<div>
  <h3>Article Categories</h3>
  <img img width="664" alt="articlebar" src="../images/articlebar.png">
</div>

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

<h3>Subreddit Categories</h3>

<div>
<table>
<tr>
<td>CANADA POLITICS<img alt="canadapolitics" src="../images/CanadaPolitics wordcloud.png"></td><td>CONSERVATIVE<img alt="conservative" src="../images/Conservative wordcloud.png"></td>
</tr>
</div>
<div>
<tr>
<td>DOCUMENTARIES<img alt="documentaries" src="../images/Documentaries wordcloud.png"></td><td>FOOD<img alt="food" src="../images/food wordcloud.png"></td>
</tr>
</div>
<div>
<tr>
<td>GADGETS<img alt="gadgets" src="../images/gadgets wordcloud.png"></td><td>INTERNET IS BEAUTIFUL<img alt="internetisbeautiful" src="../images/InternetIsBeautiful wordcloud.png"></td>
</tr>
</div>
<div>
<tr>
<td>LIBERAL<img alt="liberal" src="../images/Liberal wordcloud.png"></td><td>NBA<img alt="nba" src="../images/nba wordcloud.png"></td>
</tr>
</div>
<div>
<tr>
<td>NEWS<img alt="news" src="../images/news wordcloud.png"></td><td>NFL<img alt="nfl" src="../images/nfl wordcloud.png"></td>
</tr>
</div>
<div>
<tr>
<td>NOT THE ONION<img alt="nottheonion" src="../images/nottheonion wordcloud.png"></td><td>POLITICS<img alt="politics" src="../images/politics wordcloud.png"></td>
</tr>
</div>
<div>
<tr>
<td>PROGRAMMING<img alt="programming" src="../images/programming wordcloud.png"></td><td>SCIENCE<img alt="science" src="../images/science wordcloud.png"></td>
</tr>
</div>
<div>
<tr>
<td>SOCCER<img alt="soccer" src="../images/soccer wordcloud.png"></td><td>SPACE<img alt="space" src="../images/space wordcloud.png"></td>
</tr>
</div>
<div>
<tr>
<td>TECHNOLOGY<img alt="technology" src="../images/technology wordcloud.png"></td><td>TODAY I LEARNED<img alt="todayilearned" src="../images/todayilearnedwordcloud.png"></td>
</tr>
</div>
<div>
<tr>
<td>UK POLITICS<img alt="ukpolitics" src="../images/ukpolitics wordcloud.png"></td><td>UPLIFITING NEWS<img alt="upliftingnews" src="../images/UpliftingNews wordcloud.png">
</tr>
</div>
<div>
<tr>
</td><td>US POLITICS<img alt="uspolitics" src="../images/uspolitics wordcloud.png"></td><td>WORLD NEWS<img alt="worldnews" src="../images/worldnews wordcloud.png"></td>
</tr>
</table>
</div>

Here we see a variety of different word clouds for each of the subreddit cateogires that we studied. We used these word clouds to visualize the key words used in each of the subreddits. Key words played an important role in our prediction model, as we used the key words to predict the different subreddit topics.
