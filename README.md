# This repository about Logistic Regression and Support Vector Machine

## Motivation of Experiment

- Compare andand understand the difference between gradient descent and batch random stochastic gradient descent.
- Compare and understand the differences and relationships between Logistic regression and linear classification.
- Further understand the principles of SVM and practice on larger data.

## Dataset

Experiment uses [a9a](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/binary.html#a9a) of [LIBSVM Data](https://www.csie.ntu.edu.tw/~cjlin/libsvmtools/datasets/), including 32561/16281(testing) samples and each sample has 123/123 (testing) features. Please download the training set and validation set. The dimension may be wrong, which is due to the values of last column are all zero so it is ignored. This can be fixed by adding one column by yourself or specify the n_features to be 123 when using the function.

## Environment for Experiment

[Python3](https://www.python.org/), at least including following python package: [sklearn](http://scikit-learn.org/stable/)，[numpy](http://www.numpy.org/)，[jupyter](http://jupyter.org/)，[matplotlib](https://matplotlib.org/)
It is recommended to install [anaconda3](https://anaconda.org/) directly, which has built-in python package above.

## Experiment Step

The experimental code and drawing are completed on jupyter.

*Logistic Regression and Batch Stochastic Gradient Descent*

- Load the training set and validation set.
- Initialize logistic regression model parameter (you can consider initializing zeros, random numbers or normal distribution).
- Select the loss function and calculate its derivation, find more detail in PPT.
- Determine the size of the batch_size and randomly take some samples,calculate gradient G toward loss function from **partial samples**.
- Use the **SGD** optimization method to update the parametric model and encourage additional attempts to optimize the **Adam** method.
- Select the appropriate threshold, mark the sample whose predict scores **greater than the threshold as positive, on the contrary as negative**. Predict under validation set and get the loss *Lvalidation*.
- Repeat step 4 to 6 for several times, and **drawing graph of** *Lvalidation* **with the number of iterations**.

*Linear Classification and Batch Stochastic Gradient Descent*

- Load the training set and validation set.
- Initialize SVM model parameters (you can consider initializing zeros, random numbers or normal distribution).
- Select the loss function and calculate its derivation, find more details in PPT.
- Determine the size of the batch_size and randomly take some samples,calculate gradient G toward loss function from **partial samples**.
- Use the **SGD** optimization method to update the parametric model and encourage additional attempts to optimize the **Adam** method.
- Select the appropriate threshold, mark the sample whose predict scores **greater than the threshold as positive, on the contrary as negative**. Predict under validation set and get the loss *Lvalidation*.
- Repeat step 4 to 6 for several times, and **draw graph of** *Lvalidation* **with the number of iterations**.

