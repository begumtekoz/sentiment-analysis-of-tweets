# Sentiment Analysis of Tweets in the UK/ USA

The digitalization of life with COVID-19 affected everyone to some extent. Especially the education area with the most interaction was interrupted by the arrival of the quarantine. That's why this area started to digitalize and transform. Online education models have improved considerably in recent years, especially since universities are more familiar with this subject.

In this study, we will examine people's thoughts about online education and COVID-19 with tweets from certain regions. Population density in the areas we chose would create a significant bias. Fixing the random number of tweets will create an unbiased environment in the study. It contains the last hundred tweets posted in London and New York until 12.11.2020.

## *Data taken from USA and UK*


We first took the simplified version of the text. This json made it easy to convert the attributes we chose to csv. 
Twitter data taken from America is above. We checked how many attributes and observations this data consists of. The dimensions of the data are 100 and 8. That means, there are 100 tweets and 8 attributes.

Although the data was taken in English, the language of the data was checked again. According to the result, all of the tweets' language is English.


The most important part of the data to be analyzed is the text part. Although we tried to simplify the data in previous codes, the data contains too many elements. Therefore, the things that break the text integrity in the text are transferred to other columns. This transferred data also contains important information. This will be studied in the following sections of this analysis. Hashtags and links in the text have been transferred to new columns. And most importantly, the cleaned data is in a new column called clean_text.


## *Basic Natural Language Processing (NLP)*


At this stage after organizing our data, Basic Natural Language Processing was consulted. Transactions were made using the NLTK package.

The TweetTokenizer enables us to split text into small units. This tokenization process takes place according to the gaps in the data. It is applied this process to "clean_text" and "hashtags" in our data.

Words in sentences are an important step in understanding the sentence. In addition, it is important to examine the root of the word after tokenization. This was done with the Snowball Stemmer algorithm in NLTK. It is checked if stemming works in the code below.

Using root may not always give the correct result. Therefore, it would be more logical to do lemmatization instead of stemming. The aim here is to find the tag of the word via postag's instead of taking the root word. Like Adjective noun.

It is normalized by using this code and it creates normalized tweets and retrieves biagrams.

## *Sentiment Analysis*

Analysis was performed using NLTK's sensitivity analyzer using the VADER tool and dictionary. Emotion rating is evaluated between 1 and -1.
After measuring the sentiment of the tweets, we rated it by adding a new column to the data. This rating is negative if sentiment is less than 0, positive if greater than 0, and neutral if equal.

## *Exploratory Data Analysis*

Descriptive Statistics which illustrates the aspect of the dataset can enable us to understand the structure of the data and create research questions in the following part of the analysis.
## *Most Common 10 Hashtags*


Hashtags in raw data were in the text column. Hashtags are counted made into a list and converted to the data frame.

## *Most common 10 words in Tweets*

In the raw data, the text was full of links and hashtags. The data was cleared and  transferred to a new column, tokenized. The most repetitive words are counted put into a list and converted into a data frame.

## *The Distribution of Text Length*


Uncleaned data contained URLs and hashtags. The main text written by separating them above has been reached. The number of characters, which is an important factor for Twitter, was calculated in both data and added to the data.
To illustrate it, the minimum and the maximum values of length UK are 58 and 267 respectively. The mean of length Uk is a lower value than the median. Moreover, the variability is calculated by using the interquartile range which is the difference between the 1st quartile and the 3rd quartile. It is equal to 81.25.

## *Statistical Analysis*

Multiple Logistic Regression is applied to the effect of covariates on a binary response. It uses the logit function and models the odds of success.




