## Data Exploration and Cleaning# portfolio-part-3-mdazizulaman
portfolio-part-3-mdazizulaman created by GitHub Classroom
# E-commerce Dataset Analysis Report
## Introduction
In this portfolio analysis, we worked with an E-commerce dataset where user ratings were converted into binary values: 'like' (rating 1) and 'dislike' (rating 0). The goal was to build and evaluate predictive models like KNN to determine whether a user likes or dislikes an item based on other available features.

## Dataset Overview
**Columns**: The dataset consists of several columns, including userId, timestamp, review, item, helpfulness, gender, category, item_id, item_price, user_city, and rating.
## Data Exploration and Cleaning
**Exploration:** We started by exploring the dataset, checking for any abnormalities, and understanding the distribution of different features.
**Data Cleaning:** If necessary, we removed abnormal instances and handled missing values to ensure the dataset's quality.
## Feature Encoding
Encoding Categorical Features: We converted categorical features (e.g., gender, category) into numerical values using appropriate encoding techniques, such as OrdinalEncoder method. We found that most highly correlated feature in terms of rating is category with -0.14 where (-) sign indicates it's a negative correlation.On the other hand, least correlated feature in terms of rating is timestamp with -0.0097. Here, highly positive correlations are userId, Item, item_id, item_price while Category, Review, user_city and Gender correlations are highly negative.
## Correlation Analysis
**Correlation Matrix:** We studied the correlation between different features, especially their relationship with the 'rating' variable.
## Building Predictive Models
### Logistic Regression Model
**Data Splitting:** We split the dataset into training and testing sets.
**Model Training:** We trained a logistic regression model to predict 'rating' based on other features.
**Evaluation:** We evaluated the model's accuracy on the test set and found 0.6685288640595903.
**RFE:** We build RFE model where we use 3 best features and got 0.666666666666 accuracy but when we did the implementation based on rfe_support we found 0.6703910614525139 accuracy which is the best accuracy.
## K-Nearest Neighbors (KNN) Model
**Data Splitting:** Similar to logistic regression, we split the dataset into training and testing sets.
**Model Training:** We trained a KNN classification model to predict 'rating,' choosing an ad-hoc value for K=3.
**Evaluation:** By using KNN model we find f1_score = 0.7128987517337032 and accuracy_score = 0.6145251396648045 where k value was 3. To determine the best k value we used GridSerachCV and it is 26. We build KNN model again and this time it's performance is better than previous one. New f1_score is 0.7696139476961396 and accuracy_score is 0.6554934823091247.
## Hyperparameter Tuning
**KNN Hyperparameter Tuning:** We experimented with different values of K to observe its impact on prediction performance.
Model Performance
## Logistic Regression vs. KNN
We compared the performance of the logistic regression and KNN models.
**Discussion:** Based on the results of both model we have seen KNN model performs better than logistic regression model for this dataset.
=======
