<!--
Filename: 	note.md
Project: 	/Users/shume/Developer/DeepLearningBook/02
Author: 	shumez <https://github.com/shumez>
Created: 	2019-05-30 18:20:7
Modified: 	2019-06-03 20:55:1
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
* vectors: \(x\)

\[
	x = 
	\begin{bmatrix}
		x_1 \\ x_2 \\ \vdots \\ x_n
	\end{bmatrix}
	\tag{2.1}
\]

* matrices: \(A\)

\[
	A = 
	\begin{bmatrix}
		A_{1,1} & A_{1,2} \\
		A_{2,1} & A_{2,2} \\
		A_{3,1} & A_{3,2}
	\end{bmatrix} \Rightarrow A^T =
	\begin{bmatrix}
		A_{1,1} & A_{2,1} & A_{3,1} \\
		A_{1,2} & A_{2,2} & A_{3,2}
	\end{bmatrix}
\]

* tensors: \(\mathsf{A}\) 

\(A_{i, j, k}\)

def transposition
\[ (A^T)_{i,j} = A_{j,i} \tag{2.3} \]

\(C = A + B\) where \(C_{i,j} = A_{i,j} + B_{i,j}\)

\(D = a \cdot B + c\) where \(D_{i,j} = a \cdot B_{i,j} + c\)

\(C = A + b\) where \(C_{i,j} = A_{i,j} + b_j\)  
**broadacsting**


## 02.02. Multiplying Matrices and Vectors

**matrix product**  
\[ C = AB \tag{2.4} \]
\[ C_{i,j} = \sum_k{A_{i,k} B_{k,j}} \tag{2.5} \]

**element-wise product** (aka, **Hadamard product**)  
\[ C = A \odot B \]
\[ C_{i,j} = A_{i,j} B_{i,j} \]

**dot product**: 
\(x \cdot y = x^T y\)


\[ x^T y = y^T x \tag{2.8} \]

\[ (AB)^T = B^T A^T \tag{2.9} \]

\[ x^T y = (x^T y)^T = y^T x \tag{2.10} \]

a system of linear equations:

\[ Ax = b \tag{2.11} \]

where \(A \in \mathbb{R}^{m \times n}\), \(b \in \mathbb{R}^m\), \(x \in \mathbb{R}^n\)

\[
	\begin{align*}
		A_{1,:} x &= b_1 \tag{2.12} \\
		A_{2,:} x &= b_2 \tag{2.13} \\
		\vdots \tag{2.14} \\
		A_{m,:} x &= b_m \tag{2.15} \\
	\end{align*}
\]

\[ 
	\begin{align*}
		A_{1,1} x_1 + A_{1,2} x_2 + \cdots + A_{1,n} x_n &= b_1 \tag{2.16} \\
		A_{2,1} x_1 + A_{2,2} x_2 + \cdots + A_{2,n} x_n &= b_2 \tag{2.17} \\
		\vdots \tag{2.18} \\
		A_{m,1} x_1 + A_{m,2} x_2 + \cdots + A_{m,n} x_n &= b_m \tag{2.19} 
	\end{align*}
\]


## 02.03. Identity and Inverse Matrices

**matrix inversion**

**identity matrix** \(I_n \in \mathbb{R}^{n \times n}\)

\[ \forall x \in \mathbb{R}^n, \quad I_n x = x \tag{2.20} \]

\[ A^{-1} A = I_n \tag{2.21} \]


## 02.04. Linear Dependence and Span

in order for \(A^{-1}\) to exist

\[ Ax = b \tag{2.11} \]

eq.2.11 must have one solution

possible to have no solution / infinitely many solutions  
**NOT** possible to have more than 1 but less than infinitely solutions

if both \(x\) and \(y\) are solutions then

\[ z = \alpha x + (1 - \alpha) y \tag{2.26} \]

is also solution for any real \(\alpha\)

\[ Ax = \sum_i{x_i A_{:,i}} \tag{2.27} \]

**linear combination**

\(\{ v^{(1)}, \cdots, v^{(n)} \}\)

\[ \sum_i{c_i v^{(i)}} \tag{2.28} \]

**span** 

\(Ax = b\) have solution for all vals of \(b \in \mathbb{R}^m\)


## 02.05. Norms

**norm**: fn that measure size of vectors 

\(L^p\) norm is given by

\[ ||x||_p = \Bigg( \sum_i{|x_i|^p} \Bigg)^{\frac{1}{p}} \tag{2.30} \]

