# Twitter-Sentiment-Analysis
![hate speech](https://github.com/AbeerMahjoub/Twitter-Sentiment-Analysis/blob/main/hate-speech.jpg)

# Overview:

**Detecting hate speech in social media became a crucial task. This project objective is to be able
to detect tweets that contain hate speech such as sexist or racist tweets etc..**

# Data:

The data consists of  31962 tweets with their labels. Only 7% of the tweets are classified as hate speech.

![dist](https://github.com/AbeerMahjoub/Twitter-Sentiment-Analysis/blob/main/graphs/Dist_Label.png)

Data Resource: [Kaggle](https://www.kaggle.com/datasets/arkhoshghalb/twitter-sentiment-analysis-hatred-speech?datasetId=100982&sortBy=voteCount)

# EDA:
## Non-Negative Tweets Word Cloud:
![Non Negative Word Cloud](https://github.com/AbeerMahjoub/Twitter-Sentiment-Analysis/blob/main/graphs/nonnegcloud_clean.png)

## Negative Tweets Word Cloud:
![Negative Word Cloud](https://github.com/AbeerMahjoub/Twitter-Sentiment-Analysis/blob/main/graphs/negcloud_clean.png)

## Cleaning and processing the text includes:

- Removing words that aren't part of the tweet as the user handle which was encoded as "user".
- Removing Emojies from text.
- Deleting Markup language and links.
- Lower casing the words.
- Removing stop words.
- Lemmatization.

## Feature Engineering:

Some features are added:
- Count of words in each tweet.
- Count of stop words in each tweet.
- Count of hashtgs in each tweet.

# Modeling Pipe line:

We used tfidf transformer to vectorize the text then we solved the imbalanced problem by oversampling and undersampling together.
then we passed the vectors to:

1- Naive Bayes Classifier - AUC score of .87

2- Random Forest Classifier - AUC score of .94

