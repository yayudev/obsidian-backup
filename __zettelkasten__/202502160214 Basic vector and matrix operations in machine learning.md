---
tags:
  - machine-learning
  - matrices
  - vectors
  - math
  - dot-product
  - matrix-multiplication
  - transpose
  - L2-norm
  - unitary-vector
source: "[[Math and Architectures of Deep Learning]]"
Date: 2025-02-16
---
#### Matrix Transpose
- Matrix transpose is basically flipping a matrix over its diagonal.
- Example:
	- Given the matrix: $$
\begin{bmatrix}
	0 & 1 & 2 \\
	3 & 4 & 5 \\
	6 & 7 & 8 \\
\end{bmatrix}$$
	- Its transposed version will be: $$
\begin{bmatrix}
	0 & 3 & 6 \\
	1 & 4 & 7 \\
	2 & 5 & 8 \\
\end{bmatrix}$$

- The transpose of a MxN matrix (M rows, N columns) is another NxM matrix (N rows, M columns).
- So for a $A_{n,m}$ matrix, the transpose will be $A^T_{n,m}$.
- For a transposed matrix, $A^T[i, j]$ will be equal to $A[j, i]$.
- This also applies to vectors.
	- For a vector $$\vec{v} = \begin{bmatrix} 1 \\ 2 \\ 3 \end{bmatrix}$$
	- Its transpose will be: $$\vec{v}^T = \begin{bmatrix} 1 & 2 & 3 \end{bmatrix}$$
#### Dot product
- The dot product is the multiplication of two vectors ($\vec{x}$, $\vec{w}$) sum together.
- For a vector $\vec{x}$ and $\vec{w}$: $$
\vec{x} \cdot \vec{w} = x_0w_0 + x_1w_1 + x_2w_2 + \dots + w_nw_n
$$
- Dot product can only happen between 2 vectors of same length because we need to multiply each term in $\vec{x}$ by the corresponding term in $\vec{w}$.
- Example:
	- Given: $$
		\vec{x} = \begin{bmatrix} 1 & 2 & 3 \end{bmatrix}
		\space \space \space
		\vec{w} = \begin{bmatrix} 3 & 4 & 5 \end{bmatrix}
		$$
	- $$
	\vec{x} \cdot \vec{w} \\
		= x_0w_0 + x_1w_1 + x_2w_2 \\
		=(1)(3) + (2)(4) + (3)(5) \\
		= 3 + 8 + 15 \\
		= 26 \\
	$$
- Sometimes can also be referred as inner product, denoted $\langle \vec{a} , \vec{b} \rangle$.

#### Matrix multiplication
- Matrix multiplication can only happen between a matrix $M\times N$ ($M$ rows, $N$ columns) and another matrix $N\times P$ ($N$ rows, $P$ columns).
- Basically, matrix A must have same number of columns as Matrix B has rows.
- The result will have $M \times P$ length.
- The way it happens is as it follows:
	- $$
\begin{bmatrix} 
	x_{00} & x_{01} \\
	x_{10} & x_{11} \\
	x_{20} & x_{21} \\
\end{bmatrix}
\begin{bmatrix} 
	w_{00} & w_{01} \\
	w_{10} & w_{11} \\
\end{bmatrix}
= 
\begin{bmatrix} 
	(x_{00}w_{00} + x_{01}w_{10}) & 
	(x_{00}w_{01} + x_{01}w_{11}) \\
	
	(x_{10}w_{00} + x_{11}w_{10}) & 
	(x_{10}w_{01} + x_{11}w_{11}) \\
	
	(x_{20}w_{00} + x_{21}w_{10}) & 
	(x_{20}w_{01} + x_{21}w_{11})  \\
\end{bmatrix}
$$
- Example: $$
\begin{bmatrix} 
	1 & 2 \\
	3 & 4 \\
	5 & 6 \\
\end{bmatrix}
\begin{bmatrix} 1  \\ 2 \end{bmatrix}
= \\
\begin{bmatrix} 
	(1\times1) + (2\times2) \\
	(3\times1) + (4\times2) \\
	(5\times1) + (6\times2) \\
