# reddit-posts-classification
This is an example of a data science workflow. I will guide you throw all the steps of the process. The purpose of this work is to create a classifier of posts on reddit.com using its API and tools of the python 3.6. As a result we will get a model that classifies the two selected categories with a high accuracy.

## 1. Define the problem.

Sometimes people do not know how to categorize their posts. So we can create a model that will offer people a category or we can automatically assign the category to the post after its publishing. I choose two pairs of subreddits: ‘games’ and ‘boardgames’ (similar topics); ‘cats’ and ‘dogs’ (different topics). It will show you how my model works on different types of subreddits.

## 2. Gather the data.

We use reddit.com API to collect necessary data. The API returns data in a .json format, so it is very easy to work with the data in python. It is because the .json format is similar to a python dictionary datatype.

## 3. Explore the data.

Now when we extracted the data from the .json format, we can explore it as well as prepare for further usage. First of all we need to lead all the text to a lower case. Then we delete unnecessary symbols, e. g. leave only letters in our text. Thirdly we lemmatize all the words. And at last we delete stop words (such as ‘a’, ‘the’, ‘and’ etc). Thus our text is ready to be converted into numbers. For this purpose we use a count vectorizer and a TFID vectorizer. We need to different vectorizers to be able to compare them and decide which is better.

## 4. Model the data

I tried a few different models of classifiers on both the count and the TFID vectorizers. I used such models as:

-Logistic regression
-Multinomial naive Buyes
-Decision tree
-Random forest
-Support vectors machine
All of this models are good but we will chose one of them for every of our tasks: for classifying of similar posts (‘games’ and ‘boardgames’) and different posts (‘cats’ and ‘dogs’) based on it’s accuracy.

## 5. Evaluate the model

For evaluation of different models we use different approaches as well, such as:

- Cross-validation
- Grid search

As a metrics we can use an accuracy, a sensitivity or a specificity. As I mentioned before in this project we use the accuracy as the main metric for estimating of our models. 

## 6. Answer the problem

As a result of my work on this project I got two working models for both pairs of similar and different topics. In both cases the best results shows count vectorizing. But classifiers are different: for ‘games’ and ‘boardgames’ pair the best result has the Multinomial Naive Buyes classifier (89% accuracy), and for the ‘cats’ and ‘dogs’ pair the best result has the Decision Tree classifier (98% accuracy). We can see that even for similar subreddits a machine learning approach gives pretty high results.

## Summary

In this project I had an opportunity to compare efficiency of different classification models, different vectorizers on two types of problem: classification of similar and different blogposts on reddit.com. On the both types of problem I have got high accuracy of classification so I am sure that the machine learning approach can and should be used for decision of such kind of problems.
