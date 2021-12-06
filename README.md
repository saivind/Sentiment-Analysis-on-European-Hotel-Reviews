# Sentiment-Analysis-on-European-Hotel-Reviews

Sentiment analysis (also known as opinion mining or emotion AI) provides a very accurate analysis of the overall emotion of the text content incorporated from sources like Blogs, Articles, forums, consumer reviews, surveys, twitter etc. This analysis can be widely applied to reviews and social media for a variety of applications, ranging from marketing to customer service. In the post, we take the example of European Hotel Reviews dataset and demonstrate how this works.

This document is about the Sentimental Analysis of the Customer Reviews on some European Hotels. I have built a sentimental analysis model which will determine the review as a positive or a negative review. I have developed model using Logistic Regression and Navie Bayes. The accuracy of a sentiment analysis system is, in principle, how well it agrees with human judgments. This is usually measured by variant measures based on precision and recall over the two target categories of negative and positive texts.



![SA_2](https://user-images.githubusercontent.com/62845002/144871847-a8ece7b3-c331-4cb8-9c64-759a6c9467db.png)

In this report I am using a Hybrid approach where I can use both Machine Learning and Lexicon based approach. Here I take into consideration of a dataset ’Customer Reviews of the Hotels in Europe’ from kaggle.com. 

It is a 10000 rows of data with 20 columns. The main rows taken into consideration are positive and negative review and the ”Reviewer Score”.

Both the negative and positive reviews are combined and then Sentiment Analysis is done on them. Many reviews has either ’No positive’ or ’No negative’ which are removed in Data Preprocessing. The reviews are divided as Good or Bad based on the ”Reviewer Score”.

If the Reviewer Score is more that 8 than the review is considered Positive or Good else Bad or Negative. You can see how data is converted in Fig.(2). The Dataset consists of 5839 Positive reviews and 4160 Negative reviews.


![review_div_3](https://user-images.githubusercontent.com/62845002/144872474-a88395dd-94a5-4c3b-be9b-4128d65a85d0.png)

--- Data Preprocessing: ---

1. Converting sentences to lower case sentence (all the upper case letters will be changed to lower case)
2. Removing special characters (removes special characters like @, -, etc)
3. Removing stopwords and high/low-frequency words (like i, me, myself, you) 
4. Tokenize the text and remove punctuation (here we remove punctuation marks like ., , ,! etc and tokenise the remaining words i.e, separating the words)
5. Remove numbers ( remove any numbers in the review) 
6. Part-OfSpeech (POS) tagging: assign a tag to every word to define if it corresponds to a noun, a verb etc. using the WordNet lexical database with this library we can find the each word used is a verbs or noun and can be determined whether to remove or use the word for training the model to determine the review as good or bad.
7. Lemmatize the text: transform every word into their root form (e.g. rooms to room, slept to sleep)

![image](https://user-images.githubusercontent.com/62845002/144875232-f6106ee9-c9b2-4eac-ae11-512f4d0a3684.png)


After the Data Preprocessing is done the reviews words remaining will be divided into train and test data set with 30 percent as test data. 

The remaining training data(80percent) will be taken to train the different Machine Learning models like Logistic Regression, Navie Bayes, Support Vector Classifier(SVC), Decision Tree and Random Forest Classifier. 

After training with training data we predict the test data and measure the accuracy, which will help us in determining which model work better with the test data.

There are many evaluation metrics by which we can know which Machine Learning model works better with the test data.

Precision defines the proportion of reviews the system classified correctly to all reviews classified. 

Recall describes the proportion of reviews selected correctly to all reviews selected. An additional F-measure combines both precision and recall into a single measure by computing the harmonic mean. The F-measure uses a parameter controlling the influence of precision and recall.

 I have built the model for future reviews so we can enter any review in runtime and the model built will classify whether the review is a good or a bad one. I have tried it and the classifier is giving pretty good classification of reviews.
 
