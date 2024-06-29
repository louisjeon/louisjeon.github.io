---
title: "K-Nearest Neighbor Classifier"
excerpt: "About K-Nearest Neighbor Classifier"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/10/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-29
last_modified_at: 2024-06-29
---

## Parametric model
  - A model with fixed number of parameters
  - Information about aimed probability distribution is saved in the model
  - Logistic Regression, Naive Bayes, ...
## Non-parametric model
  - Number of parameters increases in proportion to the training data
  - Does not assume that the data follows certain distribution
  - K-Nearest Neighbor

## Parametric Density Estimation
  - Assume normal distribution
  - Probabiltiy density function
    #### $\boldsymbol{p}(x) = \frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$

## Non-Parametric Density Estimation
  - Does not assume distribution
  - Probability density function
    #### $\boldsymbol{p}(x) = \frac{1}{h}\frac{k}{N}$

## Parzen window
  - Method of getting probability density of $x$ by counting the number of samples of $h$ sized space near input variable $x$ and divide by number of whole variables and size of $h$
    #### $p(x) = \frac{1}{h^d}\frac{k_x}{N}$

## Limitations of Parzen window
- Parzen window is not free from curse of dimension
- Not less than $N^K$ samples are needed in $K$ dimension in order to keep data's density if $N$ samples are needed in first dimension 

## K-nearest neighbor estimation
- Parzen window fixes $h$ and $k$ changes according to $x$
- K-nearest neighbors estimation fixes $k$ and $h$ changes according to $x$
  #### $P_{parzen\ window}(x) = \frac{1}{h^d}\frac{k_x}{N}$
  #### $P_{knn}(x) = \frac{1}{h_x^d}\frac{k}{N}$

## Limitations of K-nearest neighbors estimation
- High computational complexity is needed to find $k$ neighbors near $x$
  - High time complexity
    - Time complexity: $O(kdN)$
- There are alorithms to solve the high time complexity problem
  - Approximated Nearest Neighbors
    - FAISS
    - ANNOY
    - ScaNN

## K-nearest neighbor classifier
- Find $k$ neighbor samples near $x$ and select $x$'s category as the most common category from $k$ neighbors
- Feature scaling is important when using KNN