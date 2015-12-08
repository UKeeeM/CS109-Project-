<h1>Find Your Expert</h1>

<h2>Overview</h2>

Many of us are frequent reddit users, and so it occured to us that often times we do not neccessarily know what the best comments are on certain posts. Despite having the upvote feature in reddit, our group wanted a more accurate way to determine the best comments. And so the goal of our project is to build an application that identifies the best comments for any article defined by the user. In order to provide the best and most relevent comments for articles that have somehow escapped the reddit verse, we first found similar articles that are related to the identified reddit post and from there we determined the best comments through a prediction model. Our work can be viewed through our <a href="http://ukeeem.github.io/CS109-Project-//">website</a> where final results from our prediction model is presented. In addition, our Google Chrome extension which can be found <a href="http://ukeeem.github.io/CS109-Project-//extension/">here</a> can be downloaded for easy user experience. 


<h2>Strategy</h2>
Explain differences between training and prediction objectives with links to notebooks, website

We first began our project by collecting data first from the reddit website, and then from articles of interest.....

<h2>Training</h2>
* Training Strategy
* Collection Factory
* Feature Factory
<h3>EDA</h3>

Our exploratory data analysis shows that there is great variation between the reddit comments and the online articles. In this part of our project we looked through both the dataset of the reddit comments and the online articles. We cleaned up the dataset and added some additional columns as well as run some preliminary visualizations on them. Ultimately we selected features that we thought would be interesting to look at and applied them to the dataset using the code from the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Feature%20Factory.ipynb">feature factory</a> and the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Collection%20Factory.ipynb">collection factory</a>. Our analysis of the feature implemented dataset tells us that similarities between reddit comments and online articles tend to be on the lower end. A more detailed analysis of our EDA can be seen <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/EDA.ipynb">here</a>.

<h2>Prediction</h2>
* Prediction Strategy
* Website
* Extension


