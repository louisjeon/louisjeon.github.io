---
title: "Ensemble Method"
excerpt: "About Ensemble Method"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/12/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-30
last_modified_at: 2024-06-30
---

## Ensemble Model
- Combine multiple models
- Different models can fill each other's gaps
  - Input -> A+B+C+D Model -> Combination algorithm -> Output
- Three problems of the ensemble system
  - Ensemble generation -> Ensemble choice -> Ensemble combination

## Ensemble generation
- What is ensemble generation?
  - Generating multiple classifiers
  - Classifiers that constitutes ensemble
    - Component classifier = Base classifier
- How to generate ensemble
  - Re-sampling the training set
    - Bagging
    - Boosting
  - Using different classification algorithms
    - Use various classifiers like MLP, SVM, KNN
  - Using subspace of feature vecter
    - Use different subspace of feature vecter as a feature vecter for each classifier 
      - ex) decision tree

## Bagging
  - Originated from bootstap aggregating
  - Sample $K$ number of subsets from data $D \to X = \{X_1, X_2, ..., X_k\}$
  - Train $K$ number of classifiers with each one
    - train model $C_i$ with $X_i$
    - $\boldsymbol{C} = \boldsymbol{C} \cup C_i$
  - return set of classifiers $\boldsymbol{C} = \{C_1, C_2, ..., C_K\}$

## Boosting
- Classifier $C_i$ and $C_{i+1}$ is related
- Add more weight to the samples that had not been classified well by $C_i$ so that they are well classified when training next classifier $C_{i+1}$

## Boosting - Adaboost
- Assign same weight to all sampels initially
- Train classifier $C_t$ with $D$ weighted by $W_t$

## Ensemble Combination
- An algorithm to assemble outputs from various classifiers
- Ensemble combination method
  - Class label based
  - Class probability based
  - Class ranking based

## Class label based
- Final label that a model selected as an output
- Class label vector (one-hot incoding)
  - $l = (0,0,1,0)$: 3rd label
  - $l = (1,0,0,0)$: 1st label
  
## Class label based majority voting
- Choose the most selected label by classifiers as the final label
  #### $y = \displaystyle\operatorname*{argmax}_{j}\displaystyle\sum_{t=1}^{T}l_{tj}$
  $l$: Class label vector
  $l_{tj}$: $j$th label from $t$th model
  $y$: Final predicted label

## Class label based weighted majority voting
- Choose the final label with weighted majority voting considering credibility and laverage of classifiers
  #### $y = \displaystyle\operatorname*{argmax}_{j}\displaystyle\sum_{t=1}^{T}\alpha_tl_{tj}$
  $l$: Class label vector
  $l_{tj}$: $j$th label from $t$th model
  $\alpha_t$: Reliability and leverage of $t$th model
  $y$: Final predicted label

## Class probability based
- What is class probability?
  - Output probability of each classifier from a model
- Class probability vector
  - Vectorized probability of each classifier
    - $p = (0.6, 0.2, 0.15, 0.05)$

  #### Sum: $y = \displaystyle\operatorname*{argmax}_{j}\displaystyle\sum_{t=1}^{T}p_{tj}$
  #### Weighted Sum: $y = \displaystyle\operatorname*{argmax}_{j}\displaystyle\sum_{t=1}^{T}\alpha_tp_{tj}$
  #### Multiplication: $y = \displaystyle\operatorname*{argmax}_{j}\displaystyle\prod_{t=1}^{T}p_{tj}$
  #### Maximum Probability: $y = \displaystyle\operatorname*{argmax}_{j}p_{tj}$

## Class ranking based
- What is a class ranking?
  - Ranking of classes
- Class ranking vector
  - Vectorized class ranking expression
    - $R = (1,2,3,4)$
    - Ranking vector transform to calculate Borda count
    - Method 1
      - Number of elements - element value
      - $S = (3,2,1,0)$
    - Method 2
      - Number of elements / Element value
      - $S = (\frac{4}{1},\frac{4}{2},\frac{4}{3},\frac{4}{4})$