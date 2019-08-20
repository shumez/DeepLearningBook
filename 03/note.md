<!--
Filename: 	note.md
Project: 	/Users/shume/Developer/DeepLearningBook/03
Author: 	shumez <https://github.com/shumez>
Created: 	2019-06-03 19:38:5
Modified: 	2019-08-20 14:40:25
-----
Copyright (c) 2019 shumez
-->

# [03. Probability and Information Theory]

## Contents

- [03.00.][0300]
- [03.01. Why Probability?][0301]
- [03.02. Random Variables][0302]
- [03.03. Probability Distributions][0303]
	- [03.03.01. Disctrete Variables and Probability Mass Functions][030301]
	- [03.03.02. Continuous Variables and Probability Density Functions][030302]
- [03.04. Marginal Probability][0304]
- [03.05. Conditional Probability][0305]
- [03.06. The Chain Rule of Conditional Probabilities][0306]
- [03.07. Independence and Conditional Independence][0307]
- [03.08. Expectation, Variance and Covariance][0308]
- [03.09. Common Probability Distributions][0309]
	- [03.09.01. Bernouulli Distribution][030901]
	- [03.09.02. Multinoulli Distribution][030902]
	- [03.09.03. Gaussian Distribution][030903]
- [03.10. Useful Properties of Common Functions][0310]
- [03.11. Bayes’ Rule][0311]
- [03.12. Technical Details of Continuous Variables][0312]
- [03.13. Information Theory][0313]
- [03.14. Structured Probabilistic Models][0314]


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

**marginal probability** distribution

**sum rule**

for discrete rand var 

\[ \forall x \in \mathrm{x}, P(\mathrm{x}=x) = \sum_y{P(\mathrm{x}=x, \mathrm{y}=y)} \tag{3.3} \]

for continulous var

\[p(x) = \int{p(x,y)dy} \tag{3.4}\]


## 03.05. Conditional Probability

**conditional probability**

\[ P(\mathrm{y}=y | \mathrm{x}=x) = \frac{P(\mathrm{y}=y, \mathrm{x}=x)}{P(\mathrm{x}=x)} \tag{3.5} \]



**intervention query**: domain of **causal modeling**


## 03.06. The Chain Rule of Conditional Probabilities

joint prob dist may be decomposed into conditional dist

\[ P(\mathrm{x}^{(1)}, \cdots \mathrm{x}^{(n)}) = P(\mathrm{x}^{(1)}) \prod_{i=2}^n{P(\mathrm{x}^{(i)} | \mathrm{x}^{(1)}, \cdots, \mathrm{x}^{(i-1)})} \tag{3.6} \]

**chain rule** (**product rule**)

e.g., 

\[
	\begin{align*}
		P(a,b,c) &= P(a | b,c) P(b,c) \\
		P(b,c) &= P(b | c) P(c) \\
		P(a,b,c) &= P(a | b,c) P(b | c) P(c)
	\end{align*}
\]


## 03.07. Independence and Conditional Independence

2 random vars \(\mathrm{x}\) and \(\mathrm{y}\) are **independent**

\[\forall x \in \mathrm{x}, y \in \mathrm{y},\\ p(\mathrm{x}=x, \mathrm{y}=y) = p(\mathrm{x}=x) p(\mathrm{y}=y) \tag{3.7} \]

\(\mathrm{x}\) and \(\mathrm{y}\) are **conditionally independent**

\[\forall x \in \mathrm{x}, y \in \mathrm{y}, z \in \mathrm{z},\\ p(\mathrm{x}=x, \mathrm{y}=y | \mathrm{z}=z) = p(\mathrm{x}=x | \mathrm{z}=z) p(\mathrm{y}=y | \mathrm{z}=z) \tag{3.8} \]

\(\mathrm{x} \perp \mathrm{y}\) means that independent

\(\mathrm{x} \perp \mathrm{y} | \mathrm{z}\) means that \(\mathrm{x}\) and \(\mathrm{y}\) are conditionally independent \(\mathrm{z}\)


## 03.08. Expectation, Variance and Covariance

**expectation** (**expected value**) of some fn \(f(x)\) w respect to a prob dist \(P(x)\)

for discrete var 

\[ \mathbb{E}_{\mathrm{x} \sim P} [f(x)] = \sum_x{P(x) f(x)} \tag{3.9} \]

for continuous vars

\[ \mathbb{E}_{\mathrm{x} \sim p} [f(x)] = \int{p(x) f(x) dx} \tag{3.10} \]

expectation are linear 

\[ \mathbb{E}_{\mathrm{x}} [\alpha f(x) + \beta g(x)] = \alpha \mathbb{E}_{\mathrm{x}} [f(x)] + \beta \mathbb{E}_{\mathrm{x}} [g(x)] \tag{3.11} \]

when \(\alpha\) and \(\beta\) NOT dependent on \(x\)

**variance**

\[ \text{Var} \big( f(x) \big) = \mathbb{E} \Bigg[ \bigg(f(x) - \mathbb{E} \Big[ f(x) \Big] \bigg)^2 \Bigg] \tag{3.12} \]

**standard deviation**


**covariance**

\[ \text{Cov} \big( f(x), g(y) \big) = \mathbb{E} \Bigg[ \bigg( f(x) - \mathbb{E} \Big[ f(x) \Big] \bigg) \bigg( g(y) - \mathbb{E} \Big[ g(y) \Big] \bigg) \Bigg] \tag{3.13} \]

**covariance matrix**

\[ \text{Cov}(\mathrm{x}_{i,j}) = \text{Cov} (\mathrm{x}_i, \mathrm{x}_j) \tag{3.14} \]

\[ \text{Cov} (\mathrm{x}_i, \mathrm{x}_i) = \text{Var}(\mathrm{x}_i) \tag{3.15} \]


## 03.09. Common Probability Distributions

### 03.09.01. Bernouulli Distribution

**Bernoulli** dist

\[ P(\mathrm{x}=1) = \phi \tag{3.16} \]
\[ P(\mathrm{x}=0) = 1- \phi \tag{3.17} \]
\[ P(\mathrm{x}=x) = \phi^x (1 - \phi)^{1-x} \tag{3.18} \]
\[ \mathbb{E}_{\mathrm{x}} = \phi \tag{3.19} \]
\[ \text{Var}_{\mathrm{x}}(\mathrm{x}) = \phi(1 - \phi) \tag{3.20} \]


### 03.09.02. Multinoulli Distribution

**multinoulli** (**categorical**) dist

single discrete var w \(k\) diff states

vector \(p\in[0,1]^{k-1}\)


### 03.09.03. Gaussian Distribution

**normal distribution** (aka, **Gaussian distribution**)

\[ \mathcal{N} (x; \mu, \sigma^2) = \sqrt{\frac{1}{2\pi\sigma^2}} \exp{\Big( - \frac{1}{2\sigma^2} (x - \mu)^2 \Big)} \tag{3.21} \]

\(\mu \in \mathbb{R}\), \(\sigma \in (0, \infty)\)

\[ \mathcal{N} (x; \mu, \beta^{-1}) = \sqrt{\frac{\beta}{2\pi}} \exp{\Big( - \frac{1}{2} \beta (x - \mu)^2 \Big)} \tag{3.22} \]

**central limit theorem**



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
[030901]: #030901_bernouulli_distribution
[030902]: #030902_multinoulli_distribution
[030903]: #030903_gaussian_distribution
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