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

**1. PCA vs LDA**
  - Principal Component Analysis (PCA) works by identifying the directions (components) that maximize the variance in a dataset. In other words, it seeks to find the linear combination of features that captures as much variance as possible. PCA is supervised dimensionality reduction techniques.  Unlike PCA, however, LDA is a supervised learning method, which means it takes class labels into account when finding directions of maximum variance. This makes LDA particularly well-suited for classification tasks where you want to maximize class separability.
  - For PCA number of principal component chosed are 10 and for LDA are 8. 
  - For this classification problem, data compressed with LDA shows better performance than PCA for most of the problem.

**2. Support Vector Machine with Linear Kernel**
 - For linear Kernel, the hyperparameter is C. The C parameter tells the SVM optimization how much you want to avoid misclassifying each training example. For large values of C, the optimization will choose a smaller-margin hyperplane if that hyperplane does a better job of getting all the training points classified correctly. Conversely, a very small value of C will cause the optimizer to look for a larger-margin separating hyperplane, even if that hyperplane misclassifies more points. For very tiny values of C, you should get misclassified examples, often even if your training data is linearly separable. 
 - In this experiment, C has a little impact on the model performance. As we increases the value of C from 0.01 to 10, the test accuracy showed slight improvement only for data compressed using LDA. It seems that data is distributed in such a way that C has a little impact on the accuracy.

    |   Kernel   | Hyperparameter | Test Accuracy with PCA | Test Accuracy with LDA |
    |:----------:|:---------------:|:----------------------:|:----------------------:|
    |   Linear   |      C = 0.01      |         84.43 %        |         89.03 %        |
    |   Linear   |      C = 1      |         84.41 %        |         89.13 %        |
    |   Linear   |      C = 5      |         84.49 %        |         89.13 %        |
    |   Linear   |      C = 10     |         84.40 %        |         89.14 %        |

**3. Support Vector Machine with Polynomial Kernel**
- For polynomial kernel, the hyperparameter is degree of polynomial. The higher degree tends to make decision boundary more flexible to classify more number of training point correctly.
- For MNIST data set, Polynomial kernel performed best for degree 3. As we further increase degree, model started to overfit and test accuracy started decreasing.

    |   Kernel   | Hyperparameter | Test Accuracy with PCA | Test Accuracy with LDA |
    |:----------:|:---------------:|:----------------------:|:----------------------:|
    | Polynomial |    Degree = 3   |         91.24 %        |         90.08 %        |
    | Polynomial |    Degree = 4   |         88.07 %        |         86.64 %        |
    | Polynomial |    Degree = 5   |         88.37 %        |         86.80 %        |

**4. Support Vector Machine with RBF Kernel**
- For RBF Kernel, the hyperparameter is $\gamma$. The $\gamma$ parameter defines how far the influence of a single training example reaches, with low values meaning ‘far’ and high values meaning ‘close’. The lower values of gamma result in models with lower accuracy and the same as the higher values of $\gamma$. It is the intermediate values of $\gamma$ which gives a model with good decision boundaries.
- In this experiment, model achieve best test acuracy when $\gamma$ is equal to 0.01. As we furhter increase the value of $\gamma$ model started overfitting and test accuracy started dropping.

    |   Kernel   | Hyperparameter | Test Accuracy with PCA | Test Accuracy with LDA |
    |:----------:|:---------------:|:----------------------:|:----------------------:|
    |     RBF    | $\gamma$ = 0.01 |         93.25 %        |         90.01 %        |
    |     RBF    | $\gamma$ = 0.1  |         87.7 %         |         91.76 %        |
    |     RBF    | $\gamma$ = 1    |         30.23 %        |         88.27%         |
    |     RBF    |  $\gamma$ = 10  |         11.35%         |         32.11%         |
**5. Logistic Regression**
The hyperparameter for the logistic regressor is learning rate. It is updated using the gradient descent method. For experimentation, the learning rate is changed to different values and a loss curve is observed. It is observed that loss is converging for very few values near 10<sup>-5</sup>. When the learning rate is high, the loss is exploding and goes to infinity. When the learning rate is lower than this, loss convergence is extremely slow. Following is the loss curve during training when learning rate is 10<sup>-5</sup>

## Requirement
Python 2.0 or above

## License

 [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

Copyright (c) Feb 2023 Pradip Kathiriya
