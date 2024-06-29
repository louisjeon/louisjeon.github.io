---
title: "K-Means Clusturing"
excerpt: "About K-Means Clusturing"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/11/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-29
last_modified_at: 2024-06-29
---

## K-means Error
- Error estimation of K-means can be defined as sum of distances between clusters and each allocated samples
  - Error function below can be optimalized by gradient descent
  - However, Lloyd's algorithm converges faster than gradient descent (Bottou and Bengio, 1995)
    #### $J(Z,U) = \displaystyle\sum_{i=1}^{N}\displaystyle\sum_{j=1}^{k}\boldsymbol{u}_{ji}\|\boldsymbol{x_i}-\boldsymbol{z_j}\|^2$
    $N$: Number of samples
    $k$: Number of clusters
    $x_i$: $i$th sample
    $u_{ji}$: 1 if $\boldsymbol{x_i}$ in $C_j$(cluster of $\boldsymbol{z}_j$) else 0, $\boldsymbol{u} \in \boldsymbol{Z}$
    $\boldsymbol{z}_j$: Center of $j$th cluster, $\boldsymbol{z} \in \boldsymbol{Z}$
    $Z$: Set of cluster centers
    $U$: Set of membership

## Limitations of K-means
- Sensitive to initial values
- Can fall into local minima
- Sensitive to outlier
- Variety of K-means
  - Multi start K-means
  - K-medoids