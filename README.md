## Project Description:
In this project, I have implemented Support vector machine (Linear Kernel, Polynomial Kernel, RBF Kernel), Logistic Regression and Convolutional
Neural Network to achieve hand-written digits recognition on MNIST data set. The purpose of this project is to understand fundamentally how these 
methods work and to learn how to tune hyperparameters in this methods.

## Pipeline
### Support Vector Machine (SVM with Linear Kernel, Polynomial Kernel, and RBF Kernel)
- The data is first processed with the Principal Component Analysis (PCA) and Linear Discriminant Analysis (LDA) to represent input data in lower dimensions. The number of principal component used for PCA are 10 and for LDA are 8.
- The lower dimensional representation is then classify using the SVM with linear, polynomial and RBF kernel. You need to experiment with the hyperparameter to understand its effect on the performance.
### Logistic Regression
- The data is first processed with the Principal Component Analysis (PCA) and Linear Discriminant Analysis (LDA) to represent input data in lower dimensions. The number of principal component used for PCA are 10 and for LDA are 8.
- The lower dimensional representation is then classify by multiclass logistic regression. Multiclass logistic regression models the class posteriors of an image log-linearly in terms of its features. The model parameters are estimated to minimize the negative log-likelihood of the class labels, which are encoded as categorical vectors;this is sometimes called the cross-entropy loss.
### Convolutional Neural Network
- CNN architecture are built from the scratch, train it on the MNIST training set and test it on testing set.
- The purpose of this section is to understand how the CNN works, how to build it from scratch, to experiment with the different hyperparameter to understand its effect on the model performance and how to tune them to achieve better model performance.

## Resutls and Analysis:

1. PCA vs LDA 
  Principal Component Analysis (PCA) works by identifying the directions (components) that maximize the variance in a dataset. In other words, it seeks to find the linear combination of features that captures as much variance as possible.
