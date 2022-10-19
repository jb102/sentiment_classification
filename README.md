# sentiment_classification
Sentiment classification of Tweets using SVM (implemented in Sci-Kit Learn) and Naive Bayesian classifier (implemented from scratch). Three sentiment categories: positive, negative and neutral.

# Preprocessing

The preprocessing of tweets in the training and testing sets involved removing standard
noise as well as several elements which frequently appear in social media posts but are
not valuable for determining sentiment. These include:
• URLs
• Tags of other users (@ symbol followed by alphanumeric text)
• Hashtags (# symbol followed by alphanumeric text)
• Words that only contain non-alphanumeric characters
• Words with only a single character
The tokens (split on whitespace) are lemmatised using the Python NLTK library's WordNetLemmatizer, and stopwords are removed (by comparing with NLTK’s stopwords inventory).

# SVM

The SVM classifier was implemented using Sci-Kit Learn’s SVM model. The data was vectorised using the TfidfVectorizer class.
Shown below are the results from running this model on the same test sets.
-----------------------------------
| Test set             | F1 Score |
-----------------------------------
|twitter-dev-data.txt  | 0.577    |
-----------------------------------
|twitter-test1.txt     | 0.498    |
-----------------------------------
|twitter-test2.txt     |0.522     |
-----------------------------------
|twitter-test3.txt     |0.495     |
-----------------------------------


