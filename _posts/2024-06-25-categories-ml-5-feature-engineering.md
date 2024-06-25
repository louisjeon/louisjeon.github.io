---
title: "Feature Engineering"
excerpt: "About Feature Engineering"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/5/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-25
last_modified_at: 2024-06-25
---

## Pipeline of maching learning
- Machine learning algorithm extracts features from input and model classifies or clusters data according to the features

## Types of features
- Numerical feature
  - continuous
  - discrete
- Categorical feature
  - Ordinal
  - Nominal
- Array feature
  - example
    - image
    - sound
    - ...
  
## Numerical feature
- Numerical feature
  - continuous
  - discrete
- Range can be different between numerical features
- $\theta$'s range difference can lead to slow learning rate
  #### $h(\boldsymbol{x}) = \sigma(\theta_1x_1 + \theta_2x_2 + \cdots\theta_nx_n + \theta_0)$

## Normalizing numerical feature
- Numerical feature scaling
  - Min-Max feature scaling  
  - Mean normalization
  - Standardization
- Bucketing

## Min-Max scaling
   #### $x_{new} = \frac{x - x_{min}}{x_{max} - x_{min}}, 0\leq x_{new}\leq 1$

## Mean Normalization
  #### $x_{new} = \frac{x - x_{mean}}{x_{max} - x_{min}}, -0.5\leq x_{new}\leq 0.5$

## Problem of min-max, mean normalization
  - min, max can be set too large if outlier exists
  - Resolution of general values can fall down by outlier values

## Standardization
- Use distribution of variable $x$ to get less affected by outlier values
- Normalize by how many times of standard diviation is $x$ seperated from other average $x$s
  #### $x_{new} = \frac{x-\mu}{\sigma}$

## Bucketing
- Extract generalized and abstracted features by bucketing numeric variables in certain range

## Quantile Bucketing
- Same range bucketing might not reflect data distribution well depends on data type
- Quantile Bucketing bucket variables in a way that same number of variables exist in one bucket

## Categorical feature
- Ordinal
  - Can be replaced with numbers ex) Score: low, middle, high => 1, 2, 3
- Nominal
  - Should not be replaced with numbers ex) Port of Embarkation: Cherbourg, Queenstown, Southampton =/=> 1, 2, 3 

## One-hot encoding
- Allows nominal features to be presented as linear model
- Reform each category with seperate binary variables

## Bucketing for categorical feature
- Similar categories can be grouped with bucketing

## Polynomial feature
- What if decision border is non-linear?
- Input variables can be powered into Polynominal features and non-linear decision borders can be defined
  #### $h(x) = \sigma(\theta_1x_1 + \theta_2x_2 + \theta_3x_1^2 +\theta_0)$
  #### $h(x) = \sigma(\theta_1x_1 + \theta_2x_2 + \theta_1x_1^2 +\theta_2x_2^2 + \theta_0)$ -> Ellipse
  #### $...$