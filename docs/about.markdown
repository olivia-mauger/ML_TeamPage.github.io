---
layout: page
title: About
permalink: /about/



"""Our team will be utilizing machine learning for the purpose of sentiment analysis on social media posts. Specifically, we will be using a database of over 200,000 reddit posts, which have been labeled for suicidal content, in order to train a machine learning model to recognize suicidal and depressive social media posts. We hope that the advanced detection of severe mental health concerns via the application of such a model can allow for proactive preventative action to be taken in order to protect at-risk individuals from self-harm.
Existing research has delved into the field of sentiment analysis and depression, but has not applied machine learning to these efforts. A 2016 study developed a sentiment analysis tool which analyzed the text content of Twitter posts for depressive sentiment vocabulary. If this tool determined that a user’s posts were of a depressed sentiment, it notified social workers or designated care persons to prevent these at-risk users from harming themselves. This study used the lexicon approach to sentiment analysis, which classifies posts based purely on the vocabulary they contain. (Tao et al., 2016) We believe we can improve upon this approach by utilizing machine learning to better understand context and thus more accurately classify posts. 
We believe that the issues of suicide and depression are a poignant problem plaguing modern-day society. As we have become more interconnected via the internet, we have become increasingly disconnected from other humans. This reduction of direct social interactivity has yielded rapidly increasing rates of mental health concerns. We hope that our project can act as a means to detect depression at an early stage, and direct depressed individuals to the resources they need to aid their mental health before these issues escalate further.




To classify a post to be suicidal or non-suicidal, the multinomial naive Bayes classifer will be used. The posts will be processed into lists of words with the order being assumed to not matter. Since the order does not matter, the following classifier equation will be used:
CNB=P(y)i=1nP(xi|y)
P(xi|y) represents the probability of a word xi in the post given the classification of suicidal or non-suicidal y. P(y) represents the prior probability of the classifier y. 
To furthermore increase the efficiency of the classifier CNB, the features will be considered in terms of log: 
CNB=logP(y)+i = 1nlogP(xi|y)

For each post the CNB will be calculated for both classifiers, with the great CNB determining the category the post will be classified as.


P(y) will be initially estimated to be the percentage of class y posts in the dataset and P(xi|y) will be initially estimated to be the percentage of xi words given class y in the dataset. 


This classifier uses the  conditional probability of each word in both possible classification (suicidal or non-suicidal) to predict the classification of the post. The formula used for this classification is:
P(y|x,...,xn)=P(y)i=1n(xi|y)P(xi) . In the formula, y represents the resulting condition which would be if the written text is suicidal or not. The x variables are the events which would be the words within the text. The overall steps involved include creating a frequency table for how frequent each words appear and then creating a frequency table of the probability for each word given that the post is suicide or not. From this, the posterior probability can be calculated which is the probability of the resulting condition given the features. After calculating each posterior probability, you assign the resulting condition to the events according to the one with the higher probability.

In order to determine the success of our project, our primary metric is percent accuracy in predicting if posts contain suicidal content. One recent study examining the accuracy of different sentiment analysis classifiers reported a 85.48% accuracy for the Naive Bayes approach, which is our starting point [CITE-LIZ]. Therefore, we will consider accuracy above 80% to be a reliable final result. This may shift if we decide to implement a different approach. 
Accuracy is the most important metric for us to collect because both false positives and false negatives could have drastic effects for the health and safety of those involved in the posts.This is not a subject matter that should be treated lightly. """



---

This is the base Jekyll theme. You can find out more info about customizing your Jekyll theme, as well as basic Jekyll usage documentation at [jekyllrb.com](https://jekyllrb.com/)

You can find the source code for Minima at GitHub:
[jekyll][jekyll-organization] /
[minima](https://github.com/jekyll/minima)

You can find the source code for Jekyll at GitHub:
[jekyll][jekyll-organization] /
[jekyll](https://github.com/jekyll/jekyll)


[jekyll-organization]: https://github.com/jekyll
