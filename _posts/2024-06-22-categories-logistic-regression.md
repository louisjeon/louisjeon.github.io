---
title: "Logistic Regression"
excerpt: "About Logistic Regression..."

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/2/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-22
last_modified_at: 2024-06-22
---

## Classification

- Spam or Not?
- Positive or Negative?
- Dog or Cat or Elephant?
- Slecting N items out of descrete K
  - Binary classification: K=2, N=1
  - Multi class classification: K>2, N=1
  - Multi label classification: K>=2, N>1
  - One class classification: K=1, N=1

## Model Representation

- Supervised Learning
- $P(y|x)$
- Data set
  - $D = \{(x^{(1)}, y^{(1)}), ..., (x^{(N)}, y^{(N)})\}$
- Hypothesis set

  - $\mathcal{H} = \{\mathcal{H}_1, \mathcal{H}\_2, ...\}$
    $\widehat{M} = \displaystyle\operatorname*{argmin}_{M\in\mathcal{H}}\displaystyle\sum_{i}^{N}l(M(x^{(i)}),y^{(i)})$

- Model's output should be between 0 and 1 to make a probability approximation model

  - Logistic function

    - Sigmoid Function (Logistic function with K=1, B=0)
      $\sigma(x) = \frac{1}{1+e^{-x}}$
      <br/>

    $\boldsymbol\theta = \begin{bmatrix}\theta_1\\\theta_2\end{bmatrix}, \boldsymbol{x}=\begin{bmatrix}x_1\\x_2\end{bmatrix},y\in\{0,1\}$<br/>
    $P_{\theta}(y=1|\boldsymbol{x})=\sigma(g(\boldsymbol{x}))=\sigma(\boldsymbol\theta^T\boldsymbol{x} + \theta_0)=\frac{1}{1+e^{-(\boldsymbol\theta^Tx+\theta_0)}}=\sigma(\theta_1x_1+\theta_2x_2+\theta_0)=\frac{1}{1+e^{-(\theta_1x_1+theta_2x_2+theta_0)}}$<br/>

    ### $g(x) = \theta_0 + \theta_1x_1 + \theta_2x_2 + \cdots + \theta_nx_n$

&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;logit&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;$x_1=$tumor size, $x_2$=gender
