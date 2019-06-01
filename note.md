<!--
Filename: 	note.md
Project: 	/Users/shume/Developer/DeepLearningBook
Author: 	shumez <https://github.com/shumez>
Created: 	2018-07-06 13:36:3
Modified: 	2019-06-01 20:38:45
-----
Copyright (c) 2019 shumez
-->

# [Deep Learning Book]

[![Cover][cover]][cover]

## Contents

* [Part 0.][P0]
    * [01. Introduction][01]
        <!-- * [1.1 Who Should Read This Book?]() -->
        <!-- * [1.2 Historical Trends in Deep Learning]() -->
* [Part I. Applied Math and Machine Learning Basics][PI]
    * [02. Linear Algebra][02]
        <!-- - 2.1 Scalars,Vectors, MatricesandTensors -->
        <!-- - 2.2 Multiplying Matrices and Vectors -->
        <!-- - 2.3 Identity and Inverse Matrices -->
        <!-- - 2.4 Linear Dependence and Span -->
        <!-- - 2.5 Norms -->
        <!-- - 2.6 Special Kinds of Matricesand Vectors -->
        <!-- - 2.7 Eigendecomposition -->
        <!-- - 2.8 Singular Value Decomposition -->
        <!-- - 2.9 The Moore-Penrose Pseudoinverse -->
        <!-- - 2.10 The Trace Operator -->
        <!-- - 2.11 The Determinant -->
        <!-- - 2.12 Example: PrincipalComponentsAnalysis -->
    * [03. Probability and Information Theory][03]
        <!-- - 3.1 Why Probability? -->
        <!-- - 3.2 Random Variables -->
        <!-- - 3.3 Probability Distributions -->
        <!-- - 3.4 Marginal Probability -->
        <!-- - 3.5 Conditional Probability -->
        <!-- - 3.6 TheChainRuleofConditionalProbabilities -->
        <!-- - 3.7 Independence and Conditional Independence -->
        <!-- - 3.8 Expectation,VarianceandCovariance -->
        <!-- - 3.9 Common Probability Distributions -->
        <!-- - 3.10 UsefulPropertiesofCommonFunctions -->
        <!-- - 3.11 Bayes’ Rule -->
        <!-- - 3.12 Technical Details of Continuous Variables -->
        <!-- - 3.13 Information Theory -->
        <!-- - 3.14 Structured Probabilistic Models -->
    * [04. Numerical Computation][04]
        <!-- - 4.1 Overflow and Underflow -->
        <!-- - 4.2 Poor Conditioning -->
        <!-- - 4.3 Gradient-Based Optimization -->
        <!-- - 4.4 Constrained Optimization . . -->
        <!-- - 4.5 Example: Linear Least Squares -->
    * [05. Machine Learning Basics][05]
        <!-- - 5.1 Learning Algorithms -->
        <!-- - 5.2 Capacity,OverfittingandUnderfitting -->
        <!-- - 5.3 HyperparametersandValidationSets -->
        <!-- - 5.4 Estimators, Bias and Variance -->
        <!-- - 5.5 Maximum Likelihood Estimation -->
        <!-- - 5.6 BayesianStatistics -->
        <!-- - 5.7 Supervised Learning Algorithms -->
        <!-- - 5.8 Unsupervised Learning Algorithms -->
        <!-- - 5.9 Stochastic Gradient Descent -->
        <!-- - 5.10 Building a Machine Learning Algorithm -->
        <!-- - 5.11 ChallengesMotivatingDeepLearning -->
