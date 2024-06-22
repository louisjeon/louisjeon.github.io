---
title: "Model Parameter Learning"
excerpt: "About Model Parameter Learning"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/4/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-22
last_modified_at: 2024-06-22
---

## How to train a model
- Model learning means finding $\theta$ that can maximize probability of observing data set $D$ from model $p_\theta$
  - Cost function
  - Parameter learning algorithm

## Gradient-based optimization
- Continuous and differentiable cost function $J:\mathbb{R}^d\to\mathbb{R}$
- How should parameter $\theta$ be moved to minimize the value of cost function $J$?
- Gradient descent
  - Partially differenciate function by $\theta$ to get gradient and move towards direction where cost function $J$ is minimized
- Cost function for logistic regression
  #### $J(\boldsymbol\theta) = -\frac{1}{N}\displaystyle\sum_{i=1}^{N}[y^{(i)}logh_\boldsymbol\theta(\boldsymbol{x}^{(i)})+(1-y^{(i)})log(1-h_\boldsymbol\theta(\boldsymbol{x}^{(i)}))]$
- Gradient Descent (=Delta Learning Rule)
  #### $\theta_j := \theta_j - \alpha\frac{\partial J(\boldsymbol\theta)}{\partial\theta_j}=\theta_j-\alpha\frac{1}{N}\displaystyle\sum_{i=1}^{N}(h_\boldsymbol\theta(\boldsymbol{x}^{(i)})-y^{(i)})x_j^{(i)}$

## Gradient Descent Algorithm
- Initialize $\theta$ arbitrarily
- repeat
  - for j=0 to number of $\theta$
    $\theta_j =\theta_j-\alpha\frac{1}{N}\displaystyle\sum_{i=1}^{N}(h_\boldsymbol\theta(\boldsymbol{x}^{(i)})-y^{(i)})x_j^{(i)}$
- until $J(\boldsymbol\theta)$ converges

## Convex Optimization
- Cost function should be convex in order to find proper golobal minimum
- Non-convex function can fall into local minimum instead
- Cost function for logistic regression is convex
  #### $J(\boldsymbol\theta) = -ylogh_\boldsymbol\theta(\boldsymbol{x})+(1-y)log(1-h_\boldsymbol\theta(\boldsymbol{x})]$