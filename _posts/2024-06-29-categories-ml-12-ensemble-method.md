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

date: 2024-06-29
last_modified_at: 2024-06-29
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
- 