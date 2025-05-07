---
title: "Eigenvalue and Eigenvector"
excerpt: "About Eigenvalue and Eigenvector"

categories:
  - Machine Learning
tags:
  - [tag1, tag2]

permalink: /ml/13/

toc: true
toc_sticky: true
use_math: true

date: 2025-05-07
last_modified_at: 2025-05-07
---

## Eigenvalue and Eigenvector
- Eigenvalue and Eigenvector are concepts that represent core characteristics of a matrix in linear algebra
- For square matrix A, eigenvector is a non-zero vector that direction is unchanged when linear transformation is applied and agenvalue represents the rate of change at this time. Mathmatically represented as $Ax = {\lambda}x$.

## Meaning of Eigenvalue and Eigenvector
### Attribute of linear transformation
- Matrix A executes linear transformation (roation, expansion, reduction, etc...) in a vector space. The directon of eigenvector is identical after the transformation and eigenvalue ${\lambda}$ means scaling the vector |${\lambda}$| times.
  - ${\lambda}>1$: vector expansion
  - $0 < {\lambda} <1$: vector reduction
  - ${\lambda}<0$: direction reversal

### Mathmatical definition
- Eigenvalue is calculated by solving characteristics equation $det(A - {\lambda}I) = 0$ and eigenvector is decided as the value of $(A - {\lambda}I)x = 0$

## Importance and Application Domain
### Dimension Reduction and Data Analysis
#### PCA (Principal Component Analysis)
- Eigenvector of a covariance matrix represents maximum variance directon of data and eigenvalue decides importance of the direction. Through this, high-demensional data can be reduced into low-dimensional data.
### System Analysis
#### Vibration Analysis
- Evaluate stability of a structure by calculating natural frequency(eigenvalue) and frequency mode(eigenvector) of a machine system.
#### Quantum Dynamics
- Physical quantity like energy level is represented as eigenvalue of an operator.
### Calculation Efficiency
- Complexity is dramatically reduced when a matrix's involution $A^k$ is calculated with eigensolution. For example, when decomposed as $A = PDP^{-1}$, $A^k = PD^kP^{-1}$ is validated.
### Graph Theory
- Eigenvalue of an adjacency matrix is used for analyzing network connectivity, community structure and etc.

## Example
- For matrix $A = {\begin{pmatrix}2 & 1 \\ 1 & 2\end{pmatrix}}$,
  - Eigenvalue: ${\lambda_1 = 3, \lambda_2 = 1}$
  - Eigenvector: $v_1 = \begin{pmatrix}1 \\ 1\end{pmatrix}, v_2 = \begin{pmatrix}-1 \\ 1\end{pmatrix}$