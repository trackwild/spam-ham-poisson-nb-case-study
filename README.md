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
- Record your answer for each message.
- How accurate were your predictions?
- How many type 1 and type 2 error did you have?

## Part V