for \(p \in \mathbb{R}\), \(p \ge 1\)

* \(f(x) = 0\) &rArr; \(x=0\)
* \(f(x + y) \le f(x) + f(y)\) (**triangle inequality**)
* \(\forall\alpha \in \mathbb{R}\), \(f(\alpha x) = |\alpha| f(x)\)

\(L^2\) norm, with \(p=2\) ka **Euclidean norm** (\(||x||\))

\(L^1\) norm

\[ ||x||_1 = \sum_i{|x_i|} \tag{2.31} \]

\(L^\infty\) norm (aka, **max norm**)

\[ ||x||_\infty = \max_i{|x_i|} \tag{2.32} \]

**Frobenius norm**

\[ ||A||_F = \sqrt{\sum_{i,j}{A_{i,j}^2}} \tag{2.33} \]
is analogous to \(L^2\) norm of vec

\[ x^T y = ||x||_2 ||y||_2 \cos{\theta} \tag{2.34} \]

where \(\theta\) is angle between \(x\), \(y\)


## 02.06. Special Kinds of Matricesand Vectors

**diagonal** \(D\)  
if and only if \(D_{i,j}=0\) for all \(i \ne j\)

```py
np.random.seed(123)
v = np.random.randint(9, size=5)
np.diag(v)
```
```py
array([[2, 0, 0, 0, 0],
       [0, 2, 0, 0, 0],
       [0, 0, 6, 0, 0],
       [0, 0, 0, 1, 0],
       [0, 0, 0, 0, 3]])
```

\[ \text{diag}(v) x = v \odot x \]

```py
np.matmul(np.diag(v), x)

np.multiply(v, x)
```

\[ \text{diag}(v)^{-1} = \text{diag}\Bigg( \bigg[\frac{1}{v_1}, \ldots, \frac{1}{v_n} \bigg]^T \Bigg) \]

```py
np.linalg.inv(diag_v)
np.diag([1/vi for vi in v])
```

**symmetric** mat

\[ A = A^T \tag{2.35} \]

**unit vector**: vec w/ **unit norm**:

\[ ||x||_2 = 1 \tag{2.36} \]

vec \(x\) and vec \(y\) **orthogonal** to each other if \(x^T y = 0\)

orthogonal & unit norm **orthonormal**

**orthogonal matrix**

\[ A^T A = A A^T = I \tag{2.37} \]

implies 
\[ A^{-1} = A^T \tag{2.38} \]


```py
from scipy.stats import ortho_group

A = ortho_group.rvs(dim = 3)

np.set_printoptions(suppress=True)
AT_A = np.matmul(A, A.T)
```


## 02.07. Eigendecomposition

**eigendecomposition**: into set of eigenvectors & eigenvalues

**eigenvector** of square mat \(A\) is non-zero vec \(v\)
\[ Av = \lambda v \tag{2.39} \]

**eigenvalue** \(\lambda\) 

```py
l, V = np.linalg.eig(A)
```

[![Fig.2.3][fig0203]][fig0203]

mat \(A\) has \(n\) linearly independent eigenvec \(\{ v^{(1)}, \cdots, v^{(n)} \}\),
w/ corresponding eigenval \(\{ \lambda_1, \cdots, \lambda_n \}\)

mat \(V\): \(V = [ v^{(1)}, \cdots, v^{(b)} ] \),  
vec \(\lambda\): \([\lambda_1, \cdots, \lambda_n]^T\)

**eigendecomposition**

\[ A = V\text{diag}(\lambda) V^{-1} \tag{2.40} \]

```py
np.linalg.multi_dot([V, np.diag(l), np.linalg.inv(V)])
```

\[
	\begin{align*}
		A &= Q \Lambda Q^T \\
		&= 
		\begin{bmatrix}
			v_1 & v_2 & \cdots & v_n
		\end{bmatrix}
		\begin{bmatrix}
			\lambda_1 & 0 & \cdots & 0 \\
			0 & \lambda_2 & \cdots & 0 \\
			\vdots & \vdots & \ddots & \vdots \\
			0 & 0 & \cdots & \lambda_n 
		\end{bmatrix}
		\begin{bmatrix}
			v_1 \\ v_2 \\ \vdots \\ v_n
		\end{bmatrix}
	\end{align*}
	\tag{2.41} 
\]
  
