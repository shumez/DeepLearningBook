<!--
Filename: 	note.md
Project: 	/Users/shume/Developer/DeepLearningBook/02
Author: 	shumez <https://github.com/shumez>
Created: 	2019-05-30 18:20:7
Modified: 	2019-06-01 17:56:24
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

**matrix product**  
\[ \mathbf{C} = \mathbf{AB} \tag{2.4} \]
\[ C_{i,j} = \sum_k{A_{i,k} B_{k,j}} \tag{2.5} \]

**element-wise product** (aka, **Hadamard product**)  
\[ \mathbf{C} = \mathbf{A} \bigodot \mathbf{B} \]
\[ C_{i,j} = A_{i,j} B_{i,j} \]

**dot product**: 
\(\mathbf{x} \cdot \mathbf{y} = \mathbf{x}^T \mathbf{y}\)


\[ \mathbf{x}^T \mathbf{y} = \mathbf{y}^T \mathbf{x} \tag{2.8} \]

\[ (\mathbf{AB})^T = \mathbf{B}^T \mathbf{A}^T \tag{2.9} \]

\[ \mathbf{x}^T \mathbf{y} = (\mathbf{x}^T \mathbf{y})^T = \mathbf{y}^T \mathbf{x} \tag{2.10} \]

a system of linear equations:

\[ \mathbf{Ax} = \mathbf{b} \tag{2.11} \]

where \(\mathbf{A} \in \mathbb{R}^{m \times n}\), \(\mathbf{b} \in \mathbb{R}^m\), \(\mathbf{x} \in \mathbb{R}^n\)

\[
	\begin{align*}
		\mathbf{A}_{1,:} \mathbf{x} &= b_1 \tag{2.12} \\
		\mathbf{A}_{2,:} \mathbf{x} &= b_2 \tag{2.13} \\
		\vdots \tag{2.14} \\
		\mathbf{A}_{m,:} \mathbf{x} &= b_m \tag{2.15} \\
	\end{align*}
\]

\[ 
	\begin{align*}
		\mathbf{A}_{1,1} x_1 + \mathbf{A}_{1,2} x_2 + \cdots + \mathbf{A}_{1,n} x_n &= b_1 \tag{2.16} \\
		\mathbf{A}_{2,1} x_1 + \mathbf{A}_{2,2} x_2 + \cdots + \mathbf{A}_{2,n} x_n &= b_2 \tag{2.17} \\
		\vdots \tag{2.18} \\
		\mathbf{A}_{m,1} x_1 + \mathbf{A}_{m,2} x_2 + \cdots + \mathbf{A}_{m,n} x_n &= b_m \tag{2.19} 
	\end{align*}
\]


## 02.03. Identity and Inverse Matrices

**matrix inversion**

**identity matrix** \(\mathbf{I}_n \in \mathbb{R}^{n \times n}\)

\[ \forall\mathbf{x} \in \mathbb{R}^n, \mathbf{I}_n \mathbf{x} = \mathbf{x} \tag{2.20} \]

\[ \mathbf{A}^{-1} \mathbf{A} = \mathbf{I}_n \tag{2.21} \]


## 02.04. Linear Dependence and Span

in order for \(\mathbf{A}^{-1}\) to exist

\[ \mathbf{Ax} = \mathbf{b} \tag{2.11} \]

eq.2.11 must have one solution

possible to have no solution / infinitely many solutions  
**NOT** possible to have more than 1 but less than infinitely solutions

if both \(\mathbf{x}\) and \(\mathbf{y}\) are solutions then

\[ \mathbf{z} = \alpha \mathbf{x} + (1 - \alpha) \mathbf{y} \tag{2.26} \]

is also solution for any real \(\alpha\)

**origin**

\[ \mathbf{Ax} = \sum_i{x_i \mathbf{A}_{:,i}} \tag{2.27} \]

**linear combination**


\[ \sum_i{c_i \mathbf{v}^{(i)}} \tag{2.28} \]


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