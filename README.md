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

