---
title: "Regularization"
excerpt: "About Regularization"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/6/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-25
last_modified_at: 2024-06-25
---

## The Problem of Overfitting
- Overfitting is when a model is overly trained by training data that it only performs well for training data and not for test data

## Handling Overfitting
- Simplify a model
  - Lower the dimension of leading terms for Polynominal feature
  - Minimize the number of features
- Regularization
  - Restrain the size of learning parameter $\theta$

## Intuition of Regularization
- Restraining $\theta$ of leading terms makes the model similar to lower dimensioned ones = simplifies the model

## Cosf function with Regularization
- Apply regularization by adding regularization trem at the end of the cost function
  #### $J(\theta) = -\frac{1}{N}[\displaystyle\sum_{i=1}^{N}(y^{(i)}logh_\boldsymbol\theta(\boldsymbol{x}^{(i)}) + (1-y^{(i)})log(1-h_\theta(\boldsymbol{x}^{(i)})))] + \frac{\lambda}{2N}\displaystyle\sum_{k=1}^{K}\theta_k^2$

## How does $\lambda$ work?
- It is important to control the size of $\lambda$ since it is also a hyper-parameter
  - $\theta$ gets smaller too fast and model is overly simplified if $\lambda$ is too large: underfitting
  - Effect of regularization is marginal if $\lambda$ is too small