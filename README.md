# Twitter-Sentiment-Analysis
 The aim of this project is to analyze the sentiments of people's tweets and Visualizing them.

It is no longer difficult to understand what people think about a topic by analysing the tweets shared by people. 
Sentiment analysis is one of the most popular use cases for NLP (Natural Language Processing).

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/0.png)

Here, we are going to utilize the “Tweepy” library which is an easy-to-use Python library for accessing the Twitter API. 

> A Twitter developer account is also required, to get authorised in order to use the twitter API.
 
 ### 1. Installing and Importing Libraries
 Before analysis, we need to install textblob and tweepy libraries using !pip install command on our Jupyter Notebook.
 
And we need to import libraries that we will use in this sentiment analysis project later on.

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/1.png)

Tweepy supports both OAuth 1a (application-user) and OAuth 2 (application-only) authentication. Authentication is handled by the tweepy.AuthHandler class.

OAuth 2 is a method of authentication where an application makes API requests without the user context.

### 2. Authentication for Twitter API

After our authentication, we need to use tweepy to get text and use Textblob to calculate positive, negative, neutral, polarity and compound parameters from the text.

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/2.png)

Here, everyone will have their unique
- consumerKey
- consumerSecret
- accessToken
- accessTokenSecret

These are hidden for security reasons.

### 3. Getting Tweets With Keyword or Hashtag

In this scenario, the keyword or hashtag **"covid"** is used and the number of tweets to analyse are 2000.

The number of tweets parameter is important because of the limit.

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/3.png)

After getting 2000 tweets about **“covid”**, let’s have a look number of tweets that which sentiments:

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/4.png)

We put 2000 tweets and;

- 561 of tweets include positive sentiment
- 491 of tweets include negative sentiment
- 948 of tweets include neutral sentiment

### 4. Creating PieChart

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/5.png)

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/6.png)

### 5. Cleaning Tweets to Analyse Sentiment
When we look tweet list we can see some duplicated tweets, so we need to drop duplicates records using drop_duplicates function.

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/7.png)

Our new data frame has 1365 unique tweets.

Then, we create new data frame (tw_list) and a new feature(text), 
then clean text by using lambda function and clean RT, link, punctuation characters and finally convert to lowercase.

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/8.png)


### 6. Sentiment Analysis

Now, we can use cleaned text to calculate polarity, subjectivity, sentiment, negative, positive, neutral and compound parameters again. 
For all calculated parameters, we can create new features to my data frame

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/9.png)

We can now can split our data frame into 3 groups based on sentiment. 

For this one, creating 3 new data frame (tw_list_negative, tw_list_positive, tw_list_neutral) and import from original tw_list data frame.

We can also create a chart by using number of sentiment tweets.

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/10.png)

### 7. Function to Create Wordcloud

Now, we are going to create worcloud using 1365 tweets, So we can realize that which words most used in these tweets. 

To create a worcloud, firstly we'll define a function, 
so we can use wordcloud again for all tweets, positive tweets, negative tweets etc.

> We are going to create 3 wordclouds,
- Wordcloud for all tweets.
- Wordcloud for positive sentiment.
- Wordcloud for negative sentiment.

#### Wordcloud for all tweets.

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/11.png)

#### Wordcloud for positive sentiment.

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/12.png)

#### Wordcloud for negative sentiment.

![](https://github.com/samyakmohelay/Twitter-Sentiment-Analysis/blob/main/assets/13.png)
