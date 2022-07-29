# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

## Problem Statement
---
Reddit is a network of communities where users can share news content or comment on each other posting. As there are over 1.5 million subreddits on reddit. Given that users can post on anything on any of the subreddits, Moderator will have difficulties to visually going into all posting to ensure that postings are relevant to the respective subreddit. The objective of this project is to use machine learning to create a classification model and see how well that can it distinguish the postings and re-classify the posts to the respective subreddit or remove it.  As such I picked two closely-related subreddits for the challenge.

## Contents
---
- [Executive Summary](#Executive-Summary)
- [Data Collection](#Data-Collection)
- [Data Cleaning and EDA](#Data-Cleaning-and-EDA)
- [Preprocessing and Modeling](#Preprocessing-and-Modeling)
- [Conclusion and Recommendations](#Conclusion-and-Recommendations)

## Executive Summary
---
Reddit is a network of communities where users can share news content or comment on each other posting. As there are over 1.5 million subreddits on reddit. Given that users can post on anything on any of the subreddits, Moderator will have difficulties to visually going into all posting to ensure that postings are relevant to the respective subreddit. The objective of this project is to use machine learning to create a classification model and see how well that can it distinguish the postings and re-classify the posts to the respective subreddit or remove it.  

In this project Web scrapping from the net with API as the data collection, Data cleaning and EDA is the part and parcel for data analysis. We used 4 modeling together with GridSearchCV to fine tune the model scoring.

he Logistic Regression with CountVectorizer has the best predictive performance on the classification problem. On top of that, it has a relatively low False Negative (Type II error) whereby we predicted that post to be cryptocurrency, but in fact, the post is relating to bitcoin. Hence, we would have to look at the Sensitivity (TP/(TP+FN)), the lower the FN, the higher the Sensitivity.

We could further apply it into the system a the first validation for system to pass thur as related posting for create a expectional listing that need further human intervention. 


## Data Collection
---
- Create a function using the Pushshift's API to search for all publicly available *submissions* on reddit.
- Focused on the epoch time, so that we do not need to rescrap data that has been collected.
- Export the dataframes for each subreddits into a csv file.
- The subreddits:
    - Cryptocurrency
    - Bitcoin 
- Fields that were collected to address our problem statement.

| fields | description |
| --- | --- |
|subreddit| the name of the subreddit|
|selftext| the content of the post |

## Data Cleaning and EDA
---
- Identified and handled missing values and outliers
- Created a function to clean the outliers
- Explored and described some distributions and summary statistics

## Preprocessing and Modeling
---
- Preprocessing
    - Lemmatizing
    - CountVectorizer
    - TfidfVectorizer
- Modeling through Pipeline
    - Baseline Accuracy Score 
    - Multinomial Naïve Bayes
        - GridSearchCV for hyperparameters optimization
        - Confusion Matrix Plot
    - Logistic Regression
        - GridSearchCV for hyperparameters optimization
        - Confusion Matrix Plot
- Evaluation
    - The best model would be based on the `Accuracy`, in addition `Sensitivity` would also be referenced.
    
## Conclusion and Recommendations
---
|#| Vectorizer | Model | Best Score | Train Score | Test Score (Accuracy) | FN|
|---|---|---|---|---|---|---|
|1|CountVectorizer|Multinomial Naïve Bayes|0.7994|0.8392|0.8021|0.8398|
|2|TfidfVectorizer|Multinomial Naïve Bayes|0.8296|0.8842|0.8296|0.9089|
|3|CountVectorizer|Logistic Regression|0.8845|0.9973|0.877|0.9089|
|4|TfidfVectorizer|Logistic Regression|0.8837|0.9838|0.8735|0.906|

**Model Selection: Logistic Regression with CountVectorizer**

All the models here outperformed the baseline accuracy score of 0.654. As the focus is on getting as many correct prediction as possible. The Logistic Regression with CountVectorizer has the best predictive performance on the classification problem. On top of that, it has a relatively low False Negative (Type II error) whereby we predicted that post to be cryptocurrency, but in fact, the post is relating to bitcoin. Hence, we would have to look at the Sensitivity (TP/(TP+FN)), the lower the FN, the higher the Sensitivity. Through the research, we were able to address some other problems such identifying many common words at appear in both post, and strong coefficent features. We could further apply it into the system a the first validation for system to pass thur as related posting for create a expectional listing that need further human intervention. 

Moving forward, we could potentially include more other relevant modelling such as random forest, Knn or decision tree to further analysis is there even better modelling for this dectection to minimise the need for human intervention. In addition, image posts were not taken into account, this could be tapped on given that our current generation usually prefers to post memes instead. Lastly, a more detailed study on the True Negative (TN) would also provide insights for us to see how can we use that to improve the predictions.
