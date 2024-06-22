---
title: "Cost Function"
excerpt: "About Cost Function"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/3/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-22
last_modified_at: 2024-06-22
---

## How to train a model?
- Model $p_\theta(x)$
  - Random variable $x$
  - Parameter $\theta$
- Data
  - $D = \{x^{(1)}, x^{(2)}, ..., x^{(N)}\}$
- Model learning is finding $\theta$ that can maximize probability of observing data set $D$ from model $p_\theta(x)$
  - Cost function
  - Parameter learning algorithm

## Likelihood Estimation
- Probability of model $p_\theta(x)$ observing data set $D=\{x^{(1)}, x^{(2)}, ... ,x^{(N)}\}$
  ### $p_\theta(x^{(1)}, x^{(2)}, ... ,x^{(N)}) = p_\theta(x^{(1)})p_\theta(x^{(2)})...p_\theta(x^{(N)}) = \displaystyle\prod_{i=1}^{N}p_\theta(x^{(i)})$
- Probability of model $p_\theta(y|x)$ observing data set $D=\{(y^{(1)}, x^{(1)}), (y^{(2)}, x^{(2)}), ... ,(y^{(n)}, x^{(N)})\}$
  ### $p_\theta(y^{(1)}, y^{(2)}, ... ,y^{(N)}|x^{(1)}, x^{(2)}, ... ,x^{(N)}) = p_\theta(y^{(1)}|x^{(1)})p_\theta(y^{(2)}|x^{(2)})...p_\theta(y^{(N)}|x^{(N)}) = \displaystyle\prod_{i=1}^{N}p_\theta(y^{(i)}|x^{(i)})$

## Maximum Likelihood Estimation
- MLE is a methodology of maximizing probability of a model observing data set D

  ### $\hat\theta = \displaystyle\operatorname*{argmax}_{\theta}\displaystyle\prod_{i=1}^{N}p_\theta(y^{(i)}|x^{(i)})$

- Negative log likelihood 
  - Converts multiplying minus values into sum of logs since it's better when being computed

    ### $\hat\theta = \displaystyle\operatorname*{argmin}_{\theta}-\displaystyle\sum_{i=1}^{N}logp_\theta(y^{(i)}|x^{(i)})$

- Cost function

  ### $J(\theta) = -\frac{1}{N}\displaystyle\sum_{i=1}^{N}logp_\theta(y^{(i)}|x^{(i)})$
  $\hat\theta = \displaystyle\operatorname*{argmin}_{\theta}J(\theta)$

## Cost function for Logistic Regression
- Logistic Regression
  ### $P_\theta(y=1|\boldsymbol{x})=h(\boldsymbol{x})=\frac{1}{1+e^{-(\boldsymbol\theta^T\boldsymbol{x}+\theta_0)}}$
- Cost function for logistic regression
  ### $J(\boldsymbol\theta)=-\frac{1}{N}\displaystyle\sum_{i=1}^{N}logP_\theta(y^{(i)}|x^{(i)})$

## Cost function, Loss function

- Loss function
  - Difference between gold and predicted values per sample
    $L(\boldsymbol\theta) = -logP_\boldsymbol\theta(y|\boldsymbol{x}) = -ylogh_\boldsymbol\theta(\boldsymbol{x})-(1-y)log(1-h_\boldsymbol\theta(\boldsymbol{x}))$
    <br/>

- Cost function
  - Average difference between gold and predicted values from the entire data set
  $J(\boldsymbol\theta)=-\frac{1}{N}\displaystyle\sum_{i=1}^{N}logP_\theta(y^{(i)}|x^{(i)})$