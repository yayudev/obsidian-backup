---
tags:
  - "#math"
  - "#vectors"
  - "#AI"
  - machine-learning
source: "[[Math and Architectures of Deep Learning]]"
Date: 2025-02-14
---
#### Vectors
- Vectors can be thought of as an ordered array of two or more numbers.
- Vectors usually are a way to represent something via its components. Like a color could be represented using $\begin{bmatrix}R & G & B\end{bmatrix}$ values.

#### Geometric view of vectors
- Vectors can also be seen geometrically.
- The simplest example is a two-element vector $\vec{x} = \begin{bmatrix} x_0 \\ x_1 \end{bmatrix}$
- A 2D vector can correspond to a point in a 2D space.
- Vectors with $n$ elements can represent a point in a $n$-dimensional space.
- A vector containing coordinates with shape $\begin{bmatrix} x \\ y \end{bmatrix}$ describes the position of a point *within a given coordinate system*.
- In machine learning, it doesn't matte what the coordinate system is as long as we stick to a fixed coordinate system.
- Machine learning is about minimizing loss functions so absolute positions are not relevant, only the relative positions matter.
- In machine learning, we often deal with spaces with thousands of dimensions.

#### Vector in PyTorch
- Create a vector:
```python
vector = torch.tensor(
	 [0.11, 0.01, 0.98, 0.12], # 1D Vector
	 dtype=torch.float64,      # 64bit floats 
 ) 
```
- Accessing elements
```python
first_element = vector[0]
last_element = vector[-1]

second_to_fifth_elements = vector[1:5]
```
- Operations
```python
vector2 = [0.0, 0.1, 0.2, 0.3]
vector.sub(vector2) # [0.11, −0.09, 0.78, −0.18]
```