eigenvectors, orthogonal mat \(Q\) of \(A\),  
eigenvalues, diagonal mat \(\Lambda\) of \(A\)

eigenvalue \(\Lambda_{i,i}\) is associated w eigenvector \(Q_{:,i}\)

\(f(x) = x^T Ax \quad (||x|| = 1)\)


* **positive definite**: mat whose eigenval are all positive
* **positive semidefinite**: eigenvals are all positive / zero
* **negative definite**: eigenvals all negative
* **negative semidefinite**: eigenvals negative / zero


positive semideginite mat   
\(\forall x, x^T Ax \ge 0\)

positive definite mat  
\(x^T Ax = 0 \Rightarrow x = 0\)


## 02.08. Singular Value Decomposition

**singular value decomposition** (SVD)  
**singular vecs**, **singular vals**

```py
u, s, vh = np.linalg.svd(A, full_matrices=False)
```

eigendecomposition
\[ A = V \text{diag}(\lambda) V^{-1} \tag{2.42} \]

singular value decomposition
\[ A = UDV^T \tag{2.43} \]

\(A\) \(m \times n\) mat  
**left-singular vec** \(U\) \(m \times m\) orthogonal mat  
**singular values** \(D\) \(m \times n\) diagonal mat  
**right-singular vec** \(V\) \(n \times n\) orthogonal mat


## 02.09. The Moore-Penrose Pseudoinverse

\[
	\begin{align*}
		Ax &= y \tag{2.44} \\
		x &= By \tag{2.45}
	\end{align*}
\]

left-inverse \(B\) of mat \(A\)

**Moore-Penrose pseudoinverse**

pseudoinverse of \(A\) is defined as 

\[  A^+ = \lim\limits_{\alpha \to 0} (A^T A + \alpha I)^{-1} A^T \tag{2.46} \]

\[ A^+ = V D^+ U^+ \tag{2.47} \]

~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~


## 02.10. The Trace Operator

\[ \mathrm{Tr}(A) = \sum_i{A_{i,i}} \tag{2.48} \]

Frobenius norm 

\[ ||A||_F = \sqrt{\mathrm{Tr}(A A^T)} \tag{2.49} \]

\[ \mathrm{Tr}(A) = \mathrm{Tr}(A^T) \tag{2.50} \]

\[ \mathrm{Tr}(ABC) = \mathrm{Tr}(CAB) = \mathrm{Tr}(BCA) \tag{2.51} \]

more generally

\[ \mathrm{Tr}\bigg(\prod_{i=1}^n{F^{(i)}}\bigg) = \mathrm{Tr}\bigg( F^{(n)} \prod_{i=1}^{n-1}{F^{(i)}} \bigg) \tag{2.52} \]

\(A \in \mathbb{R}^{m \times n}\), \(B \in \mathbb{R}^{n \times m}\)  
\[ \mathrm{Tr}(AB) = \mathrm{Tr}(BA) \tag{2.53} \]

though \(AB \in \mathbb{R}^{m \times m}\), \(BA \in \mathbb{R}^{n \times n}\)


## 02.11. The Determinant

\(\det{(A)}\)


## 02.12. Example: Principal Components Analysis

**principal components analysis** (PCA)

\(m\) points \(\{ x^{(1)}, \ldots, x^{(m)} \}\) in \(\mathbb{R}^n\)

lower-dim version  
corresponding code vec \(c^{(i)} \in \mathbb{R}^l\)  
\(l < n\)

encoding fn \(f(x) = c\)  
decoding fn \(x \approx g(f(x))\)


map code back into \(\mathbb{R}^n\)  
let \(g(c) = Dc\), where \(D \in \mathbb{R}^{n \times l}\)

\(L^2\) norm:  
\[ c^* \arg_c\min{||x - g(c)||_2} \tag{2.54} \]

\[ c^* = \arg_c\min{||x - g(c)||_2^2} \tag{2.55} \]

\[
	\begin{align*} 
		&(x - g(c))^T (x - g(c)) \tag{2.56} \\
		&= x^T x - x^T g(c) - g(c)^T x + g(c)^T g(c) \tag{2.57} \\
		&= x^T x - 2x^T g(c) + g(c)^T g(c) \tag{2.58}
	\end{align*} 
\]


~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~ ~


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
[fig0203]: https://raw.githubusercontent.com/shumez/DeepLearningBook/master/02/fig/0203.png

<!-- term -->

<style type="text/css">
	img{width: 51%; float: right;}
</style>