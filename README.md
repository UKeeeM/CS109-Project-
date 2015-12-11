<h1>Find Your Expert</h1>

<h2>Overview</h2>

Many of us are frequent reddit users, the so called “Front Page of the Internet”. Websites such as fivethirtyeight.com have taken note that reddit comment data is an interesting snap shot that shows how the internet users think and talk. Our group wanted to analyze what were the factors that went in to creating a reddit comment that is well liked by the community. We also wanted to explore the differences between the different subreddit communities and examine if their views were any similar. We also wanted to use newspaper articles found online as a benchmark to see how different online opinion fared aganist journalist opinions. We aimed to examine whether using features from reddit comments, and see if we could predict how well the comments will do. Also, if the parent thread of the comment stemmed from a news article, we tried to see if how well the comment does had any relations with how similar the comment is to the news article. Our work can be viewed through our <a href="http://ukeeem.github.io/CS109-Project-//">website</a> where final results from our prediction model is presented. In addition, our Google Chrome extension which can be found <a href="http://ukeeem.github.io/CS109-Project-//extension/">here</a> can be downloaded for easier user experience. Finally, for a quick walkthrough of our project, please watch our 2 min screencast here. 

<h2>Training Strategy</h2>
The overarching strategy of our application consists of two phases, a prediction phase and a training phase. The training phase results in a parametrized model to predict top comments. The prediction phase uses this model to predict the top comments for a particular article.
<br>
<br>
The following training strategy summarizes the work completed in the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Collection%20Factory.ipynb">**Collection Factory**</a>, the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Feature%20Factory.ipynb">**Feature Factory**</a>, the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/EDA.ipynb">**Exploratory Data Analysis** </a> and the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/model.ipynb">**Model Factory** </a>.

<img src="TrainingStrat.png">
<br>
<br>
In order to train our model we need to collect articles tha exist in the reddit verse and the top comments related to that article. The <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Collection%20Factory.ipynb">**Collection Factory**</a> uses the Reddit API to collect a broad range of article and thier associated comments. The <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Feature%20Factory.ipynb">**Feature Factory**</a> uses this data to create features regarding the article content, the comment content and the similarity between them. The features are designed to articulate the relationship between the comments and the interest article. The final features are the result of an iterative process of extraction, exploration and modelling. The majority of the feature exploration occurs in the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/EDA.ipynb"> **EDA notebook**</a>. 

The feature extraction, EDA, modelling cycle is a continuous loop. The best model produced is effectively related to the number of times this cycle is completed.

<h3>Collection Factory</h3>
The <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Collection%20Factory.ipynb">**Collection Factory**</a> is the mechanism for collecting all of the data required for the application. The factory makes use of the reddit API to identify a broad range of articles similar to those we are expecting to use for prediction. The factory collects the comments related to each particular article and then collects the article itself. 

<h3>Feature Factory</h3>
The <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Feature%20Factory.ipynb">**Feature Factory**</a> is the mechanism for extracting useful attributes from the comments, the articles and the relationship between them. Some of the features were created at collection time to reduce the amount of data that would be stored; but we expand on those features here. The premise of our application is that the top comments, will be syntactically similar to the articles they are describing. For example, comments and users that use the same language of the article may increase the overall score of that article. The feature factory produces a large variety of these comparisons and we use EDA to determine the ones with the most predictive power.

<h3>Exploratory Data Analysis</h3>
Our exploratory data analysis shows that there is great variation between the reddit comments and the online articles. In this part of our project we looked through both the dataset of the reddit comments and the online articles. We cleaned up the dataset and added some additional columns as well as run some preliminary visualizations on them. Ultimately we selected features that we thought would be interesting to look at and applied them to the dataset using the code from the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Feature%20Factory.ipynb">feature factory</a> and the <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/Collection%20Factory.ipynb">collection factory</a>. Our analysis of the feature implemented dataset tells us that similarities between reddit comments and online articles tend to be on the lower end. A more detailed analysis of our EDA can be seen <a href="https://github.com/UKeeeM/CS109-Project-/blob/master/EDA.ipynb">here</a>.
Also, our implementation of the wordcloud can be seen <a href = "https://github.com/UKeeeM/CS109-Project-/tree/master/Wordcloud"> here </a>

<h3>Model Factory</h3>
Our model was based primarily on the usage of NLTK library and the TfidfVectorizer class , as well as the MultinomialNB class. We filtered the commetns into tokenized sentences so that we can use it in our Naive Bayes classifier. We also normalized the upvote data, so that the huge variance in the upvote data would not be an issue. Ultimately, we found that it is difficult to do Natural Language Processing correctly to predict reddit comment's upvote sucess very accurately for the sucess case. 
A more detailed analysis of our model can be seen <a href ="https://github.com/UKeeeM/CS109-Project-/blob/master/Model.ipynb">here</a>


<h2>Prediction Strategy</h2>
The following process identifies our prediction strategy. This process that occurs when we predict the top comments for an interest article. The primary difference between the prediction strategy and the training strategy is the concept of an interest article. This is the article for which we want to identify the top comments. In the training strategy we were looking at the relationship between comments and the article they were discussing. For prediction we look at the relationship between comments and the interest article. 

<img src="PredictionStrat.png">
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


<h2>Website</h2>

Our website displays our final results as well as initial motivation and question. It also includes a walkthrough of our project in video and contains many visualizations displaying our results. Go <a href="http://ukeeem.github.io/CS109-Project-//">here</a> to visit our website.
* Extension
