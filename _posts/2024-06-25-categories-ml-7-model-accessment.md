---
title: "Model Accessment"
excerpt: "About Model Accessment"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/7/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-26
last_modified_at: 2024-06-26
---

## What is a Model Accessment?
- Evaluating model to match our purpose
  - Metric
  - train/validation/test sets

## Metric
- Indicators that estimate model's preformance on a data set
  - Cost, Error
  - Accuracy
  - Precision
  - Recall

## Cost, Error
- Output of cost function
- Calculated difference between model and data set by cost function

## Accuracy
- Ratio of correct answers from entire sample number of data set
#### $Accuracy = \frac{\Sigma_iequals(y^{(i)},\widehat{y}^{(i)})}{N}=\frac{Number\ of\ correct}{Number\ of\ correct\ +\ Number\ of\ incorrect}$

## Precision and Recall
- True positives + false negatives = Real positives
- True Negatives + false positives = Real negatives

## Precision
  - Ratio of real positives out of expected positives
    #### $precision = \frac{TP}{TP + FP}$

## Recall
  - Ratio of expected positives out of real positives
    #### $recall = \frac{TP}{TP + FN}$

## Precision Recall Trade-off
- Model's decision border can be moved by adjusting threshold
  - There is a trade-off of precision and recall by changing threshold
- Setting high threshold results in high precision and low recall
- Setting low threshold results in low precision and high recall

## F1 score
- Harmonic mean of precision and recall
- F1 score is used when evaluating model's performance considering both precision and recall scores
- F1 score stays the same when threshold trades off precision and recall

  #### $precision = \frac{TP}{TP+FP}$
  #### $recall = \frac{TP}{TP+FN}$
  #### $f1\ score = \frac{2\cdot precision\cdot recall}{precision + recall}$

## Datasets
- Dataset consists of train set, validation set and test set
  - Train set
    - Dataset that is directly used for model parameter train
  - Validation set
    - Dataset that is used to find $h_\theta$ with high performance from hypothesis set $\mathcal{H} = \{h_{\theta^1}, h_{\theta^2}, ..., h_{\theta^I}\}$ which is made from model's learning process
      - $\hat{h}_\boldsymbol\theta = \displaystyle\operatorname*{argmin}_{h_\boldsymbol\theta\in\mathcal{H}}\sum_{i}^{N}metric(h_\boldsymbol\theta(\boldsymbol{x}^{(i)}),y^{(i)})$
  - Test set
    - Dataset that is used to evaluate model's final performance
- Things to keep in mind when dividing dataset
  - Divide to fit the purpose
  - Keep similar data distribution between train set, validation set and test set in most cases

## Model Selection
- Model selection is a process of selecting best model from hypothesis set $\mathcal{H}$
  $\hat{h}_\boldsymbol{\mathcal{H}} = \displaystyle\operatorname*{argmin}_{h_{\boldsymbol\theta}\in\mathcal{H}}\sum_{(x,y)\in D_{valid}}^{N} cost(h_{\boldsymbol\theta}(x),y)$

## Cross Validation
- How to access final performance after model selection?
  - Cross Validation
    - Methodology of model accessment
  - Popular cross validation methods
    - Holdout cross validation
    - K-fold cross validation
- Holdout cross validation
  - Fix dataset after dividing train set, validation set and test set
  - Decide final model only using validation set and record the performance of test set
    $Score_{test} = \frac{1}{N}\displaystyle\sum_{(x,y)\in D_{test}}^{N}metric(\hat{h}_\boldsymbol\theta(x),y)$
    $\hat{h}_\theta = \displaystyle\operatorname*{argmin}_{h_\theta\in\mathcal{H}}\displaystyle\sum_{(x,y)\in D_{valid}}^{N}cost(h_\theta(x),y)$
- K-fold cross validation
  - Devide the train set with K folds and use each fold as test set to calculate the performance and average the scores

## Model Diagnosis
- Bias vs Variance
- Learning curves

## Bias vs Variance
- Bias? Variance?
- High variance = model is too complicated = overfitting = low versatility
- High bias = model is too simgple = underfitting = low performance
- Need to find optimal model complexity

## Learning Curves
- A model can be diagnosed as high bias or high variance through learning curve
- In case of high bias
  - Quick convergence of performance for a small train set
  - High error
  - Adding more data won't work
- In case of high variance
  - Big difference between validation cost and training cost
  - Posibility of performance improvement by adding more data