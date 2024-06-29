---
title: "Linear Regression"
excerpt: "About Linear Regression"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/8/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-26
last_modified_at: 2024-06-26
---

## Regression
- A way of modeling correlation between several independent variables and a dependent variable

## Linear Regression
- A way of modeling linear correlation between one or more independent variables and a dependent variable
  $h_\boldsymbol\theta(\boldsymbol{x}) = \theta_0 + \theta_1x_1 + \theta_2x_2 + \cdots + \theta_kx_k$

## Polynomial Regression
- A way of modeling linear correlation between one or more independent variable $x$s and one dependent variable $y$ as $x$'s $n$th polinomial expression
  $h_\boldsymbol\theta(\boldsymbol{x}) = \theta_1x_1 + \theta_2x_1^2 + \theta_3x_1^3 + \cdots + \theta_ix_2 + \theta_{i+1}x_2^2 + \theta_{i+2}x_1^3 + \cdots + \theta_0$

## Cost function
- In linear regression or polynomial regression, cost is defined as MSE(Mean Square Error) of model's forecast values and real values
  #### $J(\boldsymbol{\theta}) = \frac{1}{2N}\displaystyle\sum_{i=1}^{N}(h_\boldsymbol\theta(\boldsymbol{x}^{(i)})-y^{(i)})^2$

## Gradient Descent
  #### $\theta_j := \theta_j - \alpha\frac{\partial J(\boldsymbol\theta)}{\partial\theta_j} = \theta_j - \alpha \displaystyle\sum_{i=1}^{N}(h_\boldsymbol\theta(\boldsymbol{x}^{(i)}) - y^{(i)})x_j^{(i)}$