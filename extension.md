---
layout: page
title: Google Chrome Extension
nav-label: Extension
permalink: /extension/
---

Source Files: <a target="_blank" href="https://github.com/UKeeeM/CS109-Project-/tree/expert-app">Found here</a>

### Install instructions

1. Clone this repo and switch to the the "expert-app" branch

2. Open your Chrome browser and type "chrome://extensions/" in the navigation bar

3. Make sure developer mode is checked

4. Click "Load unpacked extension"

5. Navigate to the cloned repo directory and select the "extension" folder within it

6. Visit a news article and click the expert icon

### Goals & Info

The goal of the Chrome Extension is to provide a user interface for individuals surfing the web to find experts and relevant information on the content that the user is viewing.

There are three components to the extension:

<b>1. Keyword Scraping</b>

The first step in the process is to understand what the article / web content is about.  We decided to use Python's Natural Language Toolkit.  To implement this toolkit, we used <a target="_blank" href="https://github.com/codelucas/newspaper">Newspaper</a>, a module specifically built for web content.  The Chrome Extension (using AJAX) passes the HTML content to the server, which then parses the content for keywords.  These keywords are used in the following two steps.

<b>2. Trending Data</b>

The goal of the project is to help individuals become experts at a particular topic by presenting them with relevant information and exposing them to other experts on the topic.  One piece of useful information is how the topic has trended over time.  For this, we used Google Trends Data.  We found this <a target="_blank" href="http://stackoverflow.com/questions/7805711/javascript-json-google-trends-api">page</a> useful.  The data is pulled from google.  The chart is produced using a javascript charting tool called <a href="http://www.highcharts.com/">HighCharts</a>.  Once the server determines the keywords for the content, it uses those keywords to extract trending data from Google.  The server then passes that data back to the Chrome Extension, which uses HighCharts to produce the graph.

<b>3. Expert finder</b>

At this time, the extension uses the <a href="https://www.reddit.com/dev/api">Reddit API</a> to find posts relevant to the keywords.  Once the server determines the keywords for a some web content, it passes those terms to the query field in a Reddit API call.  The first thing returned are relevant posts.  After receiving the post, a subsequent call is made to extract comments for those posts.  The highest rated post are used to determine who an expert is.
