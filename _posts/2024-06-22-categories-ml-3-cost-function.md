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
- Model learning is finding $\theta$ that can maximize probability of observing data set $D$ from a model $p_\theta(x)$
  - Cost function
  - Parameter learning algorithm