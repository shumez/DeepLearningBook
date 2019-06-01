<!--
Filename: 	note.md
Project: 	/Users/shume/Developer/DeepLearningBook/02
Author: 	shumez <https://github.com/shumez>
Created: 	2019-05-30 18:20:7
Modified: 	2019-06-01 15:22:5
-----
Copyright (c) 2019 shumez
-->

# [02. Linear Algebra]

## Contents

* [02.00.][0200]
* [02.01. Scalars, Vectors, Matrices and Tensors][0201]
* [02.02. Multiplying Matrices and Vectors][0202]
* [02.03. Identity and Inverse Matrices][0203]
* [02.04. Linear Dependence and Span][0204]
* [02.05. Norms][0205]
* [02.06. Special Kinds of Matricesand Vectors][0206]
* [02.07. Eigendecomposition][0207]
* [02.08. Singular Value Decomposition][0208]
* [02.09. The Moore-Penrose Pseudoinverse][0209]
* [02.10. The Trace Operator][0210]
* [02.11. The Determinant][0211]
* [02.12. Example: Principal Components Analysis][0212]

## 02.00.

*The Matrix Cookbook* ([Peterson, Pedersen, 2006][2006_Pedersen_Peterson])  
[Shilov, 1977][1977_Shilov]


## 02.01. Scalars, Vectors, Matrices and Tensors

* scalars
* vectors: \(\mathbf{x}\)

\[
	\mathbf{x} = 
	\begin{bmatrix}
		x_1 \\ x_2 \\ \vdots \\ x_n
	\end{bmatrix}
	\tag{2.1}
\]

* matrices: \(\mathbf{A}\)

\[
	\mathbf{A} = 
	\begin{bmatrix}
		A_{1,1} & A_{1,2} \\
		A_{2,1} & A_{2,2} \\
		A_{3,1} & A_{3,2}
	\end{bmatrix} \Rightarrow \mathbf{A}^T =
	\begin{bmatrix}
		A_{1,1} & A_{2,1} & A_{3,1} \\
		A_{1,2} & A_{2,2} & A_{3,2}
	\end{bmatrix}
\]

* tensors: \(\mathsf{A}\) 

\(A_{i, j, k}\)

def transposition
\[ (\mathbf{A}^T)_{i,j} = \mathbf{A}_{j,i} \tag{2.3} \]

\(\mathbf{C} = \mathbf{A} + \mathbf{B}\) where \(C_{i,j} = A_{i,j} + B_{i,j}\)

\(\mathbf{D} = a \cdot \mathbf{B} + c\) where \(D_{i,j} = a \cdot B_{i,j} + c\)

\(\mathbf{C} = \mathbf{A} + \mathbf{b}\) where \(C_{i,j} = A_{i,j} + b_j\)  
**broadacsting**


## 02.02. Multiplying Matrices and Vectors


## 02.03. Identity and Inverse Matrices


## 02.04. Linear Dependence and Span


## 02.05. Norms


## 02.06. Special Kinds of Matricesand Vectors


## 02.07. Eigendecomposition


## 02.08. Singular Value Decomposition


## 02.09. The Moore-Penrose Pseudoinverse


## 02.10. The Trace Operator


## 02.11. The Determinant


## 02.12. Example: Principal Components Analysis


##
[02. Linear Algebra]: https://www.deeplearningbook.org/contents/linear_algebra.html

<!-- toc -->
[0200]: #0200
[0201]: #0201_scalars_vectors_matrices_and_tensors
[0202]: #0202_multiplying_matrices_and_vectors
[0203]: #0203_identity_and_inverse_matrices
[0204]: #0204_linear_dependence_and_span
[0205]: #0205_norms
[0206]: #0206_special_kinds_of_matricesand_vectors
[0207]: #0207_eigendecomposition
[0208]: #0208_singular_value_decomposition
[0209]: #0209_the_moore-penrose_pseudoinverse
[0210]: #0210_the_trace_operator
[0211]: #0211_the_determinant
[0212]: #0212_example_principal_components_analysis

<!-- ref -->
[2006_Pedersen_Peterson]: #02_linear_algebra
[1977_Shilov]: #02_linear_algebra

<!-- fig -->

<!-- term -->

<style type="text/css">
	img{width: 51%; float: right;}
</style>