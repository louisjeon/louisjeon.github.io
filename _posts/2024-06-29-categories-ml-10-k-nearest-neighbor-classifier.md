---
title: "Naive Bayes Classifier"
excerpt: "About Naive Bayes Classifier"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/9/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-29
last_modified_at: 2024-06-29
---

## Bayes classifier
- Logistic regression is trained to follow $P(y|x)$
- Bayes classifier is classified using Bayes' theorem

  #### $P(y|x) = \frac{p(x|y)P(y)}{p(x)}$

## Curse of Dimension
- Curse of dimension occurs as more independent variable K is used
  - The amount of data needed to approximate distribution in K combination of spaces increases exponentially
- Small number of samples is enough to make probability distribution if number of independent variables is small
- Exponentially more data is needed for more independent variables

## Naive Bayes classifier
- Solution is needed for curse of dimension when many independent variables exist.
- Curse of dimension can be solved by removing dependency of independent variables

## How to get a probability distribution
- How to get a probability distribution of a discrete variable
  - counting
- How to get a probability distribution of continuous variable
  - Discretize
    - Make variables countable by bucketing
  - Probability density estimation
    - Suppose normal distribution
      - #### $f(x;\mu,\sigma) = \frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$

## Inference
- Naive bayes classifier's assumption
  #### $f_{naive\ bayes}(x) = \displaystyle\operatorname*{argmax}_{y}p(\boldsymbol{x}|y)P(y)$
  #### $p(\boldsymbol{x}|y)P(y) = P(y)\displaystyle\prod_{i=1}^{K}p(x_i|y)$