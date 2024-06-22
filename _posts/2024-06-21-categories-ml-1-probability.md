---
title: "Information Theory"
excerpt: "About Information Theory..."

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/1/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-21
last_modified_at: 2024-06-21
---

## Information Theory

- Researched to quantify information and compress messages efficiently

- How many bits can discribe a certain incident

- Less bits are used for frequent incidents

- More bits are used for rare incidents

- Coin flip can be described with 1 bit

- 2 bits are used for 4 choices (00/01/10/11)

## Uncertainty

- How many questions on average are needed to figure out a status

## Self-Information

- Information amount of certain accident happening with probability of distribution P is $I(x)$
- Metrics can be bit or nat depending on the base of log function calculating $I(X)$
- $log_2P(x)$: bit, $log_eP(x)$:nat

&emsp; $I(x) = -logP(x)$

- If $P(sunny) = 0.5, I(sunny) = -log_2(\frac{1}{2}) = 1$

## Entropy

- Degree of uncertainty
- How many questions are needed to check information
- Expected information amount on average when accident $x$ is sampled by probability distribution $P$<br/>
  &emsp; $H(x) = \mathbb{E}_{x{\sim}p}[I(x)] = -\displaystyle\sum_{x}P(x)logP(x)$

## KL divergence

- KL divergence is used to measure difference between probability distribution $P$ and $Q$
- Entropy difference in alternative probability distribution presenting approximate values in sampling step for certain probability distribution
- KL divergence is $D_{KL}(P||Q) \neq D_{KL}(Q||P)$<br/>
  &emsp; $D_{KL}(P||Q) = \mathbb{E}_{x{\sim}p}[logP(x) - logQ(x)]$
  &emsp; $=\displaystyle\sum_{x}log\frac{P(x)}{Q(x)}=\displaystyle\sum_{x}P(x)logP(x) - P(x)logQ(x)$
  &emsp; $=(-\displaystyle\sum_{x}P(x)logQ(x)) - (-\displaystyle\sum_{x}P(x)logP(x))$
  &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; $H(P,Q)$ &emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;&emsp; $H(P)$

## Cross Entropy

- Used to measure difference between probability distribution P and Q<br/>
  $H(P,Q) = -\displaystyle\sum_{x}P(x)logQ(x)$
