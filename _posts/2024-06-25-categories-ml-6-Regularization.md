---
title: "Model Accessment"
excerpt: "About Model Accessmen"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/7/

toc: true
toc_sticky: true
use_math: true

date: 2024-06-25
last_modified_at: 2024-06-25
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
  #### $Accuracy = \frac{\Sigma_iequals(y^{(i)},\widehat{y}^{(i)})}{N}=\frac{\#\ of\ correct}{\#\ of\ correct\ +\ \#\ of\ incorrect}$

## Precision and Recall
- True positives + false negatives = Real positives
- True Negatives + false positives = Real negatives

## Precision
  - Ratio of real positives out of expected positives
    #### $precision = \frac{TP}{TP + FP}$

## Recall
  - Ratio of expected positives out of real positives
    #### $recall = \frac{TP}{TP + FN}$