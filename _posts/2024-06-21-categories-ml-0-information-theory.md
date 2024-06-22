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

## Binomial distribution

#### - Bernoulli trial, yes or no

#### - Probability Mass Function

&emsp; $f(k;n,p) = \binom{n}{k} p^k(1-p)^{n-k}, \binom{n}{k} = \frac{n!}{k!(n-k)!}$

#### - Characteristics

- notation: $B(n,p)$
- mean: $np$
- variance: $np(1-p)$

## Multinominal distribution

#### - Generalization of Binominal distribution

- Probability distribution of choosing one from K amount of A, B, C, ... not only Yes/No.

#### - Probability Mass Function

&emsp; $f(x_1, ..., x_k;n,p_1,...,p_k) = \frac{n!}{x_1!...x_k!}p_1^{x_1}...p_k^{x_k}$

#### - Characteristics

- notation: $Mult(P),P=<p_1,...,p_k>$
- mean: $\mathbb{E}(x_i) = np_i$
- variance: $Var(x_i) = np_i(1-p_i)$

## Normal Distribution

#### - Normal distribution = Guassian distribution

#### - Many distributions that are observed in the nature follow Normal distribution

#### - Probability Mass Function

&emsp; $f(x;\mu,\sigma)=\frac{1}{\sigma\sqrt{2\pi}}e^{-\frac{(x-\mu)^2}{2\sigma^2}}$

#### - Characteristics

- notation: $N(\mu,\sigma^2)$
- mean: $\mu$
- variance: $\sigma^2$

## Beta Distribution

#### - Ranges between 0 and 1

#### - Good characteristics

#### - Probability Mass Function

&emsp; $f(\theta;\alpha,\beta)=\frac{\theta^{\alpha-1}(1-\theta)^{\beta-1}}{B(\alpha,\beta)}, B(\alpha,\beta)=\frac{\Gamma(\alpha)\Gamma(\beta)}{\Gamma(\alpha+\beta)}, \Gamma(\alpha)=(\alpha-1)!,\alpha\in\mathbb{N}^+$

#### - Characteristics

- notaion: $Beta(\alpha, \beta)$
- mean: $\frac{\alpha}{\alpha+\beta}$
- variance: $\frac{\alpha\beta}{(\alpha+\beta)^2(\alpha+\beta+1)}$
