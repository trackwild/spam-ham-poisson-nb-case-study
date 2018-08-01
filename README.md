# spam-ham-poisson-nb-case-study

## Part I

- Fork repo and clone
- Use `dev` branch
- Send pull request when complete

## Part II

- Download `spam.csv` dataset
- https://www.kaggle.com/uciml/sms-spam-collection-dataset
- Each entry is labeled as either `spam` or `ham` (not spam)
- We want to do hypothesis testing on this dataset

```
Let's imagine these are the messages in our inbox. Our hypothesis is 
that the percentage of spam in our inbox is greater than 12.5%.

Alpha is 0.025

Do we reject or not reject the null hypothesis? What's the p-value?
```

## Part III

- You will be using the Poisson Probability Distribution
- https://en.wikipedia.org/wiki/Poisson_distribution
- It is parameterized by lambda
- In `Part I` you figured out how many messages were spam
- Let's imagine that you receive that many spam messages every four weeks
- What's the probability that you will get at least 30 spam messages per day?

## Part IV

- You are a human spam detector.
- Create an interactive program that will randomly show you a message from the above list.
- You have to determine if it's spam or not (do not look at the label).
- Record your answer for a small sample of messages (about 10).
- How accurate were your predictions?
- How many Type 1 and Type 2 error did you have?

## Part V

In Part IV you were a spam detector. Let's see if we can automate this process and hopefully get better accuracy.

You will be creating a Naive Bayes Text Classification Model to determine if an incoming message is spam or not.

Here's some sample code:

```
from sklearn.feature_extraction.text import CountVectorizer
from sklearn.feature_extraction.text import TfidfTransformer
from sklearn.naive_bayes import MultinomialNB
from sklearn.model_selection import train_test_split
count_vect = CountVectorizer()
tfidf_transformer = TfidfTransformer()

counts = count_vect.fit_transform(LIST_OF_MESSAGES)  # change
tfidfs = tfidf_transformer.fit_transform(counts)

X_train, X_test, y_train, y_test = train_test_split(tfidfs, LIST_OF_LABELS, test_size=0.33, random_state=42) #change

nb = MultinomialNB().fit(X_train, y_train)
predictions = nb.predict(X_test)
```

- What is the baseline accuracy?
- What is the accuracy from your trained model?
- How many Type 1 and Type 2 errors occurred?
- What performed better, the Human or NB model?