\end{bmatrix}
= \\
\begin{bmatrix} 
	​5\\
	11\\
	17​
\end{bmatrix}
$$
- Note that since matrix multiplication is not commutative. In general, $AB \ne BA$.

#### Transposed matrix multiplication
- Given two matrices A and B, the transposed of the product is the product of individual transposes in reverse order. 
- $(AB)^T = B^TA^T$
- Example:
	-  $$\begin{pmatrix}
\begin{bmatrix} 
	1 & 2 \\
	3 & 4
\end{bmatrix}
\begin{bmatrix} 
	0 & 1 \\
	2 & 3
\end{bmatrix}
\end{pmatrix}
^T
= 
\begin{bmatrix} 
	4 & 7 \\
	8 & 15 \\
\end{bmatrix}^T
=
\begin{bmatrix} 
	4 & 8 \\
	7 & 15 \\
\end{bmatrix}
$$
	-   $$
\begin{bmatrix} 
	0 & 1 \\
	2 & 3
\end{bmatrix}^T
\begin{bmatrix} 
	1 & 2 \\
	3 & 4
\end{bmatrix}^T
= 
\begin{bmatrix} 
	0 & 2 \\
	1 & 3
\end{bmatrix}
\begin{bmatrix} 
	1 & 3 \\
	2 & 4
\end{bmatrix}
=
\begin{bmatrix} 
	4  &  8 \\
	7  & 15 \\
\end{bmatrix}
$$
#### Squared Model Error (Square L2 Norm)
- When we measure the output of a model, we care about the error made by the model to adjust the parameters.
- The error is the difference between the target ( $\overline{y}$ ) and the actual ( $y$ ) outputs.
- Can be defined as: $$e = (\overline{y} - y)$$
- When we calculate the error, we don't care about the exact value or the sign, only about how far from the actual value is.
- As such, a common practice is to square the error to get rid of the sign. $$ E^2 = (\overline{y} - y)^2$$
- Since these are vectors, we can just multiply the vector by the transpose of itself, which equals to the dot product of the errors:
- $$ 
E^2 = (\overline{y} - y)^2 
	= (\overline{y} - y)^T(\overline{y} - y)
	= (\overline{y} - y) \cdot (\overline{y} - y)
$$
-  Example: $$
E^2 
=
\begin{bmatrix}
	.5 \\
	.25 \\
	.75
\end{bmatrix}^2
=
\begin{bmatrix}
	.5 \\
	.25 \\
	.75
\end{bmatrix}
\cdot
\begin{bmatrix}
	.5 \\
	.25 \\
	.75
\end{bmatrix}
	= .25 + 0.0625 + 0.5625 = 0.875
$$
- To get a better sense of the general error, we can take that square root of this $E^2$. $$
e = ||(\overline{y} - y)||= \sqrt{E^2} = \sqrt{(\overline{y} - y) \cdot (\overline{y} - y)} = \sqrt{(\overline{y} - y)^T(\overline{y} - y)}
$$
- In the previous example: $$
e = \sqrt{E^2} = \sqrt{0.875} = 0.93541434669
$$
#### Unit vectors
- A unit vector is a vector whose length is 1
- Examples: 
	- $[1, 0]$ is 1 length pointing towards x-axis 
	- $[0, 1]$ is 1 length pointing towards y-axis.
	- $\begin{bmatrix}\frac{1}{\sqrt{2}}, \frac{1}{\sqrt{2}}\end{bmatrix}$ is a diagonal with length 1.

#### Dot product as geometric components
- Dot product can also be counted as: $$
\vec{a} \cdot \vec{b} = \vec{a}^T \vec{b} = a_xb_x + a_yb_y =||\vec{a}||\space||\vec{b}||cos(\theta)
$$
- Expressing the dot product as cosines makes easier to measure the agreement or correlation between two vectors.
	- If vectors have same direction, the angle is 0 and cosine is 1. That implies agreement.
	- If vectors are perpendicular to each other the angle increases and eventually reaches 0, implying no correlation. This is also know as orthogonal vectors.
	- If angle between them is close to 180deg, then the value goes to -1 implying they are anti-correlated.