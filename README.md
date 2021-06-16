# COVID-19-Tweet-Sentiment-Analysis

# Problem Description 

This challenge asks you to build a classification model to predict the sentiment of COVID-19 tweets.The tweets have been pulled from Twitter and manual tagging has been done then.
The names and usernames have been given codes to avoid any privacy concerns.

# Data Description

You are given the following information:
Location
Tweet At
Original Tweet
Label

COVID-19 originally known as Corona VIrus Disease of 2019, has been declared as a pandemic by World Health Organization (WHO) on 11th March 2020. Unprecedented pressures have mounted on each country to make compelling requisites for controlling the population by assessing the cases and properly utilizing available resources. The rapid number of exponential cases globally has become the apprehension of panic, fear and anxiety among people. The mental and physical health of the global population is found to be directly proportional to this pandemic disease. It is the need of the hour to implement different measures to safeguard the countries by demystifying the pertinent facts and information.


# Workflow
![image](https://user-images.githubusercontent.com/47490381/121369336-61804280-c959-11eb-92ed-f05566ff69fb.png)

# Patterns/Trends 

## Null values in Location column
![image](https://user-images.githubusercontent.com/47490381/121406127-6ce46580-c97b-11eb-891b-6eb647fac9ac.png)

## Number of unique values
![image](https://user-images.githubusercontent.com/47490381/121406296-9a311380-c97b-11eb-8e2c-e1740c6302d5.png)

## Number of tweets as per days of the month
![image](https://user-images.githubusercontent.com/47490381/121406428-c2207700-c97b-11eb-8fc8-a23b6060bbf1.png)

## Tweet sentiment count
![image](https://user-images.githubusercontent.com/47490381/121406533-dfeddc00-c97b-11eb-9a74-f3bb7e6bc370.png)

# Data Preprocessing

The preprocessing of the text data is an essential step as it makes the raw text ready for mining.

The objective of this step is to clean noise those are less relevant to find the sentiment of tweets such as punctuation, special characters, numbers, and terms which don’t carry much weightage in context to the text.

As mentioned earlier, the tweets contain lots of twitter handles (@user). We will remove all these twitter handles from the data as they don’t convey much information.

We have analyzed that most of the tweets are like #coronavirus #covid-19 and this tweets are almost present in all the sentiments. So there is no use of keeping these hashtags in text. It will make the data noisy and which will affect accuracy of model.

We are having twitter links in the data which are not useful for our Model. It will make our data noisy.

As discussed, punctuations, numbers and special characters do not help much. It is better to remove them from the text just as we removed the twitter handles,links and hashtags.

Stop words are those words in natural language that have a very little meaning, such as "is", "an", "the", etc.To remove stop words from a sentence, you can divide your text into words and then remove the word if it exits in the list of stop words provided by NLTK.

Stemming is a rule-based process of stripping the suffixes (“ing”, “ly”, “es”, “ed”, “s” etc) from a word. For example – “play”, “player”, “played”, “plays” and “playing” are the different variations of the word – “play”.

Lemmatization is a more powerful operation, and it takes into consideration morphological analysis of the words. It returns the lemma which is the base form of all its inflectional forms.

In tokenization we convert group of sentence into token . It is also called text segmentation or lexical analysis. It is basically splitting data into small chunk of words. Tokenization in python can be done by python NLTK library’s word_tokenize() function.

## Hastags count
![image](https://user-images.githubusercontent.com/47490381/121406723-1f1c2d00-c97c-11eb-86f6-fcecb6ede885.png)

# Model Evaluation
![image](https://user-images.githubusercontent.com/47490381/121406818-41ae4600-c97c-11eb-91a6-e9299fcc0dbd.png)

# Conclusion
For multiclass classification, the best model for this dataset would be CatBoost with test accuracy of 0.62.
