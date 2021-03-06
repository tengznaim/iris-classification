# Iris Classification

This is my personal attempt for the classic machine learning classification problem of the Iris dataset using various techniques.

The dataset : https://archive.ics.uci.edu/ml/datasets/iris

This is relatively simple dataset with not many examples and only a few features but I wanted to use this as a practice for a start-to-finish data science project, that is, from preprocessing and exploratory data analysis (EDA) to model training and model evaluation. I also attempt to consider various optimisation techniques to improve model performance.

## Preprocessing and Exploratory Data Analysis

Preprocessing steps used were based on the `data-preprocessing.ipynb` notebook from the following repository: https://github.com/zotroneneis/machine_learning_basics. They are also based on a few articles I read on the subject.

Although the dataset is known to be complete, I went into this assuming I didn't know anything about the dataset in order to practice preprocessing to obtain a clean dataset from the raw dataset.

Specific steps taken for this dataset were:

1. Dataset inspection
2. Encoding the classes
3. Dataset visualization
4. Duplicate data points removal
5. Attribute correlation check

Since there were no missing values in this particular dataset, one commonly vital step that was not used is handling these missing values and outliers. The features also had reasonably close scales hence I also made do without mean normalization and feature scaling.

## Models

### Logistic Regression

The first approach I tried uses a logistic regression model provided by the sklearn package. Based on the documentation, the model uses a one-vs-all approach for multiclass classification and the cross-entropy loss. The result was a model that performed reasonably well on both the training set and the test set with a typical accuracy of >= 90%.

### Neural Network

This approach uses the MLPClassifier also provided by the sklearn package. The classifier has many tweakable parameters but the current implementation mostly uses the default parameters with some changes to the solver and the number of the hidden units. The result is a classifier that performs reasonably well but not as well as the logistic regression implementation.

## References

1. Article on Data Preprocessing and EDA

   - https://towardsdatascience.com/data-preprocessing-and-eda-for-data-science-50ba6ea65c0a

2. Visualising Data with Pair Plots

   - https://towardsdatascience.com/visualizing-data-with-pair-plots-in-python-f228cf529166
   - https://seaborn.pydata.org/generated/seaborn.pairplot.html

3. Cross Validation Set vs Test Set

   - https://machinelearningmastery.com/difference-test-validation-datasets/

4. Plotting Multiple Confusion Matrices

   - https://stackoverflow.com/questions/61016110/plot-multiple-confusion-matrices-with-plot-confusion-matrix

5. Saving Models Using Pickle

   - https://stackabuse.com/scikit-learn-save-and-restore-models/
   - https://machinelearningmastery.com/save-load-machine-learning-models-python-scikit-learn/

6. Multi Layer Perceptron with Scikit Learn

   - https://annisap.medium.com/build-your-first-neural-network-in-python-c80c1afa464

7. Label Encoding vs One Hot Encoding
   - https://towardsdatascience.com/choosing-the-right-encoding-method-label-vs-onehot-encoder-a4434493149b
