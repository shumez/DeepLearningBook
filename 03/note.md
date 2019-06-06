<!--
Filename: 	note.md
Project: 	/Users/shume/Developer/DeepLearningBook/03
Author: 	shumez <https://github.com/shumez>
Created: 	2019-06-03 19:38:5
Modified: 	2019-06-06 17:52:24
-----
Copyright (c) 2019 shumez
-->

# [03. Probability and Information Theory]

## Contents

* [03.00.][0300]
* [03.01. Why Probability?][0301]
* [03.02. Random Variables][0302]
* [03.03. Probability Distributions][0303]
	* [03.03.01. Disctrete Variables and Probability Mass Functions][030301]
	* [03.03.02. Continuous Variables and Probability Density Functions][030302]
* [03.04. Marginal Probability][0304]
* [03.05. Conditional Probability][0305]
* [03.06. The Chain Rule of Conditional Probabilities][0306]
* [03.07. Independence and Conditional Independence][0307]
* [03.08. Expectation, Variance and Covariance][0308]
* [03.09. Common Probability Distributions][0309]
* [03.10. Useful Properties of Common Functions][0310]
* [03.11. Bayes’ Rule][0311]
* [03.12. Technical Details of Continuous Variables][0312]
* [03.13. Information Theory][0313]
* [03.14. Structured Probabilistic Models][0314]


## 03.00.

[Jaynes (2003)][2003_Jaynes]


## 03.01. Why Probability?

**frequent prob**

**Bayesian prob**

[Ramsey (1926)][1926_Ramsey]


## 03.02. Random Variables

**random var**


## 03.03. Probability Distributions

**probability dist**


### 03.03.01. Disctrete Variables and Probability Mass Functions

**probability mass fn** (PMF) \(P(x)\)

define var, specify which dist it follows  
\(\mathrm{x} \sim P(\mathrm{x})\)

**joint prob dist** \(P(\mathrm{x} = x, \mathrm{y} = y)\)


* \(\forall x \in \mathrm{x}, 0 \le P(x) \le 1\)
* \(\sum_{x \in \mathrm{x}}{P(x)} = 1\), **normalized**

**uniform dist**

\[ P(\mathrm{x} = x_i) = \frac{1}{k} \tag{3.1} \]

\[ \sum_i{P(\mathrm{x} = x_i)} = \sum_i{\frac{1}{k}} = \frac{k}{k} = 1 \tag{3.2} \]


### 03.03.02. Continuous Variables and Probability Density Functions

**probability density fn** (PDF) \(p\)

* \(\forall x \in \mathrm{x}, p(x) \ge 0\)  
	NOT require \(p(x) \le 1\)
* \(\int{p(x) dx} = 1\)

## 03.04. Marginal Probability
## 03.05. Conditional Probability
## 03.06. The Chain Rule of Conditional Probabilities
## 03.07. Independence and Conditional Independence
## 03.08. Expectation, Variance and Covariance
## 03.09. Common Probability Distributions
## 03.10. Useful Properties of Common Functions
## 03.11. Bayes’ Rule
## 03.12. Technical Details of Continuous Variables
## 03.13. Information Theory
## 03.14. Structured Probabilistic Models




##
[03. Probability and Information Theory]: https://www.deeplearningbook.org/contents/prob.html

<!-- toc -->
[0300]: #0300
[0301]: #0301_why_probability
[0302]: #0302_random_variables
[0303]: #0303_probability_distributions
[030301]: #030301_disctrete_variables_and_probability_mass_functions
[030302]: #030302_continuous_variables_and_probability_density_functions
[0304]: #0304_marginal_probability
[0305]: #0305_conditional_probability
[0306]: #0306_the_chain_rule_of_conditional_probabilities
[0307]: #0307_independence_and_conditional_independence
[0308]: #0308_expectation_variance_and_covariance
[0309]: #0309_common_probability_distributions
[0310]: #0310_useful_properties_of_common_functions
[0311]: #0311_bayes_rule
[0312]: #0312_technical_details_of_continuous_variables
[0313]: #0313_information_theory
[0314]: #0314_structured_probabilistic_models

<!-- ref -->
<!-- 0300 -->
[2003_Jaynes]: #0300

<!-- 0301 -->
[1926_Ramsey]: #0301

<!-- fig -->

<!-- term -->

<style type="text/css">
	img{width: 51%; float: right;}
</style>