* [Part II. Deep Networks: Modern Practices][PII]
    * [06. Deep Feedforward Networks][06]
        <!-- - 6.1 Example: Learning XOR -->
        <!-- - 6.2 Gradient-Based Learning -->
        <!-- - 6.3 Hidden Units -->
        <!-- - 6.4 Architecture Design -->
        <!-- - 6.5 Back-Propagation and Other Differentiation Algorithms -->
        <!-- - 6.6 Historical Notes -->
    * [07. Regularization for Deep Learning][07]
        <!-- - 7.1 Parameter Norm Penalties -->
        <!-- - 7.2 Norm Penalties as Constrained Optimization -->
        <!-- - 7.3 Regularization and Under-Constrained Problems -->
        <!-- - 7.4 Dataset Augmentation -->
        <!-- - 7.5 Noise Robustness -->
        <!-- - 7.6 Semi-Supervised Learning -->
        <!-- - 7.7 Multi-Task Learning -->
        <!-- - 7.8 EarlyStopping -->
        <!-- - 7.9 Parameter Tying and Parameter Sharing -->
        <!-- - 7.10 Sparse Representations -->
        <!-- - 7.11 BaggingandOtherEnsembleMethods -->
        <!-- - 7.12 Dropout -->
        <!-- - 7.13 Adversarial Training -->
        <!-- - 7.14 Tangent Distance, Tangent Prop, and Manifold Tangent Classifier -->
    * [08. Optimization for Training Deep Models][08]
        <!-- - 8.1 HowLearningDiffersfromPureOptimization -->
        <!-- - 8.2 Challenges in Neural Network Optimization -->
        <!-- - 8.3 Basic Algorithms -->
        <!-- - 8.4 Parameter Initialization Strategies -->
        <!-- - 8.5 AlgorithmswithAdaptiveLearningRates -->
        <!-- - 8.6 Approximate Second-Order Methods -->
        <!-- - 8.7 Optimization Strategies and Meta-Algorithms -->
    * [09. Convolutional Networks][09]
        <!-- - 9.1 The Convolution Operation -->
        <!-- - 9.2 Motivation -->
        <!-- - 9.3 Pooling -->
        <!-- - 9.4 Convolution and Pooling as an Infinitely Strong Prior -->
        <!-- - 9.5 Variants of the Basic Convolution Function -->
        <!-- - 9.6 Structured Outputs -->
        <!-- - 9.7 Data Types -->
        <!-- - 9.8 Efficient Convolution Algorithms -->
        <!-- - 9.9 Random or Unsupervised Features -->
        <!-- - 9.10 The Neuroscientific Basis for Convolutional Networks -->
        <!-- - 9.11 Convolutional Networks and the History of Deep Learning -->
    * [10. Sequence Modeling: Recurrent and Recursive Nets][10]
        <!-- - 10.1 Unfolding Computational Graphs -->
        <!-- - 10.2 Recurrent Neural Networks -->
        <!-- - 10.3 Bidirectional RNNs -->
        <!-- - 10.4 Encoder-Decoder Sequence-to-Sequence Architectures -->
        <!-- - 10.5 Deep Recurrent Networks -->
        <!-- - 10.6 Recursive Neural Networks -->
        <!-- - 10.7 TheChallengeofLong-TermDependencies -->
        <!-- - 10.8 Echo State Networks -->
        <!-- - 10.9 Leaky Units and Other Strategies for Multiple Time Scales -->
        <!-- - 10.10 The Long Short-Term Memory and Other Gated RNNs -->
        <!-- - 10.11 Optimization for Long-Term Dependencies -->
        <!-- - 10.12 Explicit Memory -->
    * [11. Practical Methodology][11]
        <!-- - 11.1 Performance Metrics -->
        <!-- - 11.2 Default Baseline Models -->
        <!-- - 11.3 Determining Whether to Gather More Data -->
        <!-- - 11.4 Selecting Hyperparameters -->
        <!-- - 11.5 Debugging Strategies -->
        <!-- - 11.6 Example: Multi-Digit Number Recognition -->
    * [12. Applications][12]
        <!-- - 12.1 Large-Scale Deep Learning -->
        <!-- - 12.2 Computer Vision -->
        <!-- - 12.3 Speech Recognition -->
        <!-- - 12.4 Natural Language Processing -->
        <!-- - 12.5 Other Applications -->
