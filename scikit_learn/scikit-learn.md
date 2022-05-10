#### Scikit-learn is an open source machine learning library that supports supervised and unsupervised learning. <br>
It also provides various tools for model fitting, data preprocessing, model selection, model evaluation, and many other utilities.

### Estimators
1. An object which manages the estimation and decoding of a model.
2. Estimators must provide a fit method, and should provide set_params and get_params.

### Predictors
1. An estimator supporting predict and/or fit_predict. This encompasses classifier, regressor, outlier detector and clusterer.
2. In statistics, “predictors” refers to features.

# Questions: 
## Q.1 What does calling fit() multiple times on the same model do? <br>
Ans. If you will execute model.fit() for a second time, it will start training again using passed data and will remove the existing results. <br>
It will reset the following inside model:
1. Fitted Coefficients
2. Weights
3. Intercept (bias)
4. And other training related stuff.
To avoid overwriting, you can use "warm_start" parameter, where it will initialise model parameters with the previous solution from fit(). <br>
Also, you can use partial_fit() method as well if you want your previous calculated stuff to stay and additionally train using next data.

## Q.2 Is it possible in scikit-learn to split into three sets directly? <br>
Ans. No, it's not possible in scikit-learn to split into three sets directly. <br>
However, one approach to dividing the dataset into train, test, validation with 0.6, 0.2, 0.2 would be to use the train_test_split method twice.

## Q.3 How do you solve overfitting in random forest of Python sklearn?
Ans. To avoid over-fitting in RF models, the main thing you need to do is optimize a tuning parameter that governs the number of features that are randomly chosen 
to grow each tree from the bootstrapped data.<br>
If possible, the best thing you can do is get more data, the more data the less likely it is to overfit , as random patterns that appear 
predictive start to get drowned out as the dataset size increases.<br>
Growing a larger forest will improve predictive accuracy, although there are usually diminishing returns once you get up to several hundreds of trees.
<br>
Look at the following params:
1. n_estimators: In general the more trees the less likely the algorithm is to overfit.
2. max_features: Try reducing this number. The smaller, the less likely to overfit, but too small will start to introduce under fitting.
3. max_depth: Reduction of the maximum depth helps fighting with overfitting.
4. min_samples_leaf: This has a similar effect to the max_depth parameter, it means the branch will stop splitting once the leaves have that number of samples each.

## Q.4 What is the difference between 'transform' and 'fit_transform' in sklearn ?
1. fit() method is used for generating learning model parameters from training data. This is where the model "learns" from the data.
2. transform() method is to transform the data (produce model outputs) according to the fitted model.
3. fit_transform() method to do both; Fit the model to the data, then transform the data according to the fitted model.

## Q.5 Is there a library function for Root mean square error (RMSE) in python?
Ans. Sklearn's mean_squared_error itself contains a parameter squared with default value as True. <br>
If you set it to False, the same function will return RMSE instead of MSE.<br>
from sklearn.metrics import mean_squared_error <br>
rms = mean_squared_error(y_actual, y_predicted, squared=False)

## Q.6 How to extract the decision rules from scikit-learn decision-tree?
Ans. You can use Scikit learn export_text to extract the rules from a tree. Once you've fit your model, you just need two lines of code.<br>
from sklearn.tree import export_text <br>
rules = export_text(loan_tree, feature_names=(list(X_train.columns)))<br>
print(rules)
<br>

