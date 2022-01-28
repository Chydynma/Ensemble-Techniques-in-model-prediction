# Ensemble-Techniques-in-model-prediction
The goal of the project was to analyze the data provided and, with the help of a classification model:
- Facilitate the process of visa approvals.
- Recommend a suitable profile for the applicants for whom the visa should be certified or denied based on the drivers that significantly influence the case status

The following are steps taken on the execution of this project:

1. EDA: I did univariate, bivariate, and multivariate analysis using appropriate visuals. Thereby identifying key meaningful observations on individual variables and the relationship between variables.
2. Data Preprocessing: Data types were fixed i.e. object data type was converted to a category, outliers were checked and there were not treated because the number of outliers was significant which represents actual values/occurrence and is required for model prediction.
3. Data was split into training and test data using stratified parameters. This is because when a classification problem shows a significant imbalance in the distribution of the target variable, stratify is used to ensure that relative class frequencies are approximately preserved in the train and test set.
4. Model Evaluation: Here, an evaluation of factors that can make a model prediction is done. Based on this, what factors are important to consider for the prediction and which metric (accuracy, recall, precision, and F1-score) has to be optimized.
5. A decision tree model was built with a Decision tree classifier function using ‘Gini’ as the default criteria for the split, class_weight, and random_state. Confusion Matrix is also done to show the metrics (accuracy, recall, precision, and F1-score) and give direct comparison values like True Positive, False Positives, True Negatives, and False Negatives.
The training and test performance is done to see the result of each metric. This will tell if the algorithm used (Decision Tree) is working well on the training data but generalizing on the test data considering the metric under consideration. Or vice versa 
6. Another model is built using a Bagging classifier. A confusion matrix is done just like above. The result from the training and test performance showed overfitting on the training set while it performed poorly on the test set. This is based on the metric under consideration.
7. Bagging Classifier with a weighted decision tree is done so as to reduce the variance in the decision tree. Decision trees usually overfit which results in a high variance in the model.
Model is built along with a confusion Matrix. The results give a good performance of the training set. However, it was not able to generalize on the test set.
8. Next, a Random Forest model was done. This is an extension of bagging where it takes a random subset of data and takes a random selection of features rather than using all features to build the tree. Likewise, the model is built and a confusion matrix is done as well. The results shows the test set performed well on the Random Forest in terms of the metric considered.
Then, Random Forest using the class_weight as criteria is done. The result showed not much improvements were seen in comparison to Random Forest without class_weight.
9. Next, the model was tuned using the GridSearch. Hyperparameter tuning is also tricky in the sense that there is no direct way to calculate how a change in the hyperparameter value will reduce the loss of your model, so we usually resort to experimentation. Grid search is a tuning technique that attempts to compute the optimum values of hyperparameters. It is an exhaustive search that is performed on the specific parameter values of a model. The parameters of the estimator/model used to apply these methods are optimized by cross-validated grid-search over a parameter grid.
Based on this, the result from tuning the bagging classifier shows there is improvement in the metric under consideration compared to other metrics. This is an indication the overall model is making a mistake. Then tuning is done on the random forest. This gave the same performance as the untuned random forest.
10. At this point 8models have been built. A comparison is done on all models to see their performance on all metrics. Feature importance is done. The importance of feature is computed as the normalized total reduction of the criterion brought by that feature. This is also known as Gini importance. Here, a feature importance graph is plotted. The columns with the highest values are identified as the most important features for prediction.
11. A boosting model is built where Decision Tree, Random Forest, Bagging, Adaboost, Gradient boost, and XGBoost classifiers are done and trained with default parameters. 
A comparison is done for all models to see their performance.  
Feature importance is done on the tuned Random Forest to identify the columns which are most important for prediction.
12. Based on all the analysis and models built, insights are highlighted on employees who should be certified or denied a visa, drivers of a certified visa application, and profiles of a certified applicant and a denied applicant.


