# Sentimental-Analysis-of-Airline-Tweets-for-Recommendation
@author: NIXON ABRAHAM
Project Objective:

Scrape data from Twitter on 6 different US airlines and perform sentimental analysis based on text, retweet and negative keywords. Thereafter perform collective and individual sentiment analysis of airlines. Train data to project sentiment using random forest algorithm. Sentiment analysis helps companies in their decision-making process. For instance, if public sentiment towards a product is not so good, a company may try to modify the product or stop the production altogether in order to avoid any losses.

Data Scraping/ Data Collection: Data set was created using python to connect with Twitter API after passing authentication key like customer and secret keys. Using Twitters tweepy package is used to filter out the necessary attributes of each airline, this data will be present in csv format using the pandas library and presented in tabular format inserted into a data frame.

Data Cleaning:

Tweets contain many slang words and punctuation marks. Tweets need to cleaned before they can be used for training the machine learning model. However, before cleaning the tweets, divide our dataset into feature and label sets.
The feature set will consist of tweets only. If we look at our dataset, the 11th column contains the tweet text. Note that the index of the column will be 10 since pandas columns follow zero- based indexing scheme where the first column is called 0th column. Our label set will consist of the sentiment of the tweet that we have to predict. The sentiment of the tweet is in the second column (index 1). To create a feature and a label set, we can use the iloc method off the pandas data frame.
Remove all the special characters, remove all single characters, remove single characters from the start, substituting multiple spaces with single space, removing prefixed 'b', converting to Lowercase

Representing Text in Numeric Form:

Python's Scikit-Learn library contains the TfidfVectorizer class that can be used to convert text features into TF-IDF feature vectors.
We define,
The max features should be 2500, words that occur less frequently are not very useful for classification. Max df specifies that only use those words that occur in a maximum of 80%. min- df is set to 7 which shows that include words that occur in at least 7.

Training of Model (0.2 test data):

Random Forest Classifier machine learning algorithm of sklearn package will be used. Enabling fit method on the Random Forest Classifier class and pass it our training features and labels, as parameters.

Prediction and model evaluation:

For prediction will use the predict method on the object of Random Forest Classifier.
The performance of the machine learning models, we can use classification metrics such as a confusion metrix, F1 measure, accuracy, etc.

author : NIXON ABRAHAM