* [Part III. Deep Learning Research][PIII]
    * [13. Linear Factor Models][13]
        <!-- - 13.1 ProbabilisticPCAandFactorAnalysis -->
        <!-- - 13.2 IndependentComponentAnalysis(ICA) -->
        <!-- - 13.3 Slow Feature Analysis -->
        <!-- - 13.4 Sparse Coding -->
        <!-- - 13.5 Manifold Interpretation of PCA -->
    * [14. Autoencoders][14]
        <!-- - 14.1 Undercomplete Autoencoders -->
        <!-- - 14.2 Regularized Autoencoders -->
        <!-- - 14.3 Representational Power, Layer Size and Depth -->
        <!-- - 14.4 Stochastic Encoders and Decoders -->
        <!-- - 14.5 Denoising Autoencoders -->
        <!-- - 14.6 LearningManifoldswithAutoencoders -->
        <!-- - 14.7 Contractive Autoencoders -->
        <!-- - 14.8 Predictive Sparse Decomposition -->
        <!-- - 14.9 Applications of Autoencoders -->
    * [15. Representation Learning][15]
        <!-- - 15.1 Greedy Layer-Wise Unsupervised Pretraining -->
        <!-- - 15.2 TransferLearningandDomainAdaptation -->
        <!-- - 15.3 Semi-Supervised Disentangling of Causal Factors -->
        <!-- - 15.4 Distributed Representation -->
        <!-- - 15.5 Exponential Gains from Depth -->
        <!-- - 15.6 Providing Clues to Discover Underlying Causes -->
    * [16. Structured Probabilistic Models for Deep Learning][16]
        <!-- - 16.1 TheChallengeofUnstructuredModeling -->
        <!-- - 16.2 UsingGraphstoDescribeModelStructure -->
        <!-- - 16.3 Sampling from Graphical Models -->
        <!-- - 16.4 Advantages of Structured Modeling -->
        <!-- - 16.5 Learning about Dependencies -->
        <!-- - 16.6 InferenceandApproximateInference -->
        <!-- - 16.7 The Deep Learning Approach to Structured Probabilistic Models -->
    * [17. Monte Carlo Methods][17]
        <!-- - 17.1 Sampling and Monte Carlo Methods -->
        <!-- - 17.2 Importance Sampling -->
        <!-- - 17.3 Markov Chain Monte Carlo Methods -->
        <!-- - 17.4 Gibbs Sampling -->
        <!-- - 17.5 The Challenge of Mixing between Separated Modes -->
    * [18. Confronting the Partition Function][18]
        <!-- - 18.1 The Log-Likelihood Gradient -->
        <!-- - 18.2 Stochastic Maximum Likelihood and Contrastive Divergence -->
        <!-- - 18.3 Pseudolikelihood -->
        <!-- - 18.4 Score Matching and Ratio Matching -->
        <!-- - 18.5 Denoising Score Matching -->
        <!-- - 18.6 Noise-Contrastive Estimation -->
        <!-- - 18.7 Estimating the Partition Function -->
    * [19. Approximate Inference][19]
        <!-- - 19.1 Inference as Optimization -->
        <!-- - 19.2 Expectation Maximization -->
        <!-- - 19.3 MAP Inference and Sparse Coding -->
        <!-- - 19.4 Variational Inference and Learning -->
        <!-- - 19.5 Learned Approximate Inference -->
    * [20. Deep Generative Models][20]
        <!-- - 20.1 Boltzmann Machines -->
        <!-- - 20.2 Restricted Boltzmann Machines -->
        <!-- - 20.3 Deep Belief Networks -->
        <!-- - 20.4 Deep Boltzmann Machines -->
        <!-- - 20.5 BoltzmannMachinesforReal-Valued Data -->
        <!-- - 20.6 Convolutional Boltzmann Machines -->
        <!-- - 20.7 Boltzmann Machines for Structured or Sequential Outputs -->
        <!-- - 20.8 Other Boltzmann Machines -->
        <!-- - 20.9 Back-Propagation through Random Operations -->
        <!-- - 20.10 Directed Generative Nets -->
        <!-- - 20.11 Drawing Samples from Autoencoders -->
        <!-- - 20.12 Generative Stochastic Networks -->
        <!-- - 20.13 Other Generation Schemes -->
        <!-- - 20.14 Evaluating Generative Models -->
        <!-- - 20.15 Conclusion -->

## Resources

* [Deep Learning Book]
* [Lecture]
* [github]

##
<!-- toc -->
[P0]: #contents
[01]: 01/
[PI]: #contents
[02]: 02/
[03]: 03/
[04]: 04/
[05]: 05/
[PII]: #contents
[06]: 06/
[07]: 07/
[08]: 08/
[09]: 09/
[10]: 10/
[11]: 11/
[12]: 12/
[PIII]: #contents
[13]: 13/
[14]: 14/
[15]: 15/
[16]: 16/
[17]: 17/
[18]: 18/
[19]: 19/
[20]: 20/

<!-- ref -->
[Deep Learning Book]: https://www.deeplearningbook.org
[Lecture]: https://www.deeplearningbook.org/lecture_slides.html
[github]: https://github.com/janishar/mit-deep-learning-book-pdf

<!-- fig -->
[cover]: https://images-na.ssl-images-amazon.com/images/I/61fim5QqaqL._SX373_BO1,204,203,200_.jpg

<style type="text/css">
	img{width: 51%; float: right;}
</style>