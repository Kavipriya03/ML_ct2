# ml_ct2
---
## K-fold cross validation
### What is K-fold cross validation
suppose you have traning and testing set of data and you need to split data into multiple parts to analyse the bias and the fitting of the model.
Hence the number of times the sample data is split into it is the k- fold. suppose if the model has to be split into 10 time it is called 10-fold cross validation.

**_Cross-validation is a resampling procedure used to evaluate machine learning models on a limited data sample._**

## Why K-fold is used 
If you have a machine learning model and some data, you want to tell if your model can fit. You can split your data into training and test set. Train your model with the training set and evaluate the result with test set. But you evaluated the model only once and you are not sure your good result is by luck or not. You want to evaluate the model multiple times so you can be more confident about the model design.

Cross-validation is primarily used in applied machine learning to **_estimate the skill of a machine learning model on unseen data_**. That is, to use a limited sample in order to estimate how the model is expected to perform in general when used to make predictions on data not used during the training of the model.

It is a popular method because it is simple to understand and because it generally results in a less biased or less optimistic estimate of the model skill than other methods, such as a simple train/test split.

### features of k-fold validation
**Robustness**: K-fold cross-validation helps to reduce the impact of randomness in the data split. By averaging results over multiple folds, you get a more stable estimate of a model's performance.

**Data Utilization**: It ensures that each data point is used for both training and validation exactly once during the K iterations. This helps maximize the use of available data for model evaluation.

**Variance and Bias Analysis**: K-fold cross-validation allows you to assess both the variance and bias of a model. If a model performs consistently well across all folds, it suggests low variance. If the performance varies widely, it may indicate high variance.

**Model Selection**: You can use K-fold cross-validation to compare and select between different machine learning algorithms or hyperparameters. By comparing their performance across multiple folds, you can make more informed decisions about which model or settings are better.

**Overfitting Detection**: It helps in identifying overfitting. If a model performs very well on the training data but poorly on the validation data across all folds, it may be a sign of overfitting.

**Hyperparameter Tuning**: K-fold cross-validation can be used to tune hyperparameters systematically. You can perform a grid search or random search over a range of hyperparameters and select the combination that performs best on average across the folds.

**Better Generalization**: The performance estimate obtained through K-fold cross-validation is typically a better reflection of how well the model is likely to generalize to new, unseen data compared to a single train-test split.

**Trade-Off**: The choice of K can be a trade-off. Smaller values of K (e.g., K = 5) may lead to more biased estimates, while larger values of K (e.g., K = 10) may be computationally expensive but provide a more accurate estimate.

**Stratified K-Fold**: In classification problems with imbalanced class distributions, stratified K-fold cross-validation ensures that each fold maintains the same class distribution as the original dataset. This helps prevent bias in performance estimation.
