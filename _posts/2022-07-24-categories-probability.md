---
title: "Basic Probability theorems for ML"
excerpt: "Basic probability"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/0/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-21
last_modified_at: 2024-06-21
---

# Binomial distribution

### - Bernoulli trial, yes or no

### - Probability Mass Function

$$
f(k;n,p) = \binom{n}{k} p^k(1-p)^{n-k}, \binom{n}{k} = \frac{n!}{k!(n-k)!}
$$

### - Characteristics

- notation: $B(n,p)$

- mean: $np$

- variance: $np(1-p)$

# Multinominal distribution

### - Generalization of Binominal distribution

- Probability distribution of choosing one from K amount of A, B, C, ... not only Yes/No.

### - Probability Mass Function

$$
f(x_1, ..., x_k;n,p_1,...,p_k) = \frac{n!}{x_1!...x_k!}p_1^{x_1}...p_k^{x_k}
$$

### - Characteristics

- notation: $Mult(P),P=<p_1,...,p_k>$

- mean: $\mathbb{E}(x_i) = np_i$

- variance: $Var(x_i) = np_i(1-p_i)$
