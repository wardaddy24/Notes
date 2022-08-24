## Predictive Modeling:

Predictive modeling, also called predictive analytics, is a mathematical process that seeks to predict future events or outcomes by analyzing patterns that are likely
to forecast future results. 
<br>
**Example:**
Bayesian spam filters use predictive modeling to identify the probability that a given message is spam. In fraud detection, predictive modeling is used to identify
outliers in a data set that point toward fraudulent activity. And in customer relationship management (CRM), predictive modeling is used to target messaging to customers 
who are most likely to make a purchase.

## There are four assumptions associated with a linear regression model: 

1- Linearity: The relationship between X and the mean of Y is linear. <br>
2- Homoscedasticity: The variance of residual is the same for any value of X. <br>
3- Independence: Observations are independent of each other. <br>
4- Normality: For any fixed value of X, Y is normally distributed. 

##  There are four assumptions associated with a logistic regression model: 

1- The Response Variable is Binary <br>
2- The Observations are Independent <br>
3- There is No Multicollinearity Among Explanatory Variables <br>
4- There are No Extreme Outliers <br>
5- There is a Linear Relationship Between Explanatory Variables and the Logit of the Response Variable <br>
6- The Sample Size is Sufficiently Large 

## KNN
The k-nearest neighbors (KNN) algorithm is a supervised machine learning algorithm.
<br>
If regression -> return mean of labels 
<br>
If classification -> return mode of labels 
<br>
1-As we decrease the value of K to 1, our predictions become less stable. Just think for a minute, imagine K=1 and we have a query point surrounded by several reds and one green , but the green is the single nearest neighbor. Reasonably, we would think the query point is most likely red, but because K=1, KNN incorrectly predicts that the query point is green.
<br>
2-Inversely, as we increase the value of K, our predictions become more stable due to majority voting / averaging, and thus, more likely to make more accurate predictions (up to a certain point). Eventually, we begin to witness an increasing number of errors. It is at this point we know we have pushed the value of K too far.
<br>
3-In cases where we are taking a majority vote (e.g. picking the mode in a classification problem) among labels, we usually make K an odd number to have a tiebreaker.
### Advantages
1-The algorithm is simple and easy to implement.
<br>
2-There’s no need to build a model, tune several parameters, or make additional assumptions.
<br>
3-The algorithm is versatile. It can be used for classification, regression, and search.
### Disadvantages
1 -The algorithm gets significantly slower as the number of examples and/or predictors/independent variables increase. 

<br>
**What is the difference between bagging and boosting?** <br>
Ans. Bagging, also known as bootstrap aggregating, is the process in which multiple models of the same learning algorithm are trained with bootstrapped samples of the original dataset. Then, like the random forest, a vote is taken on all of the models’ outputs. <br>
Boosting is a variation of bagging where each individual model is built sequentially, iterating over the previous one. Specifically, any data points that are falsely classified by the previous model is emphasized in the following model. This is done to improve the overall accuracy of the model. Once the first model is built, the falsely classified/predicted points are taken in addition to the second bootstrapped sample to train the second model. Then, the ensemble models (models 1 and 2) are used against the test dataset and the process continues.
<br>

## Regularization
**L1 regularization:** It adds an L1 penalty that is equal to the absolute value of the magnitude of coefficient, or simply restricting the size of coefficients. For example, Lasso regression implements this method.  L1 regularization attempts to estimate the median of data. It is robust to outliers.
<br>
**L2 Regularization:** It adds an L2 penalty which is equal to the square of the magnitude of coefficients. For example, Ridge regression and SVM implement this method. L2 regularization makes estimation for the mean of the data. It is not robust to outliers.
<br>
**Elastic Net:** When L1 and L2 regularization combine together, it becomes the elastic net method, it adds a hyperparameter.

## Backprop and Gradient descent
**Stochastic gradient descent** is an optimization algorithm for minimizing the loss of a predictive model with regard to a training dataset. <br>
**Back-propagation** is an automatic differentiation algorithm for calculating gradients for the weights in a neural network graph structure. <br>
Stochastic gradient descent and the back-propagation of error algorithms together are used to train neural network models. <br>
