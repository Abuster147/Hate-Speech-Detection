# Hate_Speech_Detection

## Introduction
***
Hate speech implies any form of content which expresses hate towards anything in a harsh manner. It can be in the form of both writing & speaking. Generally, on social media, there are some disturbing elements(especially fake accounts) that spread hatred targeting a specific domain ( it may be a person, group of persons, ideologies, or anything else) . Social Media sites face the problem of identifying and censoring problematic posts while weighing the right to freedom of speech. Hate speech detection is used to identify such texts/write-ups which express hate so that proper actions can be taken against it.

## Objectives
***
- To train a machine learning model which can recognize whether the text contains hate speech or not
-  Use the trained classifier on real-world speech to identify hate speech in the text

## Problem Statement
***
Train a classifier that classifies speech into two classes (Hate speech: 1, Non-hate : 0). <a href="https://www.kaggle.com/arkhoshghalb/twitter-sentiment-analysis-hatred-speech">Dataset</a> consisting of various tweets is used to train the model.

## Methodology
***
The method that we are going to use to achieve our objectives are detailed below in steps:
1. **Cleaning data :**
- Removed the Twitter handles associated with the tweets as these do not give any information about the sentiment of the tweet.
- Removal of special characters, symbols, punctuations is also necessary.
- Removal of all the short words ( word length <=3) as they do not convey much information. Stopwords such as I, he, him were also removed using the NLTK library. Decontraction of text was also performed.
- Lowercased the text data. While running the model on the uppercased texts, lower accuracy is obtained. 
- Eliminated the 20 most frequently occurring words along with 20 least frequent words from the dataset, as these helped in concentrating over the words which are of value in the tweet.

2. **Preprocessing data :**
- The words of the cleaned dataset are tokenized using a word tokenizer.
- Both stemming and lemmatization are applied over the word tokens and are stored.
- Thereafter we used methods such as BoW, Tf-If ( on both stemmed and lemmatized data)  in order to vectorize our data.

3. **Model :**

The preprocessed data is ready, various models such as Logistic Regression, Decision Tree, XGBoost and Random Forest are used to train the dataset.

**Results :**
***
Out of all the classifiers, the **Random Forest** model over the Tf-Idf Vectorizer on lemmatized tokens turned out to be the best. Accuracy of **0.95** is achieved over the test dataset.

 
 
