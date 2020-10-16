In the previous lab I used Naive Bayes to classify spam in this [dataset](https://archive.ics.uci.edu/ml/datasets/SMS+Spam+Collection). In this notebook, we will expand on the previous analysis by using a few of the new techniques 
such as Bagging, RandomForest & AdaBoostClassifier

It turns out that our naive bayes model actually does a pretty good job.  However, let's take a look at a few additional models to see if we can't improve anyway.

Specifically in this notebook, we will take a look at the following techniques:

* [BaggingClassifier](http://scikit-learn.org/stable/modules/generated/sklearn.ensemble.BaggingClassifier.html#sklearn.ensemble.BaggingClassifier)
* [RandomForestClassifier](http://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html#sklearn.ensemble.RandomForestClassifier)
* [AdaBoostClassifier](http://scikit-learn.org/stable/modules/generated/sklearn.ensemble.AdaBoostClassifier.html#sklearn.ensemble.AdaBoostClassifier)

Another really useful guide for ensemble methods can be found [in the documentation here](http://scikit-learn.org/stable/modules/ensemble.html).

These ensemble methods use a combination of techniques:

* **Bootstrap the data** passed through a learner (bagging).
* **Subset the features** used for a learner (combined with bagging signifies the two random components of random forests).
* **Ensemble learners** together in a way that allows those that perform best in certain areas to create the largest impact (boosting).

In general, there is a five step process that can be used to use a supervised learning method (which you actually used above):

1. **Import** the model.
2. **Instantiate** the model with the hyperparameters of interest.
3. **Fit** the model to the training data.
4. **Predict** on the test data.
5. **Score** the model by comparing the predictions to the actual values.