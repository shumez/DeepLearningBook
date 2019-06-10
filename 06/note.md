<!--
Filename: 	note.md
Project: 	/Users/shume/Developer/DeepLearningBook/06
Author: 	shumez <https://github.com/shumez>
Created: 	2019-06-10 09:01:2
Modified: 	2019-06-10 09:39:32
-----
Copyright (c) 2019 shumez
-->

# [06. Deep Feedforward Networks]

## Contents

* [06.00.][0600]
* [06.01. Example: Learning XOR][0601]
* [06.02. Gradient-Based Learning][0602]
    * [06.02.01. Cost Functions][060201]
        * [06.02.01.01. Learning Conditional Distributions with Maximum Likelihood][06020101]
        * [06.02.01.02. Learning Conditional Statistics][06020102]
    * [06.02.02. Output Units][060202]
        * [06.02.02.01. Linear Units for Gaussian Output Distributions][06020201]
        * [06.02.02.02. Sigmoid Units for Bernoulli Output Distributions][06020202]
        * [06.02.02.03. Softmax Units for Multinoulli Output Distributions][06020203]
        * [06.02.02.04. Other Output Types][06020204]
* [06.03. Hidden Units][0603]
    * [06.03.01. Rectiﬁed Linear Units and Their Generalizations][060301]
    * [06.03.02. Logistic Sigmoid and Hyperbolic Tangent][060302]
    * [06.03.03. Other Hidden Units][060303]
* [06.04. Architecture Design][0604]
    * [06.04.01. Universal Approximation Properties and Depth][060401]
    * [06.04.02. Other Architectural Considerations][060402]
* [06.05. Back-Propagation and Other Differentiation Algorithms][0605]
    * [06.05.01. Computational Graphs][060501]
    * [06.05.02. Chain Rule of Calculus][060502]
    * [06.05.03. Recursively Applying the Chain Rule to Obtain Backprop][060503]
    * [06.05.04. Back-Propagation Computation in Fully Connected MLP][060504]
    * [06.05.05. Symbol-to-Symbol Derivatives][060505]
    * [06.05.06. General Back-Propagation][060506]
    * [06.05.07. Example: Back-Propagation for MLP Training][060507]
    * [06.05.08. Complications][060508]
    * [06.05.09. Diﬀerentiation outside the Deep Learning Community][060509]
    * [06.05.10. Higher-Order Derivatives][060510]
* [06.06. Historical Notes][0606]


## 06.00.
## 06.01. Example: Learning XOR
## 06.02. Gradient-Based Learning
### 06.02.01. Cost Functions
#### 06.02.01.01. Learning Conditional Distributions with Maximum Likelihood
#### 06.02.01.02. Learning Conditional Statistics
### 06.02.02. Output Units
#### 06.02.02.01. Linear Units for Gaussian Output Distributions
#### 06.02.02.02. Sigmoid Units for Bernoulli Output Distributions
#### 06.02.02.03. Softmax Units for Multinoulli Output Distributions
#### 06.02.02.04. Other Output Types
## 06.03. Hidden Units
### 06.03.01. Rectiﬁed Linear Units and Their Generalizations
### 06.03.02. Logistic Sigmoid and Hyperbolic Tangent
### 06.03.03. Other Hidden Units
## 06.04. Architecture Design
### 06.04.01. Universal Approximation Properties and Depth
### 06.04.02. Other Architectural Considerations
## 06.05. Back-Propagation and Other Differentiation Algorithms
### 06.05.01. Computational Graphs
### 06.05.02. Chain Rule of Calculus
### 06.05.03. Recursively Applying the Chain Rule to Obtain Backprop
### 06.05.04. Back-Propagation Computation in Fully Connected MLP
### 06.05.05. Symbol-to-Symbol Derivatives
### 06.05.06. General Back-Propagation
### 06.05.07. Example: Back-Propagation for MLP Training
### 06.05.08. Complications
### 06.05.09. Diﬀerentiation outside the Deep Learning Community
### 06.05.10. Higher-Order Derivatives
## 06.06. Historical Notes




##
[06. Deep Feedforward Networks]: https://www.deeplearningbook.org/contents/mlp.html

<!-- toc -->
[0600]: #0600
[0601]: #0601_example_learning_xor
[0602]: #0602_gradient-based_learning
[060201]: #060201_cost_functions
[06020101]: #06020101_learning_conditional_distributions_with_maximum_likelihood
[06020102]: #06020102_learning_conditional_statistics
[060202]: #060202_output_units
[06020201]: #06020201_linear_units_for_gaussian_output_distributions
[06020202]: #
[06020203]: #
[06020204]: #
[0603]: #0603_hidden_units
[060301]: #
[060302]: #
[060303]: #
[0604]: #0604_architecture_design
[060401]: #
[060402]: #
[0605]: #0605_back-propagation_and_other_differentiation_algorithms
[060501]: #
[060502]: #
[060503]: #
[060504]: #
[060505]: #
[060506]: #
[060507]: #
[060508]: #
[060509]: #
[060510]: #
[0606]: #0606_historical_notes

<!-- ref -->

<!-- fig -->

<!-- term -->

<style type="text/css">
	img{width: 51%; float: right;}
</style>