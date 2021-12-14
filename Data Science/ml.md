## Predictive Modeling:

Predictive modeling, also called predictive analytics, is a mathematical process that seeks to predict future events or outcomes by analyzing patterns that are likely
to forecast future results. \
** Example: ** \
Bayesian spam filters use predictive modeling to identify the probability that a given message is spam. In fraud detection, predictive modeling is used to identify
outliers in a data set that point toward fraudulent activity. And in customer relationship management (CRM), predictive modeling is used to target messaging to customers 
who are most likely to make a purchase.

## There are four assumptions associated with a linear regression model: 

1- Linearity: The relationship between X and the mean of Y is linear. \
2- Homoscedasticity: The variance of residual is the same for any value of X. \
3- Independence: Observations are independent of each other. \
4- Normality: For any fixed value of X, Y is normally distributed. 

##  There are four assumptions associated with a logistic regression model: 

1- The Response Variable is Binary \
2- The Observations are Independent \
3- There is No Multicollinearity Among Explanatory Variables \
4- There are No Extreme Outliers \
5- There is a Linear Relationship Between Explanatory Variables and the Logit of the Response Variable \
6- The Sample Size is Sufficiently Large 

## KNN
The k-nearest neighbors (KNN) algorithm is a supervised machine learning algorithm.\
If regression -> return mean of labels \
If classification -> return mode of labels \
1-As we decrease the value of K to 1, our predictions become less stable. Just think for a minute, imagine K=1 and we have a query point surrounded by several reds and one green , but the green is the single nearest neighbor. Reasonably, we would think the query point is most likely red, but because K=1, KNN incorrectly predicts that the query point is green.\
2-Inversely, as we increase the value of K, our predictions become more stable due to majority voting / averaging, and thus, more likely to make more accurate predictions (up to a certain point). Eventually, we begin to witness an increasing number of errors. It is at this point we know we have pushed the value of K too far.\
3-In cases where we are taking a majority vote (e.g. picking the mode in a classification problem) among labels, we usually make K an odd number to have a tiebreaker.
### Advantages
1-The algorithm is simple and easy to implement.\
2-There’s no need to build a model, tune several parameters, or make additional assumptions.\
3-The algorithm is versatile. It can be used for classification, regression, and search.
### Disadvantages
1 -The algorithm gets significantly slower as the number of examples and/or predictors/independent variables increase. 
