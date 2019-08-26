# Classification Project - Online News Popularity

Checking the popularity of different online news posts.

Data Set Information:

* The articles were published by Mashable (www.mashable.com) and their content as the rights to reproduce it belongs to them. Hence, this dataset does not share the original content but some statistics associated with it. The original content be publicly accessed and retrieved using the provided urls. 
* Acquisition date: January 8, 2015 
* The estimated relative performance values were estimated by the authors using a Random Forest classifier and a rolling windows as assessment method. See their article for more details on how the relative performance values were set.

We have assumed that the most popular posts are shared the most and calculated the average number of posts as 3501.
We have also divided the data into 2 classes 
- class-4(popular posts, if the average number of posts>3501) and 
- class-2 (not-so-popular posts, if the average number of posts<=3501)
We intend to anticipate the popularity(class) of the post and it is our target variable.


### Data Source - UCI
Data source link - https://archive.ics.uci.edu/ml/datasets/Online+News+Popularity#

# Model Summary
The Accuracy score for the reduced dataset is similar or somewhat better than the score of the unreduced dataset(exception - Logistic Regression, where the Accuracy rate for the unreduced data is 88.93% which is better than 87.3% for the unreduced dataset and also Decision Tree Models).

We have used 2 PC for our different models. There is not much difference in the scores for the reduced and unreduced data, maybe because we have taken fewer number of Principal Components.

We also noticed that there is a huge variance that is being explained by the Eigen Vectors.

| Voting Classifers Scores | Hard Voting | Soft Voting |
| --- | --- | --- |
| Train | .85 | .86 |
| Test | .89 | .89 |

Soft Voting has better score than Hard Voting.

| Bagging Scores | DTree | Logistic Regression |
| --- | --- | --- |
| Train | .84 | .84 |
| Test | .89 | .89 |

There is no difference in the Train and Test Scores for both the models.

| Pasting Scores | RBF | Linear |
| --- | --- | --- |
| Train | .84 | .84 |
| Test | .89 | .89 |

There is no difference in the Train and Test Scores for both the models.

| Pasting Scores | DTree without Depth | DTree with max_depth - 5 |
| --- | --- | --- |
| Train | .84 | .93 |
| Test | .89 | .87 |

This is a case of overfitting for the DTree with max_depth=5

Gradient Boosting Classifier

Train Score - 0.8472 , Test Score - 0.8814






### ANN

The Artificial Neural Network has also given us a good enough Accuracy Score for our model(87.31%), which is in sync with the accuracy scores of our other models so the perceptron model is said to be working for our dataset.
