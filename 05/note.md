<!--
Filename: 	note.md
Project: 	/Users/shume/Developer/DeepLearningBook/05
Author: 	shumez <https://github.com/shumez>
Created: 	2019-06-06 18:02:1
Modified: 	2019-06-08 12:56:38
-----
Copyright (c) 2019 shumez
-->

# 05. Machine Learning Basics

## Contents

* [05.00.][0500]
* [05.01. Learning Algorithms][0501]
    * [05.01.01. The Task, \(T\)][050101]
    * [05.01.02. The Performance Measure, \(P\)][050102]
    * [05.01.03. The Experience, \(E\)][050103]
    * [05.01.04. Example: Linear Regression][050104]
* [05.02. Capacity, Overfitting and Underfitting][0502]
    * [05.02.01. The No Free Lunch Theorem][050201]
    * [05.02.02. Regularization][050202]
* [05.03. Hyperparameters and Validation Sets][0503]
    * [05.03.01. Cross-Validation][050301]
* [05.04. Estimators, Bias and Variance][0504]
    * [05.04.01. Point Estimation][050401]
    * [05.04.02. Bias][050402]
    * [05.04.03. Variance and Standard Error][050403]
    * [05.04.04. Trading off Bias and Variance to Minimize Mean Squared Error][050404]
    * [05.04.05. Consistency][050405]
* [05.05. Maximum Likelihood Estimation][0505]
    * [05.05.01. Conditional Log-Likelihood and Mean Squared Error][050501]
    * [05.05.02. Properties of Maximum Likelihood][050502]
* [05.06. Bayesian Statistics][0506]
    * [05.06.01. Maximum *A Posteori* (MAP) Estimation][050601]
* [05.07. Supervised Learning Algorithm][0507]
    * [05.07.01. Probabilistic Supervised Learning][050701]
    * [05.07.02. Support Vector Machines][050702]
    * [05.07.03. Other Simple Supervised Learning Algorithms][050703]
* [05.08. Unsupervised Learning Algorithms][0508]
    * [05.08.01. Principal Components Analysis][050801]
    * [05.08.02. \(k\)-means Clustering][050802]
* [05.09. Stochastic Gradient Descent][0509]
* [05.10. Building a Mchine Learning Algorithm][0510]
* [05.11. Challenges Motivating Deep Learning][0511]
    * [05.11.01. The Curse of Dimensionality][051101]
    * [05.11.02. Local Constancy and Smoothness Regularization][051102]
    * [05.11.03. Monifold Learning][051103]

## 05.00.

[Murphy (2012)][2012_Murphy], [Bishop (2006)][2006_Bishop]

## 05.01. Learning Algorithms
### 05.01.01. The Task, \(T\)
### 05.01.02. The Performance Measure, \(P\)
### 05.01.03. The Experience, \(E\)
### 05.01.04. Example: Linear Regression
## 05.02. Capacity, Overfitting and Underfitting
### 05.02.01. The No Free Lunch Theorem
### 05.02.02. Regularization
## 05.03. Hyperparameters and Validation Sets
### 05.03.01. Cross-Validation
## 05.04. Estimators, Bias and Variance
### 05.04.01. Point Estimation
### 05.04.02. Bias
### 05.04.03. Variance and Standard Error
### 05.04.04. Trading off Bias and Variance to Minimize Mean Squared Error
### 05.04.05. Consistency
## 05.05. Maximum Likelihood Estimation
### 05.05.01. Conditional Log-Likelihood and Mean Squared Error
### 05.05.02. Properties of Maximum Likelihood
## 05.06. Bayesian Statistics
### 05.06.01. Maximum *A Posteori* (MAP) Estimation
## 05.07. Supervised Learning Algorithm
### 05.07.01. Probabilistic Supervised Learning
### 05.07.02. Support Vector Machines
### 05.07.03. Other Simple Supervised Learning Algorithms
## 05.08. Unsupervised Learning Algorithms
### 05.08.01. Principal Components Analysis
### 05.08.02. \(k\)-means Clustering
## 05.09. Stochastic Gradient Descent
## 05.10. Building a Mchine Learning Algorithm
## 05.11. Challenges Motivating Deep Learning
### 05.11.01. The Curse of Dimensionality
### 05.11.02. Local Constancy and Smoothness Regularization
### 05.11.03. Monifold Learning



##
<!-- toc -->
[0500]: #0500
[0501]: #0501_learning_algorithms
[050101]: #050101_the_task_t
[050102]: #050102_the_performance_measure_p
[050103]: #050103_the_experience_e
[050104]: #050104_example_linear_regression
[0502]: #0502_capacity_overfitting_and_underfitting
[050201]: #050201_the_no_free_lunch_theorem
[050202]: #050202_regularization
[0503]: #0503_hyperparameters_and_validation_sets
[050301]: #050301_cross-validation
[0504]: #0504_estimators_bias_and_variance
[050401]: #050401_point_estimation
[050402]: #050402_bias
[050403]: #050403_variance_and_standard_error
[050404]: #050404_trading_off_bias_and_variance_to_minimize_mean_squared_error

<!-- ref -->
[2012_Murphy]: #
[2006_Bishop]: #

<!-- fig -->

<!-- term -->

<style type="text/css">
	img{width: 51%; float: right;}
</style>