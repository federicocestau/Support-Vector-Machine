# Support-Vector-Machine
What category of algorithms does Support Vector Machines classification belong to? Support Vector Machines (SVMs) are most frequently used for solving classification problems, which fall under the supervised machine learning category. Support Vector Classifier (SVC). 

Also, with small adaptations, SVMs can also be used for regression through the use of the Support Vector Regression algorithm (SVR).

Note, the algorithm allows you to control how much you care about misclassifications (and points inside the margin) by adjusting the hyperparameter C. Essentially, C acts as a weight assigned to ξ. A low C makes the decision surface smooth (more robust), while a high C aims at classifying all training examples correctly, producing a closer fit to the training data but making it less robust.

Beware, while setting a high value for C is likely to lead to a better model performance on the training data, there is a high risk of overfitting the model, producing poor results on the test data.

Before introducing gamma parameter, we need to talk about kernel trick. In some cases, data points that are not linearly separable are transformed using kernel functions so that they become linearly separable. Kernel function is kind of a similarity measure. The inputs are original features and the output is a similarity measure in the new feature space. Similarity here means a degree of closeness. It is a costly operation to actually transform data points to a high-dimensional feature space. The algorithm does not actually transform the data points to a new, high dimensional feature space. Kernelized SVM compute decision boundaries in terms of similarity measures in a high-dimensional feature space without actually doing a transformation. I think this is why it is also called kernel trick.

When we increase the C value, the margin gets smaller. Thus, the models with low C values tend to be more generalized. The difference becomes clearer with larger datasets.

Gamma is a hyperparameter used with non-linear SVM. One of the most commonly used non-linear kernels is the radial basis function (RBF). Gamma parameter of RBF controls the distance of the influence of a single training point.

Low values of gamma indicate a large similarity radius which results in more points being grouped together. For high values of gamma, the points need to be very close to each other in order to be considered in the same group (or class).

It is very significant to remember for SVM that the input data need to be normalized so that features are on the same scale and compatible.

Typical values for c and gamma are as follows. However, specific optimal values may exist depending on the application: 0.0001 < gamma < 10 0.1 < c < 100
